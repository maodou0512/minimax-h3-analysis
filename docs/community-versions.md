# MiniMax H3 开源社区版本手册

> 目标：用一份文档快速看清「有哪些开源/社区发行版、谁发的、怎么下、适合什么硬件、各自优缺点」。  
> 整理日期：2026-09-11（同日二次扩写）。社区量化与 VRAM 数字变化很快，**以各仓库 model card 为准**；本页未写死的字段标为「未公开/社区报告」。  
> **不会编造榜单分数**。许可统一注意：上游多为 [MiniMax H3 Community License](https://huggingface.co/MiniMaxAI/MiniMax-H3/blob/main/LICENSE)（含地域与商业门槛）；部分 Turbo/LoRA 标注 Apache-2.0，使用前请逐仓核对。

## 0. 先分清三层

| 层级 | 是什么 | 本地能拿到吗 |
| --- | --- | --- |
| **H3 系统** | Context-IR + Base + Regenerate-2K | 仅 **Base** 开源；IR / 2K 仍托管 API |
| **官方权重** | `FL2VA` / `Ref2VA` BF16 全量（+ diffusers 布局） | 是（HF / ModelScope） |
| **社区发行** | 重打包、量化、Turbo LoRA、ControlNet、微调、合并包 | 是（多为 ComfyUI 友好单文件） |

阅读本手册时：「版本」= 可下载的**权重发行包**（含官方与社区），不是 Hailuo App 里的产品版本号。

## 1. 一分钟选型

| 你的情况 | 建议起点 |
| --- | --- |
| 要对齐官方 / 做 SGLang·vLLM·diffusers 服务 | **MiniMaxAI/MiniMax-H3**（或 ModelScope 镜像） |
| ComfyUI 工作站，要质量+速度平衡 | **Comfy-Org/MiniMax-H3** 的 `pruned_int8_convrot` + `nvfp4_awq` 文本编码器 |
| 显存吃紧（12–16 GB） | GGUF（Abiray / unsloth 等）或 pruned INT8 + Turbo 4/8 step |
| 只要更快出片（可接受音质损失） | **lightx2v** 或 **larryvrh/drbaph** Turbo LoRA |
| 需要线稿/深度/姿态控视频、局部重绘 | **alibaba-pai Fun-Controlnet-Union** |
| Blackwell（50 系）想压显存 | 社区 **NVFP4** 扩散包（非 Blackwell 上多为仿真，优先 INT8） |

## 2. 总览对照表

| 发行名 | 类型 | 发布方 | HF 创建日（约） | 下载入口 | 任务 | 精度/形态 | 特点摘要 | 硬件粗指引 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| MiniMax-H3 Base FL2VA/Ref2VA | 官方基座 | MiniMaxAI | 2026-07-28 仓库创建；公开开源约 **2026-08-03** | [HF](https://huggingface.co/MiniMaxAI/MiniMax-H3) · [ModelScope](https://www.modelscope.cn/models/MiniMax/MiniMax-H3) · [GitHub](https://github.com/MiniMax-AI/MiniMax-H3) | FL2VA / Ref2VA | BF16 分片 | 权威权重；含 processor/tokenizer/VAE；CFG-distilled | 官方示例 **4×GPU** SGLang；全量磁盘约 **~498 GB**（双任务+多布局） |
| Comfy-Org/MiniMax-H3 | ComfyUI 重打包 | Comfy-Org | 2026-07-30 | [HF](https://huggingface.co/Comfy-Org/MiniMax-H3) · [ModelScope](https://modelscope.cn/models/Comfy-Org/MiniMax-H3) | FL2VA / Ref2VA | bf16 / int8_convrot / pruned_* / fp8_scaled；TE：bf16/int8/nvfp4_awq | Day-0 生态；模板工作流；内嵌 Turbo LoRA 与 embeddings | 消费级默认看 pruned INT8；全 bf16 需高端多卡 |
| lightx2v Minimax-h3-Turbo | 蒸馏加速 LoRA | LightX2V | 2026-08-07 | [HF](https://huggingface.co/lightx2v/Minimax-h3-Turbo) | FL2V 4/8 step、Ref2V 4 step 等 | LoRA bf16（Comfy 包内亦有） | 少步数大幅加速；社区测约 **3.4×**（4-step） | 叠在 Base/Comfy 量化上；低显存可开 |
| larryvrh MiniMax-H3-Turbo-Lora | 社区 Turbo LoRA | larryvrh | 2026-08-05 | [HF](https://huggingface.co/larryvrh/MiniMax-H3-Turbo-Lora) | 少步加速 | LoRA | Comfy 生态常用；需专用 loader 节点 | ≤12 GB 常配 `low_vram` |
| drbaph Turbo-Lora-ComfyUI | Turbo 再分发 | drbaph | 2026-08-06 | [HF](https://huggingface.co/drbaph/MiniMax-H3-Turbo-Lora-ComfyUI) | 少步加速 | pruned/动态秩等 | 面向 ComfyUI 的打包与变体 | 同 Turbo 线 |
| Abiray MiniMax-H3-GGUF | GGUF 量化 | Abiray | 2026-08-03 | [HF](https://huggingface.co/Abiray/MiniMax-H3-GGUF) | FL2VA / Ref2VA | Q3–Q8 GGUF + TE/VAE | UNet 约 15.6–36 GB；另有 Pruned-GGUF 更小 | Q4≈16 GB 档；Q5≈24 GB 档（社区） |
| Abiray MiniMax-H3-Pruned-GGUF | 剪枝+GGUF | Abiray | 2026-08-07 | [HF](https://huggingface.co/Abiray/MiniMax-H3-Pruned-GGUF) | 同上 | 约 8.9–21.6 GB | 面向消费卡的更小 UNet | 12 GB 及以下更友好 |
| unsloth MiniMax-H3-GGUF | GGUF | Unsloth | 2026-08-07 | [HF](https://huggingface.co/unsloth/MiniMax-H3-GGUF) | 视频生成 | GGUF | 另一条高下载 GGUF 线；可配 sd.cpp 等 | 视具体 quant，见卡页 |
| realrebelai / molbal / leejet GGUF | GGUF | 社区 | 2026-08 初 | 各 HF 仓 | 多 | GGUF | 并行量化源；选信得过作者与哈希 | 同 GGUF 档 |
| molbal MiniMax-H3-Turbo-GGUF | Turbo 合并 GGUF | molbal | 未在总表单独列优先看卡页 | [HF](https://huggingface.co/molbal/MiniMax-H3-Turbo-GGUF) | FL2VA Turbo 4-step | Q4/Q8/Q8_CR | **合并**蒸馏权重，不需另挂 LoRA | 需 Turbo sampler 节点 |
| Abiray nvfp4-INT4-INT8-Convrot | 低比特量化包 | Abiray | 2026-08-03 | [HF](https://huggingface.co/Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot) | Comfy | NVFP4 / INT4 / INT8 | 低显存组合拳 | INT4 社区报道可下探 6–8 GB（苛刻） |
| rockerBOO / lilcheaty NVFP4 | NVFP4 扩散 | 社区 | 2026-08 起 | [rockerBOO](https://huggingface.co/rockerBOO/minimax-h3-nvfp4) · [lilcheaty](https://huggingface.co/lilcheaty/MiniMax-H3-NVFP4) | 部分仅 Ref2VA | NVFP4 | Blackwell 原生；Ada 上仿真 | 优先 50 系；否则改 INT8 |
| alibaba-pai Fun-Controlnet-Union | ControlNet | 阿里 PAI / VideoX-Fun | 卡页未强调创建日；活跃于 2026-08 | [HF](https://huggingface.co/alibaba-pai/MiniMax-H3-Fun-Controlnet-Union) | V2V 控制+重绘 | ~6.8 GB 控制分支 | Canny/Depth/HED/MLSD/Pose + inpaint；`guidance_scale=1` | 需再加载完整 Base；单卡 80 GB 也常要 offload |
| alibaba-pai Acc-LoRAs | 加速 LoRA | 阿里 PAI | 2026-08-26 | [HF](https://huggingface.co/alibaba-pai/MiniMax-H3-Acc-LoRAs) | 加速 | LoRA | 论文关联加速；有 Comfy 转制仓 | 叠在 Base 上 |
| Kijai experimental / _comfy | 实验分发 | Kijai | 持续更新 | [experimental](https://huggingface.co/Kijai/MiniMax-H3-experimental) · [_comfy](https://huggingface.co/Kijai/MiniMax-H3_comfy) | ControlNet 等 | bf16/int8 等 | Comfy 节点作者生态；含 controlnet 再分发 | 随具体文件 |
| MATLOWAI fused-turbo-int8 | 合并包 | MATLOWAI | 2026-08-29 | [HF](https://huggingface.co/MATLOWAI/minimax-h3-fused-turbo-int8-convrot) | Comfy 单文件 | INT8+Turbo 融合 | 少文件、开箱加速 | 看卡页 VRAM |
| fal Realism-People-LoRA 等 | 风格/题材 LoRA | fal 等 | 2026-08 起 | [例](https://huggingface.co/fal/MiniMax-H3-Realism-People-LoRA) | 风格化 | LoRA | 人像写实等；生态大量 adapters | 额外显存通常不大 |
| WarmBloodAban Singularity 等 | 微调/风格 | 社区 | 2026-09 起 | [例](https://huggingface.co/WarmBloodAban/Minimax-h3_Singularity) | 微调 | 各异 | HDR/风格向微调，非「基座替代」 | 依赖所选 Base 量化 |
| multimodalart MiniMax-H3-Pruned | AdaLN 剪枝（diffusers） | multimodalart | 2026-08-09 | [HF](https://huggingface.co/multimodalart/MiniMax-H3-Pruned) | FL2VA/Ref2VA | pruned BF16 + 截断 TE | DiT 约 66→40 GB/分区；兼容 Comfy 剪枝 LoRA 坐标 | 示例峰值约 52 GB（其 H100 offload 测） |
| DiffSynth-Studio MiniMax-H3-NF4 | NF4 量化 | DiffSynth-Studio | 2026-08-04 | [HF](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-NF4) | FL2VA/Ref2VA | bitsandbytes NF4（含 pruned） | Python/DiffSynth 低显存；可训 LoRA | 作者称磁盘 offload 可至约 **8 GB** VRAM |
| unsloth MiniMax-H3-FP8 | torchao INT8/FP8 | Unsloth | 2026-08-07 | [HF](https://huggingface.co/unsloth/MiniMax-H3-FP8) | FL2VA/Ref2VA | INT8 / INT8-ConvRot / FP8 `.pt` | 基于 Comfy pruned_bf16；非 sd.cpp | 端到端峰值有作者自测下降 |
| coolthor MiniMax-H3-pruned-NVFP4 | NVFP4 | coolthor | 2026-08-04 | [HF](https://huggingface.co/coolthor/MiniMax-H3-pruned-NVFP4)（可能 gated） | FL2VA+Ref2VA | pruned NVFP4 ~11.7 GiB | 双任务 NVFP4 | 5090 峰值约 26.9 GiB（作者） |
| ModelsLab ref2va-NVFP4 | NVFP4 未剪枝 | ModelsLab | 2026-08-03 | [HF](https://huggingface.co/ModelsLab/MiniMax-H3-ref2va-NVFP4) | Ref2VA | NVFP4 ~38.6 GB | 未剪枝体积更大 | 需大显存/Blackwell |
| Ar4ikov transformer-W4A16-RTN | W4A16 | Ar4ikov | 2026-08-03 | [HF](https://huggingface.co/Ar4ikov/MiniMax-H3-transformer-W4A16-RTN) | transformer only | AutoRound W4A16 | AdaLN 保持 BF16；66→38 GB 级 | 未做完整画质对比 |
| FastVideo FastH3 4-step Preview | 蒸馏学生 | FastVideo | 2026-08-27 | [HF](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree) | **仅 T2VA** | 4-step DMD2 + VSA | 少步独立学生模型；preview | 多为多卡示例，非消费级主路径 |
| WanGP / DiffSynth / SGLang 运行时 | 启动器/框架 | 各团队 | — | [Wan2GP](https://github.com/deepbeepmeep/Wan2GP) 等 | 加载官方或社区权重 | — | 低 VRAM 启动与服务配方 | 视所选权重 |

> HF `createdAt` 来自 Hub API（仓库创建时间），**不等于**官方新闻稿发布日。官方开源公告为 **2026-08-03**。

## 3. 官方基座详解

### 3.1 MiniMaxAI/MiniMax-H3（权威）

| 字段 | 内容 |
| --- | --- |
| 名称 | MiniMax-H3（H3-Base：**FL2VA** / **Ref2VA**） |
| 发布方 | MiniMax（MiniMaxAI） |
| 发布时间 | 开源公告 **2026-08-03**；HF 仓约 2026-07-28 起可见 |
| 下载 | https://huggingface.co/MiniMaxAI/MiniMax-H3 |
| 镜像 | https://www.modelscope.cn/models/MiniMax/MiniMax-H3 （ModelScope 统计整库体积约 **498 GB** 量级，勿无筛选全下） |
| 代码/技能 | https://github.com/MiniMax-AI/MiniMax-H3 |
| 精度 | BF16；CFG-distilled Omni Transformer |
| 组件 | 每任务：`processor/` `tokenizer/` `text_encoder/`（Qwen3-VL-32B）`transformer/` `visual_vae/` `audio_vae/`；另有 diffusers 布局 |
| 能力 | 4–15 s、24 fps、短边默认 768p、32 kHz 立体声、11 语对白；FL2VA=文/首末帧；Ref2VA=多参考 |
| **不含** | H3-Context-IR、H3-Regenerate-2K（API） |
| 推荐框架 | SGLang、vLLM、diffusers、ComfyUI |
| 硬件（官方口径） | SGLang 示例：`--num-gpus 4 --ulysses-degree 4`。单卡消费级**不是**官方主推路径 |
| 硬件（社区对照） | 全 bf16 常见叙述：磁盘/显存极高（社区表常写 ~80 GB 级或四卡）；实际请按你选的服务框架测 |

下载示例：

```bash
hf download MiniMaxAI/MiniMax-H3 --include "model_index.json" "FL2VA/*" "Ref2VA/*" --local-dir MiniMax-H3
```

### 3.2 官方「未开源但相关」

| 名称 | 说明 |
| --- | --- |
| H3-Context-IR | 多模态指令 → 中间表示；质量关键；仅 API |
| H3-Regenerate-2K | 768p+上下文 → 2K 再生成；仅 API |

## 4. Comfy-Org 重打包（社区默认入口）

| 字段 | 内容 |
| --- | --- |
| 名称 | Comfy-Org/MiniMax-H3 |
| 发布方 | Comfy-Org |
| 创建 | 约 2026-07-30（Hub） |
| 下载 | https://huggingface.co/Comfy-Org/MiniMax-H3 |
| 文档 | https://docs.comfy.org/tutorials/video/minimax/minimax-h3 |
| 工作流 | T2V / I2V / R2V JSON 模板（见 Comfy workflow_templates） |

### 4.1 扩散模型文件族（同一 Base 的不同「版本感」）

对 **FL2VA** 与 **Ref2VA** 各有一套：

| 文件后缀 | 含义 | 优势 | 注意 |
| --- | --- | --- | --- |
| `*_bf16.safetensors` | 接近原精度单文件 | 质量参考上限 | 体积/显存最大 |
| `*_int8_convrot.safetensors` | INT8 + ConvRot | 质量与速度折中；Comfy 推荐在 **PyTorch+cu130** 时优先 | 非剪枝版仍偏大 |
| `*_pruned_bf16` / `*_pruned_int8_convrot` | AdaLN 等可缓存部分预计算/剪枝思路（约小 ~40% 量级，社区常用说法） | **消费级默认首选之一** | 纯推理友好；微调场景要谨慎 |
| `*_pruned_fp8_scaled` | FP8 | 无法用 int8_convrot 时的备选 | Comfy-Org：**仅当不能用 int8_convrot 再用** |

### 4.2 文本编码器 / VAE / 附加

| 组件 | 典型文件 | 说明 |
| --- | --- | --- |
| TE BF16 / INT8 / NVFP4-AWQ | `qwen3vl_32b_minimax_h3_*.safetensors` | NVFP4-AWQ **不强制** Blackwell（卡页声明） |
| Video VAE | `minimax_h3_video_vae_fp16` | 社区强调音频 VAE 保持 fp32 更稳 |
| Audio VAE | `minimax_h3_audio_vae_fp32` | 用 fp16 易音画不同步（社区共识） |
| Turbo LoRA（仓内） | `minimax_h3_*_turbo_*_comfyui_bf16` | 来自 lightx2v 等 |
| Fun ControlNet | `minimax_h3_fun_controlnet_union_pruned_*` | 对应 PAI 控制分支的 Comfy 形态 |
| Embeddings | `minimaxh3_*.safetensors` | 提示里 `embedding:文件名` |

**硬件（社区汇总，非官方承诺）**

| 配置 | 磁盘量级 | 常见 VRAM 叙述 |
| --- | --- | --- |
| pruned INT8 + NVFP4 TE | ~42.5 GB | ~24 GB；12 GB + 大内存 offload 有人能跑 |
| 非剪枝 int8_convrot | ~67 GB | ~48 GB 档 |
| 全 bf16 | ~123 GB+ | 高端 / 多卡 |

## 5. 量化与低显存线

### 5.1 GGUF 主线

| 发行 | 发布方 | 链接 | 要点 |
| --- | --- | --- | --- |
| MiniMax-H3-GGUF | Abiray | https://huggingface.co/Abiray/MiniMax-H3-GGUF | FL2VA/Ref2VA 各 Q3–Q8；附 TE/VAE；UNet 约 15.6–36 GB |
| MiniMax-H3-Pruned-GGUF | Abiray | https://huggingface.co/Abiray/MiniMax-H3-Pruned-GGUF | 剪枝后约 8.9–21.6 GB |
| MiniMax-H3-GGUF | Unsloth | https://huggingface.co/unsloth/MiniMax-H3-GGUF | 高下载；偏 sd.cpp / 工具链文档 |
| MiniMax-H3_GGUFs | realrebelai | https://huggingface.co/realrebelai/MiniMax-H3_GGUFs | 基于 Comfy-Org 再量化 |
| MiniMax-H3-GGUF | molbal / leejet 等 | 各 HF 仓 | 多源；下载前核 sha / 卡页 |

**GGUF 硬件经验档（社区表）**

| Quant | UNet 约 | 常见目标卡 |
| --- | --- | --- |
| Q3_K_* | ~15.6 GB | 12 GB 档 |
| Q4_K_M | ~19.9 GB | 16 GB 档 |
| Q5_K_M | ~23.9 GB | 24 GB 档 |

需 ComfyUI-GGUF（或作者指定 fork）等节点；**不是**官方 SGLang 路径。

### 5.2 INT8 / INT4 / NVFP4 / W4A8

| 发行 | 链接 | 特点 |
| --- | --- | --- |
| Comfy-Org int8_convrot / pruned | 见 §4 | 主流推荐 |
| Abiray nvfp4-INT4-INT8-Convrot | https://huggingface.co/Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot | 低比特全家桶 |
| AX1Y2JP W4A8-ConvRot | https://huggingface.co/AX1Y2JP/MiniMax-H3-W4A8-ConvRot | 权重 4bit / 激活 8bit 向 |
| koongrizzly INT4 W4A8 pruned | https://huggingface.co/koongrizzly/MiniMax_H3_int4_W4A8_ConvRot_Pruned | 更极端低显存 |
| rockerBOO / lilcheaty NVFP4 | 见总表 | Blackwell 友好；双重量化有误差累积风险（lilcheaty 自述） |

**社区低显存极限（报告，风险自负）**

| 档位 | 常见配方叙事 | 备注 |
| --- | --- | --- |
| 24 GB | pruned INT8 + NVFP4 TE 或 Q5 GGUF | 消费级甜区 |
| 16 GB | Q4 GGUF 或 pruned INT8 + CUDA 13 | 4080/5080 常见 |
| 12 GB | pruned INT8 + NVFP4 TE + 64 GB 内存 + Turbo | 强烈依赖系统内存 offload |
| 8 GB | INT4/INT8 + 大内存 + 降分辨率/帧数 | 可用但慢 |
| 6 GB | INT4 ConvRot + Turbo；≤~0.4 MP | 有笔记本过热/硬件故障报告，不建议长时间满载 |

## 6. 加速：Turbo / Acc LoRA

| 发行 | 发布方 | 链接 | 步数/形态 | 优势 | 代价 |
| --- | --- | --- | --- | --- | --- |
| Minimax-h3-Turbo | lightx2v | https://huggingface.co/lightx2v/Minimax-h3-Turbo | 4-step / 8-step 等 | 社区测可达约 **3.4×**；Studio/API 可选 | 音质/口音/硬切易劣化；草稿友好 |
| MiniMax-H3-Turbo-Lora | larryvrh | https://huggingface.co/larryvrh/MiniMax-H3-Turbo-Lora | 少步 LoRA | Comfy 常用 | 需正确 alpha/strength、节点 |
| Turbo-Lora-ComfyUI | drbaph | https://huggingface.co/drbaph/MiniMax-H3-Turbo-Lora-ComfyUI | 多种 pruned/动态秩 | 面向 Comfy 打包 | 版本多，别混用错文件 |
| Acc-LoRAs | alibaba-pai | https://huggingface.co/alibaba-pai/MiniMax-H3-Acc-LoRAs | 加速 LoRA | 与 VideoX-Fun / 论文线相关 | 按卡页接入 |
| Turbo-GGUF（合并） | molbal 等 | https://huggingface.co/molbal/MiniMax-H3-Turbo-GGUF | 4-step 合并权重 | 免 LoRA 加载 | 仍需 Turbo sampler |

实践建议（社区收敛）：**Turbo 出草稿 → 同种子关 Turbo 出成片**；音频敏感镜头少用 4-step。

## 7. 控制与扩展

| 发行 | 发布方 | 链接 | 能做什么 |
| --- | --- | --- | --- |
| Fun-Controlnet-Union | alibaba-pai | https://huggingface.co/alibaba-pai/MiniMax-H3-Fun-Controlnet-Union | 单一权重：Canny/Depth/HED/MLSD/Pose + inpaint；挂 5 个 transformer block；`guidance_scale=1.0` |
| Kijai controlnet 再分发 | Kijai | https://huggingface.co/Kijai/MiniMax-H3-experimental | Comfy 友好 pruned bf16/int8 控制文件 |
| 风格/题材 LoRA | fal、社区等 | 如 Realism-People、spatial-physics… | 在 Base 上叠风格；HF 上 adapters 数量持续增长 |
| 融合/实验合并 | MATLOWAI、xmarre、joeygambino 等 | 各仓 | Turbo+量化合并、Ref delta fuse、跨模型实验 | 实验性，质量自负 |

ControlNet 内存：PAI 卡页写明 Transformer(~62 GB)+TE(~62 GB) 难以整装进单卡 80 GB，需 **offload / qfloat8** 策略。

## 8. 硬件总表（把「版本」映射到机器）

> 综合：官方 SGLang 示例 + [awesome-minimax-H3 performance 指南](https://github.com/wildminder/awesome-minimax-H3/blob/main/guides/minimax-h3-performance.md)（更新标注 2026-08-16）+ 各 model card。**全部为范围值。**

| 硬件档 | 推荐版本组合 | 最低可玩（社区） |
| --- | --- | --- |
| 多卡数据中心（官方路径） | MiniMaxAI BF16 + SGLang/vLLM | 按框架文档 |
| 24 GB（4090/3090/5090） | Comfy pruned INT8 + NVFP4 TE；或 Q5 GGUF；可选 Turbo 4-step | 同左降分辨率 |
| 16 GB（4080/5080） | Q4 GGUF 或 pruned INT8；CUDA 13 收益大 | Turbo + 降像素 |
| 12 GB | pruned INT8 + NVFP4 TE + **64 GB RAM** + Turbo/EasyCache | 32 GB RAM 勉强 |
| 8 GB | INT4/INT8 + ≥32 GB RAM + 短片段 | NF4 等路线见社区教程 |
| 6 GB | INT4 ConvRot + Turbo + 极低分辨率 | 不推荐生产力用途 |
| Apple Silicon 16 GB+ | MLX / VPIPE 社区项目（非官方主路径） | 很慢但可出片 |
| DGX Spark 等 | INT8 + Sol Engine 等加速运行时 | 运行时≠权重版本 |

**运行时加速（不是权重版本，但选型常一起看）**

- NVIDIA **Sol Engine**（on-device 加速笔记）：https://nvlabs.github.io/Sana/Sol-Engine/H3-OnDevice/  
- 社区：sol-attn（无损）、SageAttention、EasyCache、Spectrum（有损）等

## 9. 快速读懂「某一版」的检查清单

打开任意 HF/ModelScope 卡页时，按这个顺序扫：

1. **Base 关系**：`base_model: MiniMaxAI/MiniMax-H3` 还是基于 Comfy-Org？  
2. **任务**：只 FL2VA、只 Ref2VA，还是两者？  
3. **形态**：全量分片 / Comfy 单文件 / GGUF / LoRA / ControlNet / Merge？  
4. **精度**：bf16、int8_convrot、pruned、fp8、nvfp4、Q3–Q8…  
5. **依赖节点**：是否要 ComfyUI-GGUF、Turbo loader、Kitchen attention？  
6. **VRAM + 系统内存** 是否写明？没有就按 §8 档位估。  
7. **许可**：Community License vs Apache；是否允许你的商用/地区。  
8. **音频**：是否提醒 Audio VAE fp32、Turbo 伤音质。  
9. **更新日期** 与 issue：量化是否双重量化、是否仅 Blackwell。

## 10. 资料与维护

### 一手

- https://www.minimax.io/news/minimax-h3-open-source  
- https://huggingface.co/MiniMaxAI/MiniMax-H3  
- https://www.modelscope.cn/models/MiniMax/MiniMax-H3  
- https://github.com/MiniMax-AI/MiniMax-H3  
- https://design.minimax.io/h3  

### 社区索引（二次整理，请回跳一手）

- https://huggingface.co/Comfy-Org/MiniMax-H3  
- https://github.com/wildminder/awesome-minimax-H3  
- https://comfyui-wiki.com/en/models/minimax  
- Hub 搜索：`MiniMax-H3`（adapters/quantized 持续增加）

### 本文件维护约定

- 新增发行：补总表一行 + 一小节；必须带 URL。  
- 不确定的日期/VRAM 写「未核实」或「社区报告」。  
- NSFW 或违规向权重不收录细表（Hub 上存在 adapters，自行检索）。  
- 发现失效链接请 PR。

---

*本手册服务 [minimax-h3-analysis](https://github.com/maodou0512/minimax-h3-analysis) 分析项目，不替代各作者 model card。*


## 11. 二次扩写：补充发行详表

以下条目在首版总表之外补全，便于「按名字搜到就能读懂」。

### multimodalart/MiniMax-H3-Pruned

| 字段 | 内容 |
| --- | --- |
| 下载 | https://huggingface.co/multimodalart/MiniMax-H3-Pruned |
| 发布 | multimodalart · 约 2026-08-09 |
| 特点 | AdaLN 剪枝的 **diffusers** 形态；DiT 分区约 66.28→40.24 GB（参数约 33.14B→20.11B）；TE 截断层 51–63；VAE 仍指向官方 |
| 优势 | 与 Comfy 剪枝 LoRA 坐标系兼容；适合 ModularPipeline |
| 硬件 | 作者 H100 offload 示例峰值约 52.7 GB（pruned）vs 65.2 GB（released）——仅该配置 |
| 注意 | 数值近似重构，非 bit-identical；常需 `trust_remote_code=True` |

### DiffSynth-Studio/MiniMax-H3-NF4

| 字段 | 内容 |
| --- | --- |
| 下载 | https://huggingface.co/DiffSynth-Studio/MiniMax-H3-NF4 |
| 发布 | DiffSynth-Studio · 约 2026-08-04 |
| 特点 | `bitsandbytes` **NF4**；含 fl2va/ref2va 与 pruned-nf4；TE/VAE 亦有 NF4；支持 LoRA 训练 |
| 优势 | 面向 DiffSynth/Python 的极低显存路径 |
| 硬件 | 作者宣称磁盘 offload 可至约 **8 GB** VRAM；训练示例涉及 H20≈48GB / 4090≈24GB |
| 注意 | processor 等仍可能取自官方仓 |

### unsloth/MiniMax-H3-FP8 与 GGUF 补充

| 发行 | 链接 | 要点 |
| --- | --- | --- |
| unsloth GGUF | https://huggingface.co/unsloth/MiniMax-H3-GGUF | pruned Q2–Q8；建议 TE 放 CPU；VAE 取 Comfy-Org |
| unsloth FP8/INT8 | https://huggingface.co/unsloth/MiniMax-H3-FP8 | `.pt` INT8 / INT8-ConvRot / FP8；源为 Comfy pruned_bf16；**不适用于** sd.cpp |
| molbal GGUF | https://huggingface.co/molbal/MiniMax-H3-GGUF | Q8_CR/U16G 等需作者指定 ComfyUI-GGUF 节点；U16G 面向约 16GB |

### coolthor / ModelsLab / rockerBOO NVFP4 族

| 发行 | 链接 | 要点 |
| --- | --- | --- |
| coolthor pruned-NVFP4 | https://huggingface.co/coolthor/MiniMax-H3-pruned-NVFP4 | FL2VA+Ref2VA；可能 gated；5090 峰值约 26.9 GiB（作者） |
| ModelsLab ref2va-NVFP4 | https://huggingface.co/ModelsLab/MiniMax-H3-ref2va-NVFP4 | **未剪枝** Ref2VA NVFP4 ~38.6 GB |
| rockerBOO nvfp4-convrot | https://huggingface.co/rockerBOO/minimax-h3-nvfp4-convrot | 文档较全；推荐 pruned_nvfp4_convrot_int8 等组合 |
| lilcheaty NVFP4 | https://huggingface.co/lilcheaty/MiniMax-H3-NVFP4 | **仅 Ref2VA**；双重量化有误差累积自述 |

**Blackwell 提示**：NVFP4 在 50 系上原生；Ada/Hopper 上多为仿真，优先 INT8 ConvRot。

### Ar4ikov W4A16-RTN

| 字段 | 内容 |
| --- | --- |
| 下载 | https://huggingface.co/Ar4ikov/MiniMax-H3-transformer-W4A16-RTN |
| 特点 | 仅量化 transformer（AutoRound W4A16 RTN）；AdaLN 保持 BF16；约 66→38 GB |
| 注意 | 作者未提供完整与 BF16 的视频质量对比 |

### FastVideo FastH3（4-step Preview）

| 字段 | 内容 |
| --- | --- |
| 下载 | https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree |
| 发布 | FastVideo · 约 2026-08-27 |
| 特点 | 4-step DMD2 + VSA 稀疏；**仅 T2VA** 的蒸馏学生；preview |
| 硬件 | 公开示例偏多卡服务；不要默认当成 单卡消费级替换 Base |
| 许可 | 继承 H3 Community License（以卡页为准） |

### 运行时与门户（再次强调）

| 名称 | 链接 | 角色 |
| --- | --- | --- |
| SGLang cookbook | https://docs.sglang.io/cookbook/diffusion/MiniMax/MiniMax-H3 | 官方服务配方（含 ModelScope、量化、Turbo、FastH3 等） |
| vLLM recipes | https://recipes.vllm.ai/MiniMaxAI/MiniMax-H3 | 视频 API / 双 DiT 等 |
| Wan2GP | https://github.com/deepbeepmeep/Wan2GP | 低 VRAM 启动器与剪枝脚本 |
| design.minimax.io/h3 | https://design.minimax.io/h3 | 官方开放生态与 FAQ |
| cybermotaz Qwen3-VL NVFP4 | https://huggingface.co/cybermotaz/Qwen3-VL-32B-Instruct-NVFP4 | Comfy `nvfp4_awq` TE 上游之一 |
| Sol Engine | https://nvlabs.github.io/Sana/Sol-Engine/H3-OnDevice/ | 不改权重的推理加速 |

### 选用补丁（更新）

| 目标 | 优先 |
| --- | --- |
| Diffusers 剪枝 | multimodalart Pruned |
| 极低显存 Python | DiffSynth NF4 / WanGP |
| sd.cpp / Unsloth GGUF | unsloth MiniMax-H3-GGUF |
| 仅要更快的 T2VA 学生模型 | FastH3 Preview（接受质量上限） |
| Blackwell 再压 DiT | coolthor / lilcheaty / rockerBOO |

