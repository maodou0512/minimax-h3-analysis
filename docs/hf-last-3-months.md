# Hugging Face 近 3 个月 MiniMax H3 相关仓完整清单

> 覆盖窗口：**2026-06-11 → 2026-09-11**。
> 收录：**315** 个 HF 模型仓（Hub API 检索 + 关键词过滤）。
> `创建日` = `createdAt`；`下载量/Likes` 为抓取快照，会随时间变化。
> 选型与硬件详解见 [community-versions.md](community-versions.md)；本页追求**近 3 个月全量索引**。
> 官方开源公告日：**2026-08-03**（与部分仓 `createdAt` 早于该日不冲突——预上传常见）。

## 分类统计

| 类别 | 数量 |
| --- | ---: |
| 01-官方基座 | 1 |
| 02-Comfy官方生态重打包 | 1 |
| 03-量化与剪枝权重 | 64 |
| 04-GGUF量化 | 27 |
| 05-Turbo少步加速 | 26 |
| 06-加速LoRA-Acc | 7 |
| 07-FastH3蒸馏 | 28 |
| 08-ControlNet控制 | 5 |
| 09-风格题材LoRA | 46 |
| 10-Apple-MLX | 9 |
| 11-组件-VAE-TE-提示器 | 26 |
| 12-题材角色LoRA含NSFW | 26 |
| 13-微调合并实验 | 13 |
| 14-工作流工具箱 | 5 |
| 15-镜像转载与其它 | 31 |
| **合计** | **315** |

## 完整分表

### 01-官方基座

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-07-28 | 5080204 | 5131 | [`MiniMaxAI/MiniMax-H3`](https://huggingface.co/MiniMaxAI/MiniMax-H3) | image-text-to-video | license:other |

### 02-Comfy官方生态重打包

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-07-30 | 18813055 | 1759 | [`Comfy-Org/MiniMax-H3`](https://huggingface.co/Comfy-Org/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 03-量化与剪枝权重

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-03 | 226187 | 227 | [`Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot`](https://huggingface.co/Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot) | image-text-to-video | quantized, comfyui, int4, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 65137 | 27 | [`AX1Y2JP/MiniMax-H3-W4A8-ConvRot`](https://huggingface.co/AX1Y2JP/MiniMax-H3-W4A8-ConvRot) | diffusion-single-file | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-21 | 45202 | 27 | [`xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI`](https://huggingface.co/xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI) | image-text-to-video | comfyui, int8, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, license:other |
| 2026-08-22 | 30697 | 94 | [`joeygambino/MiniMax-H3-x-Z-Image-native`](https://huggingface.co/joeygambino/MiniMax-H3-x-Z-Image-native) | text-to-video | comfyui, comfy-native, comfy-quant, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 25476 | 28 | [`drbaph/Viggle-Animate-ComfyUI`](https://huggingface.co/drbaph/Viggle-Animate-ComfyUI) | video-to-video | comfyui, int8, license:other |
| 2026-08-09 | 23109 | 6 | [`koongrizzly/MiniMax_H3_int4_W4A8_ConvRot_Pruned`](https://huggingface.co/koongrizzly/MiniMax_H3_int4_W4A8_ConvRot_Pruned) | minimax-h3 | int4, quantization, license:apache-2.0 |
| 2026-09-04 | 21386 | 20 | [`drbaph/vdn-minimax-h3-int8-convrot-comfyui`](https://huggingface.co/drbaph/vdn-minimax-h3-int8-convrot-comfyui) | minimax-h3 | comfyui, int8, quantization, license:other |
| 2026-08-09 | 14589 | 7 | [`abakanai/Minimax_h3_hybrid`](https://huggingface.co/abakanai/Minimax_h3_hybrid) | image-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-03 | 14176 | 28 | [`rockerBOO/minimax-h3-nvfp4-convrot`](https://huggingface.co/rockerBOO/minimax-h3-nvfp4-convrot) | text-to-video | nvfp4, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 12656 | 20 | [`rzgar/minimax_h3_fl2va_fp8_e4m3fn`](https://huggingface.co/rzgar/minimax_h3_fl2va_fp8_e4m3fn) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-20 | 10269 | 3 | [`MATLOWAI/minimax-h3-nvfp4`](https://huggingface.co/MATLOWAI/minimax-h3-nvfp4) | diffusion-single-file | comfyui, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-24 | 7322 | 5 | [`hoidhxd/MiniMax-H3-x-Z-Image-hybrid`](https://huggingface.co/hoidhxd/MiniMax-H3-x-Z-Image-hybrid) | image-to-video | int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 5737 | 7 | [`berryber09/MiniMax-H3-ref2va-fl2va-hybrid-w4a8`](https://huggingface.co/berryber09/MiniMax-H3-ref2va-fl2va-hybrid-w4a8) | image-to-video | comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 3353 | 2 | [`rzgar/minimax_h3_ref2va_fp8_e4m3fn`](https://huggingface.co/rzgar/minimax_h3_ref2va_fp8_e4m3fn) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-27 | 2419 | 0 | [`fkyyy/MiniMax-H3-fp8`](https://huggingface.co/fkyyy/MiniMax-H3-fp8) | image-text-to-video | license:other |
| 2026-08-04 | 2395 | 20 | [`coolthor/MiniMax-H3-pruned-NVFP4`](https://huggingface.co/coolthor/MiniMax-H3-pruned-NVFP4) | image-text-to-video | nvfp4, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-15 | 2030 | 2 | [`joeygambino/MiniMax-H3-comfy-native-fl2va`](https://huggingface.co/joeygambino/MiniMax-H3-comfy-native-fl2va) | text-to-video | comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-05 | 1211 | 10 | [`Raretutor/vdn-minimax-h3-comfyui-int8-convrot`](https://huggingface.co/Raretutor/vdn-minimax-h3-comfyui-int8-convrot) | text-to-video | comfyui, int8, base_model:OpenVDN/vdn-minimax-h3, base_model:finetune:OpenVDN/vdn-minimax-h3, license:other |
| 2026-08-03 | 1201 | 1 | [`OzzyGT/MiniMax_H3_sdnq_dynamic_4bit`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_dynamic_4bit) | diffusers |  |
| 2026-08-11 | 867 | 1 | [`OzzyGT/MiniMax_H3_sdnq_4bit_pruned`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_4bit_pruned) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 407 | 0 | [`rockerBOO/minimax-h3-nvfp4-fp8`](https://huggingface.co/rockerBOO/minimax-h3-nvfp4-fp8) | text-to-video | nvfp4, fp8, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 407 | 0 | [`rockerBOO/minimax-h3-nvfp4`](https://huggingface.co/rockerBOO/minimax-h3-nvfp4) | text-to-video | nvfp4, fp8, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 406 | 0 | [`yuivs/Minimax-H3-nvfp4-INT4-INT8-Convrot`](https://huggingface.co/yuivs/Minimax-H3-nvfp4-INT4-INT8-Convrot) | image-text-to-video | quantized, comfyui, int4, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 374 | 0 | [`AcademiaSD/MiniMax-H3-NF4`](https://huggingface.co/AcademiaSD/MiniMax-H3-NF4) | diffusers |  |
| 2026-08-20 | 371 | 1 | [`ravibhai1212/MiniMax_H3_int4_W4A8_ConvRot_Pruned`](https://huggingface.co/ravibhai1212/MiniMax_H3_int4_W4A8_ConvRot_Pruned) | minimax-h3 | int4, quantization, license:apache-2.0 |
| 2026-09-07 | 293 | 3 | [`xtanqn/MiniMax-H3-fl2va-ref2va-b25-49-r1024-r0`](https://huggingface.co/xtanqn/MiniMax-H3-fl2va-ref2va-b25-49-r1024-r0) | minimax-h3 | fp8, license:other |
| 2026-08-03 | 239 | 2 | [`Ar4ikov/MiniMax-H3-transformer-W4A16-RTN`](https://huggingface.co/Ar4ikov/MiniMax-H3-transformer-W4A16-RTN) | image-text-to-video | int4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 233 | 0 | [`OzzyGT/MiniMax_H3_sdnq_8bit_pruned`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_8bit_pruned) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 198 | 1 | [`1ronman1993/MiniMax-H3-SVDQuant-fp4-pdd8`](https://huggingface.co/1ronman1993/MiniMax-H3-SVDQuant-fp4-pdd8) | minimax-h3 | svdquant, comfyui, license:apache-2.0 |
| 2026-08-03 | 159 | 38 | [`Merserk/MiniMax-H3-INT4-ConvRot`](https://huggingface.co/Merserk/MiniMax-H3-INT4-ConvRot) | image-text-to-video | comfyui, int4, license:other |
| 2026-09-07 | 122 | 2 | [`speach1sdef178/VDN-H3-INT8-ConvRot-ComfyUI`](https://huggingface.co/speach1sdef178/VDN-H3-INT8-ConvRot-ComfyUI) | minimax-h3 | comfyui, int8, license:other |
| 2026-08-20 | 118 | 6 | [`diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024`](https://huggingface.co/diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024) | image-text-to-video | base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-01 | 115 | 0 | [`rootonchair/MiniMax-H3-nunchaku-lite-nvfp4`](https://huggingface.co/rootonchair/MiniMax-H3-nunchaku-lite-nvfp4) | diffusers | svdquant, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 78 | 0 | [`1ronman1993/MiniMax-H3-SVDQuant-int4-pdd8`](https://huggingface.co/1ronman1993/MiniMax-H3-SVDQuant-int4-pdd8) | minimax-h3 | svdquant, comfyui, license:apache-2.0 |
| 2026-09-04 | 60 | 0 | [`aufjsufjaujda3/vdn-minimax-h3-int8-convrot-comfyui`](https://huggingface.co/aufjsufjaujda3/vdn-minimax-h3-int8-convrot-comfyui) | minimax-h3 | comfyui, int8, quantization, license:other |
| 2026-08-27 | 52 | 0 | [`Wesley1234/minimax_h3_ref2va_patchin_hf102`](https://huggingface.co/Wesley1234/minimax_h3_ref2va_patchin_hf102) | image-text-to-video | comfyui, int8-convrot, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-07 | 39 | 0 | [`cccian091/MiniMax-H3-T2V-NVFP4`](https://huggingface.co/cccian091/MiniMax-H3-T2V-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-06 | 18 | 0 | [`noctuashap/MiniMax-H3-pruned-r16`](https://huggingface.co/noctuashap/MiniMax-H3-pruned-r16) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-02 | 0 | 14 | [`Gluttony10/MiniMax-H3-INT8-CONVROT`](https://huggingface.co/Gluttony10/MiniMax-H3-INT8-CONVROT) | image-text-to-video | comfyui, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 107 | [`lilcheaty/MiniMax-H3-NVFP4`](https://huggingface.co/lilcheaty/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 7 | [`ModelsLab/MiniMax-H3-ref2va-NVFP4`](https://huggingface.co/ModelsLab/MiniMax-H3-ref2va-NVFP4) |  | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 23 | [`Winnougan/MiniMax-H3-INT4_Convrot_ComfyUI`](https://huggingface.co/Winnougan/MiniMax-H3-INT4_Convrot_ComfyUI) | image-to-video | comfyui, quantization, int4, license:apache-2.0 |
| 2026-08-03 | 0 | 38 | [`tsolful/Minimax_H3_INT4MixedConvRot`](https://huggingface.co/tsolful/Minimax_H3_INT4MixedConvRot) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 9 | [`dotexec/MiniMax-H3-T2V-NVFP4`](https://huggingface.co/dotexec/MiniMax-H3-T2V-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 32 | [`DmitryDB/MiniMax-H3-ComfyUI-Quants`](https://huggingface.co/DmitryDB/MiniMax-H3-ComfyUI-Quants) | image-text-to-video | comfyui, quantization, int8, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 0 | 9 | [`DiffSynth-Studio/MiniMax-H3-NF4`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-NF4) |  | license:apache-2.0 |
| 2026-08-05 | 0 | 2 | [`vonkaiser/MiniMax-H3-NVFP4`](https://huggingface.co/vonkaiser/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 0 | 0 | [`Rudra-ai/MiniMax-H3-NF4`](https://huggingface.co/Rudra-ai/MiniMax-H3-NF4) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-07 | 0 | 14 | [`unsloth/MiniMax-H3-FP8`](https://huggingface.co/unsloth/MiniMax-H3-FP8) | image-text-to-video | fp8, int8, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 0 | [`yitongl/minimax-h3-nvfp4-lambda-modality`](https://huggingface.co/yitongl/minimax-h3-nvfp4-lambda-modality) |  | svdquant, nvfp4, quantization, license:other |
| 2026-08-09 | 0 | 0 | [`yitongl/minimax-h3-deltaquant-nvfp4`](https://huggingface.co/yitongl/minimax-h3-deltaquant-nvfp4) |  | deltaquant, nvfp4, quantization, license:other |
| 2026-08-09 | 0 | 0 | [`Simplismart/Minimax-H3-FL2V-NVFP4`](https://huggingface.co/Simplismart/Minimax-H3-FL2V-NVFP4) |  |  |
| 2026-08-13 | 0 | 0 | [`naiwen888/MiniMax-H3-NVFP4`](https://huggingface.co/naiwen888/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 0 | 29 | [`WarmBloodAban/Minimax_h3_ref2va_XUELUO_int8_convrot`](https://huggingface.co/WarmBloodAban/Minimax_h3_ref2va_XUELUO_int8_convrot) |  |  |
| 2026-08-19 | 0 | 0 | [`ModelsLab/MiniMax-H3-svdquant-int4_r32`](https://huggingface.co/ModelsLab/MiniMax-H3-svdquant-int4_r32) | text-to-video | svdquant, int4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 0 | 0 | [`ModelsLab/MiniMax-H3-svdquant-nvfp4_r32`](https://huggingface.co/ModelsLab/MiniMax-H3-svdquant-nvfp4_r32) | text-to-video | svdquant, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 0 | 0 | [`xvmrjxc/MiniMax-H3-NVFP4`](https://huggingface.co/xvmrjxc/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 0 | 2 | [`dreamkrate/Minimax-H3-Hybrid-BF16-Pruned`](https://huggingface.co/dreamkrate/Minimax-H3-Hybrid-BF16-Pruned) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 0 | 0 | [`corechan/MiniMax-H3_NF4`](https://huggingface.co/corechan/MiniMax-H3_NF4) | text-generation | quantized, nf4, license:other |
| 2026-08-30 | 0 | 0 | [`corechan/MiniMax-H3_nvfp4`](https://huggingface.co/corechan/MiniMax-H3_nvfp4) | text-generation | quantized, nvfp4, license:other |
| 2026-09-02 | 0 | 0 | [`pottokao/H3-RotNVFP4-ComfyUI-Loader`](https://huggingface.co/pottokao/H3-RotNVFP4-ComfyUI-Loader) | minimax-h3 | comfyui, nvfp4, license:apache-2.0 |
| 2026-09-02 | 0 | 0 | [`pottokao/MiniMax-H3-NVFP4-rotated`](https://huggingface.co/pottokao/MiniMax-H3-NVFP4-rotated) | text-to-video | comfyui, nvfp4, quantization, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 0 | 0 | [`pottokao/minimax-h3-2x16gb`](https://huggingface.co/pottokao/minimax-h3-2x16gb) | text-to-video | nvfp4, quantized, license:other |
| 2026-09-10 | 0 | 1 | [`jfar-z/MiniMax-H3-FL2VA-Ref2VA-Hybrid-NVFP4`](https://huggingface.co/jfar-z/MiniMax-H3-FL2VA-Ref2VA-Hybrid-NVFP4) | image-to-video | comfyui, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 04-GGUF量化

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-03 | 952223 | 132 | [`Abiray/MiniMax-H3-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 689374 | 272 | [`unsloth/MiniMax-H3-GGUF`](https://huggingface.co/unsloth/MiniMax-H3-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-02 | 496689 | 57 | [`DeepBeepMeep/MiniMax-H3`](https://huggingface.co/DeepBeepMeep/MiniMax-H3) | diffusion-single-file | gguf |
| 2026-08-03 | 299932 | 219 | [`realrebelai/MiniMax-H3_GGUFs`](https://huggingface.co/realrebelai/MiniMax-H3_GGUFs) |  | gguf, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:unknown |
| 2026-08-04 | 264105 | 8 | [`joeygambino/MiniMax-H3-encoder-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-encoder-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3 |
| 2026-08-07 | 151172 | 61 | [`Abiray/MiniMax-H3-Pruned-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-Pruned-GGUF) | image-text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 83538 | 56 | [`molbal/MiniMax-H3-GGUF`](https://huggingface.co/molbal/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 76497 | 21 | [`leejet/MiniMax-H3-GGUF`](https://huggingface.co/leejet/MiniMax-H3-GGUF) | image-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3 |
| 2026-08-05 | 36723 | 5 | [`joeygambino/MiniMax-H3-curve-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-curve-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 25841 | 14 | [`nif0/Qwen3-VL-32B-Instruct-MiniMax-H3-GGUF`](https://huggingface.co/nif0/Qwen3-VL-32B-Instruct-MiniMax-H3-GGUF) |  | gguf, base_model:unsloth/Qwen3-VL-32B-Instruct-GGUF, base_model:quantized:unsloth/Qwen3-VL-32B-Instruct-GGUF, license:apache-2.0 |
| 2026-08-04 | 17305 | 23 | [`vantagewithai/MiniMax-H3-comfyUI-GGUF`](https://huggingface.co/vantagewithai/MiniMax-H3-comfyUI-GGUF) | image-text-to-video | gguf, license:other |
| 2026-08-04 | 11916 | 3 | [`joeygambino/MiniMax-H3-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-22 | 10245 | 29 | [`joeygambino/MiniMax-H3-x-Z-Image-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-x-Z-Image-GGUF) | text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 7747 | 1 | [`PurpleBlazey/Minimax-H3-pruned-GGUF`](https://huggingface.co/PurpleBlazey/Minimax-H3-pruned-GGUF) | image-text-to-video | gguf, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-13 | 7698 | 3 | [`hoidhxd/MiniMax-H3-Hybrid-b25-49-GGUF`](https://huggingface.co/hoidhxd/MiniMax-H3-Hybrid-b25-49-GGUF) | image-to-video | gguf, comfyui, quantized, base_model:smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models, base_model:quantized:smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models |
| 2026-08-06 | 3014 | 2 | [`woodfireind/MiniMax-H3-GGUF-MiniStack`](https://huggingface.co/woodfireind/MiniMax-H3-GGUF-MiniStack) | text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 2360 | 22 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-GGUF) | gguf | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA |
| 2026-08-16 | 1534 | 0 | [`brurpo/MiniMax-H3-NVFP4-GGUF`](https://huggingface.co/brurpo/MiniMax-H3-NVFP4-GGUF) | image-text-to-video | gguf, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 1523 | 3 | [`indhic-ai/MiniMax_H3-Prompt_Rewriter-8B-LORA-Merged-GGUF`](https://huggingface.co/indhic-ai/MiniMax_H3-Prompt_Rewriter-8B-LORA-Merged-GGUF) | image-text-to-text | gguf, lora-merge, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:merge:Qwen/Qwen3-VL-8B-Instruct, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, base_model:merge:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, license:apache-2.0 |
| 2026-08-10 | 1507 | 0 | [`MarxistLeninist/MiniMax-H3-FL2VA-Pruned-IQ1-GGUF`](https://huggingface.co/MarxistLeninist/MiniMax-H3-FL2VA-Pruned-IQ1-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 1439 | 5 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-Omni-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-Omni-GGUF) | image-text-to-text | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni |
| 2026-09-05 | 1378 | 1 | [`pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-GGUF`](https://huggingface.co/pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-GGUF) | image-text-to-text | gguf, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-07 | 1237 | 0 | [`on-nurida-mov/My-MiniMax-H3`](https://huggingface.co/on-nurida-mov/My-MiniMax-H3) | diffusion-single-file | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 1065 | 1 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-8B-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-8B-GGUF) | image-text-to-text | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B |
| 2026-08-10 | 988 | 0 | [`myhuggingbb/MiniMax-H3-GGUF`](https://huggingface.co/myhuggingbb/MiniMax-H3-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-24 | 820 | 1 | [`hoidhxd/MiniMax-H3-x-Z-Image-hybrid-GGUF`](https://huggingface.co/hoidhxd/MiniMax-H3-x-Z-Image-hybrid-GGUF) | image-to-video | gguf, base_model:hoidhxd/MiniMax-H3-x-Z-Image-hybrid, base_model:quantized:hoidhxd/MiniMax-H3-x-Z-Image-hybrid, license:apache-2.0 |
| 2026-09-08 | 277 | 0 | [`alibaybay/MiniMax-H3-Prompt-Rewriter-GGUF`](https://huggingface.co/alibaybay/MiniMax-H3-Prompt-Rewriter-GGUF) | text-generation | gguf, base_model:Qwen/Qwen2.5-Omni-7B, base_model:quantized:Qwen/Qwen2.5-Omni-7B, license:apache-2.0 |

### 05-Turbo少步加速

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-07 | 1372782 | 889 | [`lightx2v/Minimax-h3-Turbo`](https://huggingface.co/lightx2v/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-29 | 268985 | 161 | [`MATLOWAI/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/MATLOWAI/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-05 | 247074 | 955 | [`larryvrh/MiniMax-H3-Turbo-Lora`](https://huggingface.co/larryvrh/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-06 | 211372 | 409 | [`drbaph/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/drbaph/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, turbo, pruned-model, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-11 | 14621 | 16 | [`ChrisColeTech/minimax-h3-turbo-GGUF`](https://huggingface.co/ChrisColeTech/minimax-h3-turbo-GGUF) | text-to-video | gguf, quantized, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 13964 | 49 | [`Abiray/MiniMax-H3-Turbo-Lora-Pruned-ComfyUI`](https://huggingface.co/Abiray/MiniMax-H3-Turbo-Lora-Pruned-ComfyUI) | image-text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-15 | 13760 | 9 | [`PulpCut/MiniMax-H3-Ref2VA-Turbo-INT8-ConvRot`](https://huggingface.co/PulpCut/MiniMax-H3-Ref2VA-Turbo-INT8-ConvRot) | minimax-h3 | int8, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 4490 | 12 | [`infosave/MiniMax-H3-Turbo-cmf`](https://huggingface.co/infosave/MiniMax-H3-Turbo-cmf) | text-to-video | base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-13 | 3185 | 1 | [`molbal/MiniMax-H3-Turbo-GGUF`](https://huggingface.co/molbal/MiniMax-H3-Turbo-GGUF) | image-to-video | gguf, comfyui, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-13 | 2183 | 4 | [`PulpCut/MiniMax-H3-Turbo-INT8-ConvRot`](https://huggingface.co/PulpCut/MiniMax-H3-Turbo-INT8-ConvRot) | minimax-h3 | int8, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 1609 | 0 | [`e5ey/MiniMax-H3-Turbo-Lora-Pruned-Fixed`](https://huggingface.co/e5ey/MiniMax-H3-Turbo-Lora-Pruned-Fixed) | text-to-video | turbo, lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-25 | 1408 | 1 | [`Rkss/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_native`](https://huggingface.co/Rkss/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_native) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-06 | 1403 | 6 | [`InstantX/MiniMax-H3-Turbo-Lora-Diffusers`](https://huggingface.co/InstantX/MiniMax-H3-Turbo-Lora-Diffusers) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-18 | 1014 | 0 | [`DARK-MING/MiniMax-H3-Turbo-Lora`](https://huggingface.co/DARK-MING/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-08 | 530 | 0 | [`Jackxuanxuan/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/Jackxuanxuan/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-09-08 | 393 | 0 | [`chfm/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/chfm/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-30 | 103 | 0 | [`HAOOOOOOO51/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_pruned`](https://huggingface.co/HAOOOOOOO51/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_pruned) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-05 | 44 | 0 | [`EllipsesMark/larryvrh-Turbo-Lora`](https://huggingface.co/EllipsesMark/larryvrh-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-05 | 33 | 0 | [`pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-SVDQuant-vLLM-Omni`](https://huggingface.co/pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-SVDQuant-vLLM-Omni) | image-to-video | turbo, nvfp4, svdquant, license:apache-2.0 |
| 2026-09-07 | 11 | 0 | [`Drakonff1/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/Drakonff1/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, turbo, pruned-model, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-06 | 0 | 60 | [`t8star/minimax-h3-4step-turbo-loras-comfyui-exp`](https://huggingface.co/t8star/minimax-h3-4step-turbo-loras-comfyui-exp) |  |  |
| 2026-08-06 | 0 | 14 | [`Mamad8/MiniMaxH3_R2V-PDD-Turbo-LoRA-Mamad8`](https://huggingface.co/Mamad8/MiniMaxH3_R2V-PDD-Turbo-LoRA-Mamad8) |  |  |
| 2026-08-10 | 0 | 65 | [`joyfox/MiniMax-H3-Turbo`](https://huggingface.co/joyfox/MiniMax-H3-Turbo) | image-to-video | comfyui, lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-08-20 | 0 | 105 | [`lightx2v/Minimax-h3-Turbo-SLA`](https://huggingface.co/lightx2v/Minimax-h3-Turbo-SLA) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-04 | 0 | 0 | [`NaukNauk/minimax-h3-turbo-ref2va-merged`](https://huggingface.co/NaukNauk/minimax-h3-turbo-ref2va-merged) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 0 | 0 | [`pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-rotated-T1`](https://huggingface.co/pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-rotated-T1) | image-to-video | comfyui, turbo, nvfp4, license:apache-2.0 |

### 06-加速LoRA-Acc

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-26 | 73676 | 221 | [`alibaba-pai/MiniMax-H3-Acc-LoRAs`](https://huggingface.co/alibaba-pai/MiniMax-H3-Acc-LoRAs) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 36028 | 65 | [`aptech0081/MiniMax-H3-Acc-LoRAs-ComfyUI`](https://huggingface.co/aptech0081/MiniMax-H3-Acc-LoRAs-ComfyUI) | text-to-video | comfyui, lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-29 | 31998 | 8 | [`t8star/Minimax-H3-Super-Acceleration-Comfy`](https://huggingface.co/t8star/Minimax-H3-Super-Acceleration-Comfy) | minimax-h3 | comfyui |
| 2026-08-29 | 7334 | 5 | [`fbjr/MiniMax-H3-Acc-LoRAs-sidecar`](https://huggingface.co/fbjr/MiniMax-H3-Acc-LoRAs-sidecar) | text-to-video | comfyui, lora, base_model:alibaba-pai/MiniMax-H3-Acc-LoRAs, base_model:adapter:alibaba-pai/MiniMax-H3-Acc-LoRAs, license:other |
| 2026-08-31 | 32 | 0 | [`taurusduan/Minimax-H3-Super-Acceleration-Comfy`](https://huggingface.co/taurusduan/Minimax-H3-Super-Acceleration-Comfy) | minimax-h3 | comfyui |
| 2026-08-26 | 0 | 4 | [`t8star/MiniMax-H3-Acc-8Step-comfy`](https://huggingface.co/t8star/MiniMax-H3-Acc-8Step-comfy) |  |  |
| 2026-08-27 | 0 | 1 | [`Wesley1234/MiniMax-H3-Acc-8Step-comfy`](https://huggingface.co/Wesley1234/MiniMax-H3-Acc-8Step-comfy) |  |  |

### 07-FastH3蒸馏

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-27 | 221472 | 298 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 21931 | 18 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-LoRA`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-LoRA) | minimax-h3 | lora, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 11953 | 13 | [`barelymining/ComfyUI-MiniMax-H3-FastVideo`](https://huggingface.co/barelymining/ComfyUI-MiniMax-H3-FastVideo) | diffusers | comfyui, lora, fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:adapter:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-08-23 | 7657 | 7 | [`drozbay/MiniMax-H3-FastH3-Preview-LoRA`](https://huggingface.co/drozbay/MiniMax-H3-FastH3-Preview-LoRA) | minimax-h3 | lora, comfyui, base_model:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, base_model:adapter:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, license:other |
| 2026-09-05 | 4990 | 0 | [`zhurrka/FastVideo-FastH3-4-step-Preview-v1-LoRA`](https://huggingface.co/zhurrka/FastVideo-FastH3-4-step-Preview-v1-LoRA) | minimax-h3 | lora, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 1888 | 18 | [`realrebelai/FastH3_GGUFs`](https://huggingface.co/realrebelai/FastH3_GGUFs) | image-to-video | gguf, quantized, comfyui, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:quantized:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-08-23 | 1633 | 27 | [`FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2`](https://huggingface.co/FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 479 | 1 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-29 | 326 | 0 | [`Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-Q8`](https://huggingface.co/Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-Q8) | text-to-video | mlx, license:other |
| 2026-09-02 | 270 | 1 | [`vantagewithai/FastVideo-FastH3-4-step-VSA-DataFree-ComfyUI-GGUF`](https://huggingface.co/vantagewithai/FastVideo-FastH3-4-step-VSA-DataFree-ComfyUI-GGUF) | text-to-video | gguf, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-29 | 249 | 1 | [`Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-BF16`](https://huggingface.co/Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-BF16) | text-to-video | mlx, fasth3, license:other |
| 2026-09-07 | 244 | 2 | [`zerubroberts/MiniMax-H3-FastH3-v1-dense-datafree-ComfyUI`](https://huggingface.co/zerubroberts/MiniMax-H3-FastH3-v1-dense-datafree-ComfyUI) | minimax-h3 | lora, comfyui, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 93 | 0 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1900`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1900) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 60 | 1 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1300`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1300) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 42 | 3 | [`FastVideo/FastVideo-Minimax-FastH3-Preview-v0.1`](https://huggingface.co/FastVideo/FastVideo-Minimax-FastH3-Preview-v0.1) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 35 | 0 | [`KyleNeverGivesUp/FastH3-Preview-v0.2-r16`](https://huggingface.co/KyleNeverGivesUp/FastH3-Preview-v0.2-r16) | text-to-video | fasth3, base_model:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, base_model:finetune:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, license:other |
| 2026-08-28 | 0 | 0 | [`TechnoBaptist/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree`](https://huggingface.co/TechnoBaptist/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-29 | 0 | 2 | [`KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16`](https://huggingface.co/KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16) | text-to-video | fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-08-30 | 0 | 5 | [`PulpCut/FastH3-VSA-INT8-ConvRot`](https://huggingface.co/PulpCut/FastH3-VSA-INT8-ConvRot) | text-to-video | int8, fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-01 | 0 | 2 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT8`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT8) | text-to-video | mlx, fasth3, quantized, int8, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-01 | 0 | 0 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT6`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT6) | text-to-video | mlx, fasth3, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-01 | 0 | 3 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4) | text-to-video | mlx, fasth3, quantized, int4, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-01 | 0 | 0 | [`MaximMerk/fasth3-v0.2-int8-convrot`](https://huggingface.co/MaximMerk/fasth3-v0.2-int8-convrot) |  |  |
| 2026-09-01 | 0 | 1 | [`kevin-mi/FastH3-4step-Preview-overlay`](https://huggingface.co/kevin-mi/FastH3-4step-Preview-overlay) | sglang-diffusion | fasth3 |
| 2026-09-02 | 0 | 1 | [`LoboForge/minimax-h3-fastvideo-nvfp4`](https://huggingface.co/LoboForge/minimax-h3-fastvideo-nvfp4) | text-to-video | comfyui, fasth3, nvfp4, quantization, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-02 | 0 | 0 | [`MrMofer/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4`](https://huggingface.co/MrMofer/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4) | text-to-video | mlx, fasth3, quantized, int4, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-02 | 0 | 4 | [`pottokao/MiniMax-H3-FastH3-NVFP4-rotated`](https://huggingface.co/pottokao/MiniMax-H3-FastH3-NVFP4-rotated) | text-to-video | comfyui, nvfp4, quantization, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 0 | 1 | [`lpiao3825/FastH3-ComfyUI-Community-Workflow`](https://huggingface.co/lpiao3825/FastH3-ComfyUI-Community-Workflow) |  |  |

### 08-ControlNet控制

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-24 | 9610 | 174 | [`alibaba-pai/MiniMax-H3-Fun-Controlnet-Union`](https://huggingface.co/alibaba-pai/MiniMax-H3-Fun-Controlnet-Union) | text-to-video | controlnet, license:other |
| 2026-08-24 | 62 | 0 | [`TechnoBaptist/MiniMax-H3-Fun-Controlnet-Union`](https://huggingface.co/TechnoBaptist/MiniMax-H3-Fun-Controlnet-Union) | text-to-video | controlnet, license:other |
| 2026-08-06 | 0 | 112 | [`javawock7618/comfy-MiniMax-H3-workflows`](https://huggingface.co/javawock7618/comfy-MiniMax-H3-workflows) | image-to-video | comfyui, controlnet, controlnet-union, int8, turbo-lora, quantization |
| 2026-08-24 | 0 | 0 | [`GJuarez67/MiniMax-H3-Fun-Controlnet-Union-Demo`](https://huggingface.co/GJuarez67/MiniMax-H3-Fun-Controlnet-Union-Demo) | video-to-video | controlnet |
| 2026-09-10 | 0 | 0 | [`berryber09/MiniMax-H3-Fun-Controlnet-Union-w4a8`](https://huggingface.co/berryber09/MiniMax-H3-Fun-Controlnet-Union-w4a8) | minimax-h3 | controlnet, comfyui, quantized, base_model:alibaba-pai/MiniMax-H3-Fun-Controlnet-Union, base_model:adapter:alibaba-pai/MiniMax-H3-Fun-Controlnet-Union, license:other |

### 09-风格题材LoRA

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-10 | 61724 | 379 | [`fal/MiniMax-H3-Realism-People-LoRA`](https://huggingface.co/fal/MiniMax-H3-Realism-People-LoRA) | image-text-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 22396 | 5 | [`rzgar/minimax_h3_fl2v_lightx2v_4step_int8-convrot_comfy`](https://huggingface.co/rzgar/minimax_h3_fl2v_lightx2v_4step_int8-convrot_comfy) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-09 | 19649 | 6 | [`nyxia/H3-Loras`](https://huggingface.co/nyxia/H3-Loras) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 18477 | 109 | [`Jojocodex/minimax-h3-spatial-physics-lora`](https://huggingface.co/Jojocodex/minimax-h3-spatial-physics-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-21 | 12081 | 0 | [`NTU-yiwen/awm-minimax-h3-new1344-lora-checkpoints`](https://huggingface.co/NTU-yiwen/awm-minimax-h3-new1344-lora-checkpoints) | minimax-h3 | lora |
| 2026-08-16 | 10211 | 63 | [`Jojocodex/minimax-h3-Camera-Motion-lora`](https://huggingface.co/Jojocodex/minimax-h3-Camera-Motion-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 7195 | 55 | [`Jojocodex/minimax-h3-wushu-action-lora`](https://huggingface.co/Jojocodex/minimax-h3-wushu-action-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-30 | 6776 | 28 | [`Jojocodex/wushu-action-v7-minimax-h3-fl2va-ref2va-lora`](https://huggingface.co/Jojocodex/wushu-action-v7-minimax-h3-fl2va-ref2va-lora) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 5966 | 0 | [`KENIC-1/Comfy-Org-MiniMax-H3-loras`](https://huggingface.co/KENIC-1/Comfy-Org-MiniMax-H3-loras) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 4808 | 41 | [`rzgar/minimax-h3_fl2v_8Step_motion_enhancer`](https://huggingface.co/rzgar/minimax-h3_fl2v_8Step_motion_enhancer) | image-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-25 | 4320 | 70 | [`lovis93/studio-1939-old-animation-lora-minimax-h3`](https://huggingface.co/lovis93/studio-1939-old-animation-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-24 | 4280 | 13 | [`Beidouqixing/minimax-h3-4step-lora-flashgen`](https://huggingface.co/Beidouqixing/minimax-h3-4step-lora-flashgen) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-31 | 4278 | 52 | [`prithivMLmods/MiniMax-H3-Facial-Realism-CloseUp`](https://huggingface.co/prithivMLmods/MiniMax-H3-Facial-Realism-CloseUp) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-15 | 3835 | 25 | [`MATLOWAI/MiniMax-H3-Motion-Adapter`](https://huggingface.co/MATLOWAI/MiniMax-H3-Motion-Adapter) | image-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-08-31 | 2536 | 53 | [`KennethFal/vh5tape-vhs-lora-minimax-h3`](https://huggingface.co/KennethFal/vh5tape-vhs-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-01 | 2344 | 22 | [`JOKER141/MiniMax-H3-Combat-Base-V2`](https://huggingface.co/JOKER141/MiniMax-H3-Combat-Base-V2) | minimax-h3 | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-08-09 | 1936 | 2 | [`multimodalart/MiniMax-H3-Pruned`](https://huggingface.co/multimodalart/MiniMax-H3-Pruned) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 1796 | 1 | [`masafy/minimax-h3-masafy-lora`](https://huggingface.co/masafy/minimax-h3-masafy-lora) | image-to-video | lora, character-lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-21 | 1456 | 0 | [`sonnybox/MiniMax-H3_experimental`](https://huggingface.co/sonnybox/MiniMax-H3_experimental) | image-text-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-06 | 1323 | 82 | [`Alissonerdx/Minimax-H3-ComfyUI`](https://huggingface.co/Alissonerdx/Minimax-H3-ComfyUI) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-06 | 1191 | 2 | [`kabachuha/mh3-morphing-helper`](https://huggingface.co/kabachuha/mh3-morphing-helper) | image-text-to-video | lora, template:diffusion-lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-05 | 1163 | 60 | [`speach1sdef178/MiniMax-H3-Semantic-Bridge`](https://huggingface.co/speach1sdef178/MiniMax-H3-Semantic-Bridge) | minimax-h3 | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 898 | 16 | [`siraxe/3d_to_real_detail_slider_H3`](https://huggingface.co/siraxe/3d_to_real_detail_slider_H3) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-04 | 859 | 25 | [`JOKER141/MiniMax-H3-Weapon-Combat-LoRA`](https://huggingface.co/JOKER141/MiniMax-H3-Weapon-Combat-LoRA) | minimax-h3 | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-20 | 847 | 10 | [`ostris/minimax_h3_ref2va_jacked_lora`](https://huggingface.co/ostris/minimax_h3_ref2va_jacked_lora) | video-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 743 | 13 | [`siraxe/H3_slider_experiments`](https://huggingface.co/siraxe/H3_slider_experiments) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-16 | 671 | 2 | [`taurusduan/MiniMax-H3-Realism-People-LoRA`](https://huggingface.co/taurusduan/MiniMax-H3-Realism-People-LoRA) | image-text-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 533 | 1 | [`B4100/vh5tape-vhs-lora-minimax-h3`](https://huggingface.co/B4100/vh5tape-vhs-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 169 | 2 | [`t8star/Minimax-H3-World-Comfy`](https://huggingface.co/t8star/Minimax-H3-World-Comfy) | image-to-video | comfyui, lora, license:apache-2.0 |
| 2026-09-02 | 112 | 1 | [`B4100/MiniMax-H3-Facial-Realism-CloseUp`](https://huggingface.co/B4100/MiniMax-H3-Facial-Realism-CloseUp) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 88 | 0 | [`TheMindExpansionNetwork/swingusinnerz_t2v_minimax_h3_v1`](https://huggingface.co/TheMindExpansionNetwork/swingusinnerz_t2v_minimax_h3_v1) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-08-29 | 36 | 0 | [`nikomateos/minimax-h3-project-lora`](https://huggingface.co/nikomateos/minimax-h3-project-lora) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-10 | 19 | 1 | [`Efficient-Large-Model/H3-to-LTX-Latent-Adapter`](https://huggingface.co/Efficient-Large-Model/H3-to-LTX-Latent-Adapter) | minimax-h3 |  |
| 2026-09-05 | 4 | 11 | [`prithivMLmods/MiniMax-H3-I2V-Anime-Motion-LoRA`](https://huggingface.co/prithivMLmods/MiniMax-H3-I2V-Anime-Motion-LoRA) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 0 | 22 | [`ostris/minimax_h3_training_adapter`](https://huggingface.co/ostris/minimax_h3_training_adapter) |  |  |
| 2026-08-09 | 0 | 19 | [`tutututututu/Tutu-MiniMax-H3-AudioVideo-20to8-NFE-LoRA`](https://huggingface.co/tutututututu/Tutu-MiniMax-H3-AudioVideo-20to8-NFE-LoRA) | image-text-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 15 | [`ethanfel/MiniMax-H3-Pruned-Ref2VA-Delta-LoRAs-Experimental`](https://huggingface.co/ethanfel/MiniMax-H3-Pruned-Ref2VA-Delta-LoRAs-Experimental) |  | comfyui, lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-10 | 0 | 0 | [`yitongl/minimax-h3-nvfp4-lora-recovery`](https://huggingface.co/yitongl/minimax-h3-nvfp4-lora-recovery) |  | nvfp4, quantization, lora, post-training-quantization, license:other |
| 2026-08-14 | 0 | 16 | [`DiffSynth-Studio/MiniMax-H3-LoRA-LineartAnime`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-LoRA-LineartAnime) |  | license:apache-2.0 |
| 2026-08-18 | 0 | 84 | [`mvp-lab/MiniMax-H3-RAVEN-Streaming-LoRA`](https://huggingface.co/mvp-lab/MiniMax-H3-RAVEN-Streaming-LoRA) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 0 | 12 | [`diffusers-modular/minimax-h3-inpainting`](https://huggingface.co/diffusers-modular/minimax-h3-inpainting) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-01 | 0 | 40 | [`JOKER141/MiniMax-H3-General-Motion-Continuity-Repair`](https://huggingface.co/JOKER141/MiniMax-H3-General-Motion-Continuity-Repair) |  | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-03 | 0 | 32 | [`rehan-fal/minimax-h3-vr180-sbs-lora`](https://huggingface.co/rehan-fal/minimax-h3-vr180-sbs-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 0 | 17 | [`shamanic/minimax-h3-equi360-lora`](https://huggingface.co/shamanic/minimax-h3-equi360-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 0 | 8 | [`EllipsesMark/minimax-h3-vr180-sbs-lora`](https://huggingface.co/EllipsesMark/minimax-h3-vr180-sbs-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 0 | 11 | [`TenStrip/Minimax-h3_Singularity-Lora`](https://huggingface.co/TenStrip/Minimax-h3_Singularity-Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 10-Apple-MLX

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-03 | 4546 | 15 | [`ddalcu/MiniMax-H3-FL2VA-MLX-Serve-8bit`](https://huggingface.co/ddalcu/MiniMax-H3-FL2VA-MLX-Serve-8bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 4242 | 7 | [`pipenetwork/MiniMax-H3-MLX-8bit`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-8bit) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 2688 | 7 | [`ddalcu/MiniMax-H3-FL2VA-MLX-Serve-4bit`](https://huggingface.co/ddalcu/MiniMax-H3-FL2VA-MLX-Serve-4bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 1856 | 6 | [`pipenetwork/MiniMax-H3-MLX-4bit`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-4bit) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 1219 | 6 | [`pipenetwork/MiniMax-H3-MLX-bf16`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-bf16) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 685 | 1 | [`water1234/MiniMax-H3-MLX-Argus-Calibrated-INT8`](https://huggingface.co/water1234/MiniMax-H3-MLX-Argus-Calibrated-INT8) | text-to-video | mlx, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-09 | 2 | 0 | [`Vayden/Qwen3-VL-32B-H3-MLX-q8-vision-paged`](https://huggingface.co/Vayden/Qwen3-VL-32B-H3-MLX-q8-vision-paged) | mlx | mlx, comfyui, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:other |
| 2026-09-09 | 1 | 0 | [`Vayden/MiniMax-H3-Ref2VA-MLX-q8-extended-paged`](https://huggingface.co/Vayden/MiniMax-H3-Ref2VA-MLX-q8-extended-paged) | mlx | mlx, comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-09 | 0 | 0 | [`yvankob/minimax-h3-base-8bit-mlx-by-appautomaton`](https://huggingface.co/yvankob/minimax-h3-base-8bit-mlx-by-appautomaton) | text-to-video | mlx, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 11-组件-VAE-TE-提示器

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-20 | 19222 | 54 | [`iamkaikai/MiniMax-H3-Single-Frame-VAE-500K`](https://huggingface.co/iamkaikai/MiniMax-H3-Single-Frame-VAE-500K) | diffusers | base_model:Mamad8/MiniMax-H3-Image-VAE, base_model:finetune:Mamad8/MiniMax-H3-Image-VAE |
| 2026-08-18 | 857 | 41 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B) | image-text-to-text | lora, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:adapter:Qwen/Qwen3-VL-8B-Instruct |
| 2026-08-18 | 653 | 0 | [`6block/MiniMax-H3-Qwen3-VL-NVFP4`](https://huggingface.co/6block/MiniMax-H3-Qwen3-VL-NVFP4) | text-to-video | nvfp4, comfyui, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-07 | 569 | 182 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA) | peft | lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B |
| 2026-08-26 | 489 | 44 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni) | text-generation | lora, base_model:Qwen/Qwen2.5-Omni-7B, base_model:adapter:Qwen/Qwen2.5-Omni-7B, license:other |
| 2026-08-19 | 362 | 0 | [`qtum/MiniMax-H3-Qwen3-VL-NVFP4`](https://huggingface.co/qtum/MiniMax-H3-Qwen3-VL-NVFP4) | text-to-video | nvfp4, comfyui, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-05 | 98 | 2 | [`pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-NVFP4-AWQ`](https://huggingface.co/pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-NVFP4-AWQ) | image-text-to-text | nvfp4, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-09-02 | 42 | 12 | [`Asirus/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY`](https://huggingface.co/Asirus/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY) |  | comfyui, requantization, base_model:LBH-123-AI/Minimax_h3_latent_Upscaler, base_model:finetune:LBH-123-AI/Minimax_h3_latent_Upscaler, license:apache-2.0 |
| 2026-09-07 | 35 | 2 | [`PuppetVision/qwen3vl-32b-minimax-h3-amd-rocm-optimized-comfy-triton`](https://huggingface.co/PuppetVision/qwen3vl-32b-minimax-h3-amd-rocm-optimized-comfy-triton) | minimax-h3 | comfyui, int8, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-19 | 26 | 1 | [`moonzerokevin/qwen3vl-32b-minimax-h3-nf4`](https://huggingface.co/moonzerokevin/qwen3vl-32b-minimax-h3-nf4) | image-text-to-text | nf4, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-04 | 0 | 202 | [`sakamakismile/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/sakamakismile/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-05 | 0 | 22 | [`linjian257/qwen3vl_32b_minimax_h3_int8_convrot_uncensored-by-linjian257`](https://huggingface.co/linjian257/qwen3vl_32b_minimax_h3_int8_convrot_uncensored-by-linjian257) |  | comfyui, int8, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-07 | 0 | 165 | [`Momoking/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Momoking/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-08 | 0 | 77 | [`Mamad8/MiniMax-H3-Image-VAE`](https://huggingface.co/Mamad8/MiniMax-H3-Image-VAE) |  | comfyui |
| 2026-08-09 | 0 | 144 | [`NicoLab28/ClipProj-MiniMax-H3`](https://huggingface.co/NicoLab28/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-14 | 0 | 6 | [`DiffSynth-Studio/MiniMax-H3-Text-Embeddings`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-Text-Embeddings) |  | license:apache-2.0 |
| 2026-08-17 | 0 | 270 | [`LBH-123-AI/Minimax_h3_latent_Upscaler`](https://huggingface.co/LBH-123-AI/Minimax_h3_latent_Upscaler) |  |  |
| 2026-08-17 | 0 | 0 | [`xdkings/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/xdkings/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-27 | 0 | 0 | [`Jamphus/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Jamphus/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-29 | 0 | 0 | [`jackieccwu/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/jackieccwu/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-30 | 0 | 0 | [`cjpgxm/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/cjpgxm/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-31 | 0 | 0 | [`taurusduan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/taurusduan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-01 | 0 | 23 | [`lihaoyun6/MiniMax-H3-VAE-ONNX`](https://huggingface.co/lihaoyun6/MiniMax-H3-VAE-ONNX) |  | base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-07 | 0 | 0 | [`Allen987/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Allen987/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-08 | 0 | 0 | [`Jackxuanxuan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Jackxuanxuan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-09 | 0 | 0 | [`cuifurong/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/cuifurong/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |

### 12-题材角色LoRA含NSFW

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-18 | 28914 | 23 | [`Hearmeman/minimax-h3-loras`](https://huggingface.co/Hearmeman/minimax-h3-loras) | text-to-video | lora, comfyui, nsfw, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 19074 | 2 | [`lynaNSFW/DaSiWa_MiniMax_H3`](https://huggingface.co/lynaNSFW/DaSiWa_MiniMax_H3) | text-to-image | lora, template:diffusion-lora, base_model:lynaNSFW/minimaxH3_Collection, base_model:adapter:lynaNSFW/minimaxH3_Collection |
| 2026-08-16 | 7784 | 21 | [`sakamakismile/10Eros-Max-beta2-NVFP4`](https://huggingface.co/sakamakismile/10Eros-Max-beta2-NVFP4) | image-to-video | nvfp4, comfyui, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-30 | 6764 | 7 | [`berryber09/10Eros-Max-h3-turbo-hybrid-beta4-w4a8`](https://huggingface.co/berryber09/10Eros-Max-h3-turbo-hybrid-beta4-w4a8) | text-to-video | comfyui, quantized, turbo, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-21 | 5119 | 11 | [`Abiray/10Eros-Max-fl2va-Beta2-GGUF`](https://huggingface.co/Abiray/10Eros-Max-fl2va-Beta2-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-23 | 2576 | 7 | [`Abiray/10Eros-Max-ref2va-Beta2-GGUF`](https://huggingface.co/Abiray/10Eros-Max-ref2va-Beta2-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-09-04 | 1907 | 3 | [`brurpo/DaSiWa-MiniMax-H3-Hybrid`](https://huggingface.co/brurpo/DaSiWa-MiniMax-H3-Hybrid) | image-text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 1630 | 4 | [`lynaNSFW/minimaxH3_Collection`](https://huggingface.co/lynaNSFW/minimaxH3_Collection) | text-to-image | lora, template:diffusion-lora, base_model:pmczip/MiniMaxH3_LoRAs, base_model:adapter:pmczip/MiniMaxH3_LoRAs |
| 2026-08-05 | 1193 | 390 | [`SexGod1979/PinkCherry_MiniMax-H3`](https://huggingface.co/SexGod1979/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-25 | 1190 | 3 | [`berryber09/10Eros-Max-h3-turbo-hybrid-beta3-w4a8`](https://huggingface.co/berryber09/10Eros-Max-h3-turbo-hybrid-beta3-w4a8) | text-to-video | comfyui, quantized, turbo, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-29 | 1135 | 2 | [`LokkenJP/10Eros_Max_optimized_w4a8_exp_learned`](https://huggingface.co/LokkenJP/10Eros_Max_optimized_w4a8_exp_learned) | image-text-to-video | comfyui, int8, quantization, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-18 | 1104 | 119 | [`SexGod1979/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/SexGod1979/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-08-20 | 860 | 0 | [`vasilerosca891/MiniMax-H3`](https://huggingface.co/vasilerosca891/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-27 | 391 | 0 | [`Wesley1234/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8`](https://huggingface.co/Wesley1234/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-05 | 386 | 100 | [`SexGod1979/PinkFluffyBunny-MiniMax-H3`](https://huggingface.co/SexGod1979/PinkFluffyBunny-MiniMax-H3) |  | license:apache-2.0 |
| 2026-08-14 | 286 | 102 | [`Smite79/MiniMax-H3-Longvideos`](https://huggingface.co/Smite79/MiniMax-H3-Longvideos) | text-to-video | comfyui, comfyui-nodes, license:other |
| 2026-09-07 | 53 | 43 | [`SexGod1979/NaughtyTimes-MiniMax-H3`](https://huggingface.co/SexGod1979/NaughtyTimes-MiniMax-H3) |  | license:apache-2.0 |
| 2026-08-05 | 0 | 18 | [`DmitryDB/MiniMax-H3-10Eros-Max-Quants`](https://huggingface.co/DmitryDB/MiniMax-H3-10Eros-Max-Quants) | image-text-to-video | comfyui, quantization, int8, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-10 | 0 | 14 | [`t8star/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8`](https://huggingface.co/t8star/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-24 | 0 | 101 | [`Playtime-AI/Minimax_H3-Sydney_Sweeney`](https://huggingface.co/Playtime-AI/Minimax_H3-Sydney_Sweeney) |  | license:apache-2.0 |
| 2026-08-24 | 0 | 11 | [`Playtime-AI/Minimax_H3-Salma_Hayek`](https://huggingface.co/Playtime-AI/Minimax_H3-Salma_Hayek) |  | license:apache-2.0 |
| 2026-08-26 | 0 | 22 | [`Playtime-AI/Minimax_H3-Margot_Robbie`](https://huggingface.co/Playtime-AI/Minimax_H3-Margot_Robbie) |  | license:apache-2.0 |
| 2026-08-27 | 0 | 11 | [`Playtime-AI/Minimax_H3-Zendaya`](https://huggingface.co/Playtime-AI/Minimax_H3-Zendaya) |  | license:apache-2.0 |
| 2026-08-29 | 0 | 44 | [`Playtime-AI/Minimax_H3-Megan_Fox`](https://huggingface.co/Playtime-AI/Minimax_H3-Megan_Fox) |  | license:apache-2.0 |
| 2026-08-31 | 0 | 23 | [`Playtime-AI/Minimax_H3-Anya_Taylor_Joy`](https://huggingface.co/Playtime-AI/Minimax_H3-Anya_Taylor_Joy) |  | license:apache-2.0 |
| 2026-09-09 | 0 | 0 | [`laoda/DasiwaMinimaxH3_dasiwaHybrid8turboV1`](https://huggingface.co/laoda/DasiwaMinimaxH3_dasiwaHybrid8turboV1) | text-to-video | comfyui |

### 13-微调合并实验

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-09-05 | 96682 | 262 | [`WarmBloodAban/Minimax-h3_Singularity`](https://huggingface.co/WarmBloodAban/Minimax-h3_Singularity) | image-to-video | comfyui, license:apache-2.0 |
| 2026-08-06 | 14027 | 0 | [`KENIC-1/Comfy-Org-MiniMax-H3`](https://huggingface.co/KENIC-1/Comfy-Org-MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 13699 | 20 | [`t8star/Vdn-Minimax-H3-Comfy`](https://huggingface.co/t8star/Vdn-Minimax-H3-Comfy) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 13464 | 3 | [`taurusduan/MiniMax-H3`](https://huggingface.co/taurusduan/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 2097 | 12 | [`Hippotes/MiniMax-H3-Experiments`](https://huggingface.co/Hippotes/MiniMax-H3-Experiments) | diffusers | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 47 | 0 | [`kevin-mi/VDN-H3-overlay`](https://huggingface.co/kevin-mi/VDN-H3-overlay) | minimax-h3 | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-02 | 39 | 286 | [`OpenVDN/vdn-minimax-h3`](https://huggingface.co/OpenVDN/vdn-minimax-h3) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-10 | 10 | 0 | [`taurusduan/Vdn-Minimax-H3-Comfy`](https://huggingface.co/taurusduan/Vdn-Minimax-H3-Comfy) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 68 | [`Plaguekind/Minimax-H3`](https://huggingface.co/Plaguekind/Minimax-H3) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-11 | 0 | 75 | [`Inner-Reflections/MiniMax-H3-Looping-Sketch-Anime`](https://huggingface.co/Inner-Reflections/MiniMax-H3-Looping-Sketch-Anime) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3 |
| 2026-08-11 | 0 | 238 | [`smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-25 | 0 | 26 | [`FX-FeiHou/MiniMax-H3-Remix`](https://huggingface.co/FX-FeiHou/MiniMax-H3-Remix) | image-to-video | comfyui, license:other |
| 2026-09-10 | 0 | 0 | [`ibyteohdear/MiniMax-H3-LightX8-Fused-fl2v`](https://huggingface.co/ibyteohdear/MiniMax-H3-LightX8-Fused-fl2v) | image-text-to-video | license:other |

### 14-工作流工具箱

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-04 | 571 | 69 | [`joeygambino/MiniMax-H3-Multishot-Workflow`](https://huggingface.co/joeygambino/MiniMax-H3-Multishot-Workflow) | text-to-video | comfyui, license:apache-2.0 |
| 2026-08-09 | 0 | 171 | [`PoopMan333/H3_Character_Sheet_Generator`](https://huggingface.co/PoopMan333/H3_Character_Sheet_Generator) | image-to-image | comfyui, license:other |
| 2026-08-28 | 0 | 23 | [`RuneXX/Minimax-H3-Workflows`](https://huggingface.co/RuneXX/Minimax-H3-Workflows) | image-to-video | comfy, comfyui |
| 2026-09-02 | 0 | 10 | [`PoopMan333/H3_Easy_Ref2V_Workflow`](https://huggingface.co/PoopMan333/H3_Easy_Ref2V_Workflow) | video-to-video | comfyui, license:other |
| 2026-09-07 | 0 | 2 | [`jayseanbrambila/minimax-h3-prompt-workflow-toolkit`](https://huggingface.co/jayseanbrambila/minimax-h3-prompt-workflow-toolkit) | image-to-video | license:apache-2.0 |

### 15-镜像转载与其它

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-21 | 4475 | 4 | [`jasperz111/redcraft-minimax-h3-a2a-redmix`](https://huggingface.co/jasperz111/redcraft-minimax-h3-a2a-redmix) | minimax-h3 | comfyui |
| 2026-08-24 | 1575 | 0 | [`fkyyy/MiniMax-H3-slim`](https://huggingface.co/fkyyy/MiniMax-H3-slim) | image-text-to-video | license:other |
| 2026-08-15 | 1032 | 0 | [`MHWJJ/MiniMax-H3`](https://huggingface.co/MHWJJ/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 914 | 0 | [`Stim748/MiniMax-H3`](https://huggingface.co/Stim748/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-15 | 899 | 0 | [`JNcharkey1/MiniMax-H3`](https://huggingface.co/JNcharkey1/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-13 | 887 | 0 | [`burningfeet/MiniMax-H3`](https://huggingface.co/burningfeet/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 881 | 0 | [`A1Azmi/MiniMax-H3`](https://huggingface.co/A1Azmi/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 876 | 0 | [`Lite01385/MiniMax-H3`](https://huggingface.co/Lite01385/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-18 | 875 | 0 | [`LILUMY/MiniMax-H3`](https://huggingface.co/LILUMY/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-16 | 811 | 0 | [`musafa901/MiniMax-H3_20260816`](https://huggingface.co/musafa901/MiniMax-H3_20260816) | image-text-to-video | license:other |
| 2026-08-27 | 609 | 0 | [`ljt520lxy/MiniMax-H3`](https://huggingface.co/ljt520lxy/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-01 | 213 | 0 | [`skySakir/MiniMax-H3`](https://huggingface.co/skySakir/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 198 | 21 | [`unsloth/MiniMax-H3`](https://huggingface.co/unsloth/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-05 | 135 | 0 | [`xiaogongshou/MiniMax-H3`](https://huggingface.co/xiaogongshou/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-02 | 111 | 0 | [`star08/MiniMax-H3`](https://huggingface.co/star08/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-03 | 110 | 1 | [`wudingdeet/MiniMax-H3`](https://huggingface.co/wudingdeet/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-01 | 103 | 0 | [`saluca-labs/MiniMax-H3`](https://huggingface.co/saluca-labs/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-09 | 90 | 1 | [`Rurbino/MiniMax-H3`](https://huggingface.co/Rurbino/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 0 | 1 | [`acckpoot/MiniMax-H3`](https://huggingface.co/acckpoot/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-04 | 0 | 164 | [`Kijai/MiniMax-H3-TAE`](https://huggingface.co/Kijai/MiniMax-H3-TAE) |  | license:apache-2.0 |
| 2026-08-05 | 0 | 22 | [`AiNinja94/MiniMax-H3`](https://huggingface.co/AiNinja94/MiniMax-H3) |  |  |
| 2026-08-05 | 0 | 434 | [`Kijai/MiniMax-H3-experimental`](https://huggingface.co/Kijai/MiniMax-H3-experimental) |  |  |
| 2026-08-06 | 0 | 51 | [`EllaPriest45/MinimaxH3_Actions`](https://huggingface.co/EllaPriest45/MinimaxH3_Actions) |  |  |
| 2026-08-06 | 0 | 13 | [`EllaPriest45/MinimaxH3_Styles`](https://huggingface.co/EllaPriest45/MinimaxH3_Styles) |  |  |
| 2026-08-07 | 0 | 419 | [`Kijai/MiniMax-H3_comfy`](https://huggingface.co/Kijai/MiniMax-H3_comfy) |  |  |
| 2026-08-07 | 0 | 46 | [`silveroxides/MiniMax-H3_tests`](https://huggingface.co/silveroxides/MiniMax-H3_tests) |  |  |
| 2026-08-08 | 0 | 3 | [`jayseanbrambila/MiniMax-H3-AI-Video-Generator`](https://huggingface.co/jayseanbrambila/MiniMax-H3-AI-Video-Generator) | image-to-video | comfyui, license:mit |
| 2026-08-10 | 0 | 15 | [`JahJedi/MiniMax-H3-Character-Sheet`](https://huggingface.co/JahJedi/MiniMax-H3-Character-Sheet) |  | comfyui, license:apache-2.0 |
| 2026-09-03 | 0 | 4 | [`junchaoh-cs/SolarWM-H3-33B`](https://huggingface.co/junchaoh-cs/SolarWM-H3-33B) | pytorch |  |
| 2026-09-05 | 0 | 30 | [`malcolmrey/minimaxh3`](https://huggingface.co/malcolmrey/minimaxh3) |  | license:apache-2.0 |
| 2026-09-11 | 0 | 0 | [`drawthingsai/MiniMax-H3`](https://huggingface.co/drawthingsai/MiniMax-H3) | image-text-to-video | license:other |

## 说明

- **15-镜像转载与其它**：多为同名镜像、个人备份、或尚未细分类的仓；使用前请核对 `base_model` 与文件哈希。
- **12-题材角色 LoRA**：含 NSFW / 名人向适配器，仅作索引，不代表推荐。
- 快照文件：`hf_last3m.json`（同日 API 导出）。
