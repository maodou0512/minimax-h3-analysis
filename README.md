# MiniMax H3 分析笔记

面向研究者与工程师的 **MiniMax H3**（Hailuo 3.0）开放资料整理与架构解读。  
本仓库**不是**官方推理/训练代码，也不托管模型权重；目标是把「系统怎么拆、能做什么、本地 vs API 怎么走」说清楚。

> 主要依据：[MiniMax 官方开源公告](https://www.minimax.io/news/minimax-h3-open-source)（2026-08-03）、Hugging Face [`MiniMaxAI/MiniMax-H3`](https://huggingface.co/MiniMaxAI/MiniMax-H3)、[H3 Open 资源页](https://design.minimax.io/h3)。未核到的数字会标明「待核实」，**不会编造榜单分数**。

## H3 是什么

MiniMax H3 是面向**通用视频生成**的开源全模态（omni-modal）系统：统一理解文本 / 图像 / 视频 / 音频组成的多模态上下文，并在**同一次前向**中生成带**原生立体声音频**的视频。

| 项目 | 规格（官方公开信息） |
| --- | --- |
| 参数规模 | 约 **33B** 稠密 Omni-Transformer（其中约 **13B** 在 AdaLN 相关分支） |
| 文本编码器 | **Qwen3-VL-32B**（取第 50 层 hidden states） |
| 输出时长 | **4–15 秒** |
| 帧率 | **24 FPS** |
| 分辨率 | 开源 Base 默认可生成短边 **768p**；官方 **2K** 走 `H3-Regenerate-2K`（托管） |
| 音频 | **32 kHz 立体声**，与画面同一次生成（非后期配音） |
| 画幅 | 支持多种宽高比（含 21:9、16:9、4:3、1:1、3:4、9:16 等） |
| 对白语言 | 稳定支持 11 种：ar / zh / en / fr / de / it / ja / ko / pt / ru / es |

## 三件套：开源 vs 托管

完整官方链路由三个模块组成：

```mermaid
flowchart LR
  A[多模态输入<br/>text / image / video / audio] --> B[H3-Context-IR<br/>托管 · 指令理解与中间表示]
  B --> C[H3-Base<br/>开源权重 · 768p 音视频]
  C --> D[H3-Regenerate-2K<br/>托管 · 上下文内 2K 再生成]
```

| 模块 | 是否开源 | 作用 |
| --- | --- | --- |
| **H3-Context-IR** | 否（提供 API） | 解析复杂多模态指令，产出 Base 更易消费的 Context Intermediate Representation |
| **H3-Base** | **是**（FL2VA / Ref2VA） | 基于 IR / 提示生成 **768p** 视频 + 立体声 |
| **H3-Regenerate-2K** | 否（提供 API） | 把 768p 结果与原始上下文一起，用 in-context 方式再生成 **2K** |

实用含义：个人可以只部署 Base 做本地 768p 迭代；要官方级 2K 或完整 Context-IR，需要对接 MiniMax Open Platform API。

## 两个开源检查点

| Checkpoint | 任务 | 典型输入 |
| --- | --- | --- |
| **FL2VA** | Text / First-Last-Frame → Audio-Video | 纯文本；或首帧 / 末帧 / 首末帧图像 |
| **Ref2VA** | Omni-reference → Audio-Video | 文本 + 最多 9 图 / 3 视频片段 / 3 音频片段（跨类型文件总数 ≤ 12；音频不能单独作为唯一输入） |

权重与组件按 Hugging Face 风格目录分发（`processor/`、`tokenizer/`、`text_encoder/`、`transformer/`、`visual_vae/`、`audio_vae/` 等）。官方示例下载：

```bash
hf download MiniMaxAI/MiniMax-H3 --include "FL2VA/*" "Ref2VA/*" --local-dir MiniMax-H3
```

## 架构速览

- **统一 packed 多模态序列**：各模态经对应 encoder / VAE 编码后拼成一条序列，经 **MM-RoPE**（t, h, w）进入 Omni-Transformer。
- **VisualVAE**：时空因果视频自编码器，记为 **f16t4d24**（空间 16×、时间 4×、24 latent 通道）；再经 `1×2×2` patchify，进入 Transformer 的视觉 token 等效空间下采样约 **32×**。
- **AudioVAE**：左右声道共享编解码器、分通道处理再合成立体声；32 kHz → 约 **40 Hz** latent 序列。
- **Omni-Transformer**：单流稠密设计；模态专用参数主要落在输入输出与 **AdaLN** 分支。AdaLN 调制可预计算缓存，推理部署可不加载对应参数；完整权重仍发布以便微调。
- **稀疏注意力**：训练后期引入 native sparse attention；**首发开源推理为 full attention**，稀疏实现后续单独发布。

更细的拆解见 [`docs/architecture.md`](docs/architecture.md)。

## 本地部署入口（摘要）

官方推荐框架（详见 [`docs/deployment.md`](docs/deployment.md)）：

- [SGLang](https://github.com/sgl-project/sglang)
- [vLLM](https://github.com/vllm-project/vllm) / vLLM-Omni 相关配方
- [diffusers](https://github.com/huggingface/diffusers)
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI)（day-0 工作流模板）

SGLang 示例（需多卡，以官方 cookbook 为准）：

```bash
sglang serve \
  --model-path MiniMaxAI/MiniMax-H3 \
  --num-gpus 4 \
  --ulysses-degree 4 \
  --performance-mode speed \
  --host 0.0.0.0 \
  --port 30010 \
  --model-variant fl2va
```

## 文档导航

| 文档 | 内容 |
| --- | --- |
| [架构分析](docs/architecture.md) | Encoder / VAE / Transformer / 2K 再生成 |
| [模型变体](docs/variants.md) | FL2VA vs Ref2VA 输入约束 |
| [能力与提示](docs/capabilities.md) | I/O、Context-IR、语言与安全护栏 |
| [部署指南](docs/deployment.md) | 本地 768p 与 Full 2K 工作流 |
| [对比与定位](docs/comparison.md) | 与同代视频模型的对比框架（无编造榜单） |
| [社区版本手册](docs/community-versions.md) | 开源/量化/Turbo/ControlNet 等发行对照、下载与硬件 |
| [资料索引](docs/sources.md) | 一手链接与二次资料 |

## 许可证提示

上游模型遵循 **MiniMax H3 Community License Agreement**。本仓库文档以整理与解读为目的；使用权重与衍生作品前请阅读官方许可与 [License Q&A](https://www.minimax.io/news/minimax-h3-open-source)。见 [`NOTICE`](NOTICE)。

## 贡献

欢迎纠错与补充一手链接，见 [`CONTRIBUTING.md`](CONTRIBUTING.md)。

## English summary

**MiniMax H3** is a ~33B dense omni-modal video model that generates **video + native stereo audio** in one pass (4–15s, 24fps). Open weights cover **H3-Base** (**FL2VA** / **Ref2VA**) at ~768p short-side; **H3-Context-IR** and **H3-Regenerate-2K** remain hosted APIs. See `docs/` for architecture, variants, deployment, and primary sources.
