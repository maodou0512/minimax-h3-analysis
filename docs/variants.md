# 模型变体：FL2VA 与 Ref2VA

来源：[MiniMax H3 开源公告](https://www.minimax.io/news/minimax-h3-open-source)。

H3-Base 以两个**任务专用** checkpoint 发布，各自包含专用 Omni Transformer 以及 processor、tokenizer、text encoder、Visual VAE、Audio VAE 等组件。

## 对照表

| | **FL2VA** | **Ref2VA** |
| --- | --- | --- |
| 全称含义 | First-and-Last-Frame → Video-Audio | Reference → Video-Audio |
| 支持任务 | `t2va`、`fl2va`（含首/末/首末帧） | `ref2va` 全参考生成 |
| 图像 | 0 / 1 / 2 张（无图=纯 T2V；一图=首或末；两图=首末） | ≤ **9** 张 |
| 视频参考 | — | ≤ **3** 段；每段 2–15s；总时长 ≤ 15s |
| 音频参考 | — | ≤ **3** 段；须伴随图像或视频，**不能单独作为唯一输入**；每段 2–15s；总时长 ≤ 15s |
| 混合输入 | 文本 + 可选首末帧 | 全类型文件总数 ≤ **12** |
| 输出 | 视频 + 音频 | 视频 + 音频 |
| 精度（公告） | BF16 | BF16 |

## FL2VA 使用直觉

- **纯文本**：叙事/镜头语言写清楚，依赖 Context-IR 或自建提示工程补全声画细节。  
- **单图**：锁定开场或收束画面，适合「从这张海报动起来」或「落到这张定妆」。  
- **双图**：强约束起止构图，适合转场与镜头匹配实验。

## Ref2VA 使用直觉

适合角色一致性、运动参考、素材续写、声线参考、视频编辑类指令。公告中的 Ref2VA 示例工作流包含：主体定义、源视频编辑、背景乐部分复用、对白音色参考等结构化字段（常由 Context-IR 生成）。

## 仓库布局（概念）

```
<TASK>/          # FL2VA 或 Ref2VA
├── model_index.json
├── processor/
├── tokenizer/
├── text_encoder/
├── transformer/
├── visual_vae/
└── audio_vae/
```

Hugging Face 仓库中「原始 checkpoint」与 diffusers 格式可能并列；按框架只下载需要的子集，避免整库误拉。

## 选型建议（实践）

| 你的目标 | 更可能选 |
| --- | --- |
| 文生视频、简单首帧驱动 | FL2VA |
| 多参考一致、剪辑式改造、音色/运动锚定 | Ref2VA |
| 只要官方观感的 2K | Base（本地或 API）+ **Regenerate-2K API** |
