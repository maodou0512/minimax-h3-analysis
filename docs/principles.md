# MiniMax H3 原理知识

> 本页是仓库的**原理知识板块**：用可核对的公开材料，把 H3「为什么这样设计、关键机制做什么」讲清楚。  
> 与 [`architecture.md`](architecture.md) 的关系：本页偏**原理与设计动机**；架构页偏**模块数据流与实现细节**。  
> 维护约定：每周例行更新会复查官方博客 / 开源公告 / Tech Report（若已发布）/ Hub 卡页，有新公开知识则补进本文「知识更新日志」。  
> 首版整理：**2026-09-23**。未公开处标「未公开 / 待 Tech Report」。

## 1. 一句话抓住核心

H3 把过去按任务切开的「文生图 / 图生视频 / 参考 / 编辑 / 配音」等能力，收成**统一的多模态上下文理解 + 原生音视频同生**。语言（以及更广义的「智能结构」）被当作打通任务边界的桥梁；系统上再配 **Contextual Omni Representation（公开叙述）/ Context-IR（产品模块）**、**H3-VAE**、**H3-Omni Transformer**，以及用 **In-Context Regeneration** 做 2K，而不是单独训一个传统超分头。

## 2. 设计第一性：打破任务与模态边界

官方研究博客（2026-07-31）明确：前代 Hailuo 01/02 之后，H3 的第一原则是 **unify and generalize across tasks（跨任务统一与泛化）**。

过去常见的割裂包括：

| 领域 | 典型割裂 |
| --- | --- |
| 图像 | T2I、编辑、主体参考、运动参考、风格参考分属不同专家模型 |
| 音频 | 人声、音效、音乐分域研究 |
| 视频 | T2V、I2V、首末帧、主体/运动/音色参考、视频编辑彼此分家，且图/视/音之间也有硬边界 |

这些边界既限制创作自由度，也限制训练期的泛化。H3 的回应是：在**预训练阶段**就尽量把多模态理解与生成能力做宽，而不是靠后期拼很多专用头。

### 2.1 预训练范式（公开摘要）

官方给出的预训练关注点（摘要）：

- **数据与任务覆盖**：T2I、T2V（音频**原生立体声**同生）、原生多镜头建模、T2A（人声/音效/音乐**不拆开**联合建模）、广义参考与编辑（图→图、图→视、音→音、音视频→音视频）。
- **「广义参考与编辑」的含义**：
  - 尽量来自真实自然数据，利于规模化；
  - 参考/编辑关系用**自然语言**表达，而不是锁死在固定任务集合里——语言是通往泛化的桥。
- **架构与训练策略**：尽早融合多样数据类型与任务；混合比例（mixing ratio）被强调为关键。

应用侧的变化：创作者越来越用自然语言描述完整创作意图，而不只是短视觉提示；模型从「生成一个片段」走向更深地参与内容生产流程。

## 3. Contextual Omni Representation / Context-IR

### 3.1 原理：用语言统一「任务」

工程上官方强调加强 **captioning（多模态描述）** 能力：

- 不再只描述目标视频，还要描述**上下文与目标的关系**，以及上下文内部元素之间的关系；
- 需要**联合描述视频与音频**，多镜头下音画关系更复杂；
- 这被表述为一种 **Contextual Omni Representation**：语言充当可泛化的桥梁与解释器，把封闭任务表改写成开放的描述形式——这是 H3 **指令遵循能力**的根。

公开博客还提到：为此建了专用模型与全模态理解流水线；多数素材约需 **100K tokens** 量级的推理，再蒸馏到平均约 **4K tokens**。这些数字以博客为准，完整算法细节 **待 Tech Report**。

### 3.2 产品模块：H3-Context-IR（托管）

开源公告中的 **H3-Context-IR** 可视为上述思想的产品化入口：

- 解析自由形式的多模态输入（指令解析、跨模态关联、时间理解、复杂逻辑）；
- 序列化为 Base 更易消费的 **Context Intermediate Representation**；
- 在不偏离用户意图的前提下可补全欠定语义。

因多阶段托管流水线，**Context-IR 未随 Base 开源**；提供 API，并鼓励社区按 Prompting Guidance 自建预处理。  
**原理含义**：本地只跑 Base 时，你等于在「跳过或自行近似」这一层表示学习；质量差距往往出在这里，而不只是采样步数。

## 4. H3-VAE：压缩、重建与可学习性

H 系列持续迭代 tokenizer。官方称 H3 **彻底重做**前代 tokenizer，在**重建质量**与**可学习性**上全面提升，带来效率竞争力；高压缩率带来约 **4× 有效序列长度收益**，显著降低训推成本，并支撑**原生 2K**相关能力叙事。

开源侧公开的实现形态（见开源公告 / model card）：

| 组件 | 公开要点 |
| --- | --- |
| **VisualVAE** | 时空因果；**f16t4d24**（空间 16×、时间 4×、24 latent 通道）；进入 Transformer 前再 `(t,h,w)` 上 `1×2×2` patchify → 视觉 token 等效约 **32×** 空间下采样 |
| **AudioVAE** | 左右声道共享编解码、分通道处理再合并；32 kHz → 约 **40 Hz** latent；受 VA-VAE 思路启发优化 latent |

**原理读法**：VAE 不只是「压小一点」，而是在**重建保真**与**生成可学**之间做折中；序列长度收益直接决定能否在可接受算力下吃下更长的音画联合上下文。

## 5. H3-Omni Transformer：为任务泛化服务的架构

### 5.1 哲学：「架构应服务于任务」

官方明确：通用与高效是唯二目标；为此**放下**曾有优势的 Hailuo-02 架构，因为在以任务泛化为中心的定义下会引入多余复杂性——「任务泛化是不可逆趋势，架构技巧应为模型定义让路」。

### 5.2 公开结构要点（开源公告）

- **~33B** 稠密单流 Transformer；约 **13B** 在 AdaLN 相关分支；AdaLN 调制可预计算缓存 → 纯推理可不加载对应参数；完整权重仍发布以便微调。
- Attention / FFN **无**按模态拆分的结构；模态专用主要在 I/O 与 AdaLN。
- **MM-RoPE**：三维多模态旋转位置编码，覆盖 `(t, h, w)`。
- 输入侧：文本经 H3-Encoder（**Qwen3-VL-32B** 第 50 层 hidden）；视觉经 Encoder + VisualVAE；音频经 AudioVAE；再 packed 成统一序列。
- 输出：联合预测视频与音频 latent，再分别解码。
- 训练后期引入 native **sparse attention**；**首发开源推理为 full attention**，稀疏实现后续单独发布。
- 发布权重为 **CFG-distilled** Omni Transformer（以卡页为准）。

### 5.3 训练系统侧（博客）

多模态上下文使序列长度方差约 **3×**；理解与生成算力更异构。官方称采用理解/生成负载分离的训练架构，并联合平衡样本内异构算力与样本间负载，端到端训练吞吐提升近 **30%**。实现细节 **待 Tech Report**。

### 5.4 与社区「剪枝」的关系

社区常见 AdaLN / curve 预计算剪枝，使消费级体积下降，是对「AdaLN 可缓存」原理的工程利用，**不等于**改写了官方任务泛化定义；数值通常非 bit-identical。

## 6. In-Context Regeneration（2K）

对 2K，官方**不用**传统独立超分模块，而是让 Base **in-context 再生成**自己的低分辨率结果：

1. 尽量复用 Base 已有生成能力；  
2. 再带上原始多模态上下文，恢复传统超分常只能「猜」的细节（如小字）。

这也被当作**任务泛化**的例子：提高分辨率被收成同一套生成先验能做的任务。  
产品模块 **H3-Regenerate-2K** 因系统复杂**尚未开源**，提供 API。  
**原理含义**：2K 质量强依赖「低分结果 + 原上下文」；只放大像素、丢掉上下文，就偏离官方路径。

## 7. 系统分层：原理如何落到「能跑什么」

```mermaid
flowchart TB
  subgraph principle [原理层]
    P1[任务/模态统一 · 语言作桥]
    P2[Contextual Omni Representation]
    P3[高效 VAE · 联合音画 latent]
    P4[单流 Omni-Transformer]
    P5[In-Context 高分辨再生成]
  end
  subgraph product [产品/开源层]
    IR[H3-Context-IR · 托管]
    BASE[H3-Base FL2VA/Ref2VA · 开源]
    R2K[H3-Regenerate-2K · 托管]
  end
  P1 --> P2 --> IR
  P3 --> BASE
  P4 --> BASE
  P5 --> R2K
  IR --> BASE --> R2K
```

| 你只部署… | 你实际在用的原理子集 |
| --- | --- |
| 仅 Base 768p | VAE + Omni-Transformer +（自建或省略的）提示/IR 近似 |
| Base + Context-IR API | 加上官方 Contextual Omni 流水线 |
| Base + IR + Regenerate-2K | 完整公开叙事的官方质量路径 |

## 8. 与 FL2VA / Ref2VA 的关系

两个 checkpoint 是**任务专用权重**，不是两套不同哲学：

- **FL2VA**：文生 / 首末帧条件，覆盖「从文本到起止画面」的主路径；  
- **Ref2VA**：多参考（图/视/音）条件，覆盖广义参考与编辑类意图。

它们共享同一套 Omni + VAE 原理；差异主要在条件接口与专用 Omni 权重。详见 [`variants.md`](variants.md)。

## 9. 读原理时的常见误区

1. **把 H3 当成「只有一个扩散 UNet」** — 实际是 Encoder + 双 VAE + Omni-Transformer 的联合系统，且音频与视频同前向。  
2. **以为开源 = 完整官方 2K 体验** — IR 与 2K 再生成仍托管。  
3. **用传统超分替代 Regenerate-2K 并声称等价** — 官方路径强调上下文再利用。  
4. **把 Turbo / FastH3 蒸馏当成「同一原理的无损加速」** — 它们是推理加速/蒸馏变体，常牺牲音质或难动作；原理上属于另一条工程权衡。  
5. **把社区量化剪枝当成架构论文结论** — 多为部署优化。

## 10. 推荐阅读顺序

1. 本页（原理地图）  
2. [`architecture.md`](architecture.md)（数据流与模块规格）  
3. [`capabilities.md`](capabilities.md)（能力边界与 Context-IR 角色）  
4. [`deployment.md`](deployment.md)（本地 vs Full 2K）  
5. [`community-versions.md`](community-versions.md)（原理落到具体权重包）  
6. 一手： [研究博客](https://www.minimax.io/blog/minimax-h3) · [开源公告](https://www.minimax.io/news/minimax-h3-open-source) · [HF 卡页](https://huggingface.co/MiniMaxAI/MiniMax-H3)

官方称将分享完整 **H3 Technical Report**；发布后应优先吸收进本页。

## 11. 待核实 / 开放问题（跟踪列表）

| 问题 | 状态 |
| --- | --- |
| Tech Report 全文与训练配方细节 | 待发布 |
| Sparse attention 开源时间表与质量差 | 未公开完整细节 |
| Context-IR 内部模型清单与 100K→4K 蒸馏精确流程 | 博客摘要级；待报告 |
| Mixing ratio、理解/生成分离训练的具体实现 | 待报告 |
| AdaLN 缓存与社区剪枝的形式化等价条件 | 社区经验为主 |
| In-context 2K 与传统超分的系统消融 | 官方定性；缺公开定量表 |

## 12. 知识更新日志

| 日期 | 变更 |
| --- | --- |
| 2026-09-23 | 初版：依据研究博客 + 开源公告 + 既有架构笔记，建立原理板块（任务泛化、Omni Representation、VAE、Omni-Transformer、In-Context Regeneration、开源边界与误区） |

<!-- 每周例行：若官方/一手有新公开知识，在此追加一行，并改正文对应小节。 -->
