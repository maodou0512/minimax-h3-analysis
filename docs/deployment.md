# 部署与工作流

## 两条验证路径（官方）

1. **仅本地 H3-Base** → 验证 **768p** 音视频。  
2. **Full 2K Workflow** → 本地 Base + 官方 **Context-IR** + **Regenerate-2K** API，对齐平台直出 2K 质量。

## 权重获取

```bash
# 两个任务族
hf download MiniMaxAI/MiniMax-H3 --include "FL2VA/*" "Ref2VA/*" --local-dir MiniMax-H3

# 或只拉一个
hf download MiniMaxAI/MiniMax-H3 --include "FL2VA/*" --local-dir MiniMax-H3
```

diffusers 用户可按文档用 `ModularPipeline.from_pretrained("MiniMaxAI/MiniMax-H3")` 按需拉取组件（以当前 diffusers 文档为准）。

## 推荐推理栈

| 场景 | 常见选择 |
| --- | --- |
| 服务器多卡 | SGLang、vLLM（及 Omni 相关配方） |
| Python 可编程流水线 | diffusers / DiffSynth 等 |
| 个人工作站可视化 | ComfyUI（官方提到 day-0 模板） |
| 低显存探索 | 社区量化/裁剪包（如 Comfy 生态 INT8 等，**以社区卡页为准**） |

### SGLang 示例

FL2VA：

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

Ref2VA：将 `--model-variant` 改为 `ref2va`，端口可改为 `30011`。  
具体参数以 [MiniMax-H3 deployment guide / cookbook](https://www.minimax.io/news/minimax-h3-open-source) 为准。

## Full 2K 环境变量（概念）

```bash
SGLANG_DEPLOYMENT_URL="<your-sglang-url>"
# 中国区
MINIMAX_API_BASE="https://api.minimaxi.com"
# 国际区示例
# MINIMAX_API_BASE="https://api.minimax.io"
TOKEN="<minimax-token>"
```

相关 API（名称以平台文档为准）：

- Create H3-2K / video-generation-v2-create  
- H3-Context-IR  
- H3-Regenerate-2K / regeneration  

官方 case 脚本覆盖 T2VA、I2VA（首帧）、Ref2VA，并提供 API 直出的 768p/2K 参考结果便于对齐。

## 硬件与加速（二手线索）

NVIDIA SANA 团队公开过在 DGX Spark / RTX 5090 上用 **Sol Engine** 加速 MiniMax-H3 的笔记（推理侧加速，非改权重）。若你做性能对比，请写明：分辨率、步数、帧数、是否官方参考实现、加速器版本。  
参见：<https://nvlabs.github.io/Sana/Sol-Engine/H3-OnDevice/>

## 安全实践

- 勿把 `TOKEN` 提交进本仓库。  
- 生产环境优先用可访问 URL 传 `base_video`，而不是长期依赖超大 Base64。  
- 遵守 Community License 的地域与用途限制。
