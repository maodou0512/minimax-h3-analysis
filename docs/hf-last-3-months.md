# Hugging Face 近 3 个月 MiniMax H3 相关仓完整清单

> 覆盖窗口：**2026-06-29 → 2026-09-29**。
> 收录：**1035** 个 HF 模型仓（Hub API 检索 + 关键词过滤）。
> `创建日` = `createdAt`；`下载量/Likes` 为抓取快照（2026-09-29），会随时间变化。
> 选型与硬件详解见 [community-versions.md](community-versions.md)；本页追求**近 3 个月全量索引**。
> 官方开源公告日：**2026-08-03**（与部分仓 `createdAt` 早于该日不冲突——预上传常见）。
> 本次（2026-09-29）检索面比上一版（2026-09-11，315 仓）更宽：除 `MiniMax-H3` 关键词外，还按 `base_model:*MiniMax-H3` / `minimax-h3` 标签与仓名含独立 `H3` 词（如 `*-h3-lora`）补扫，因此部分 9 月 11 日前创建、上一版未收录的仓也在本次出现；已删除/转私有的仓已剔除，改名仓按新名收录。其中 `createdAt` 晚于上一版快照（2026-09-11）的新仓约 **259** 个。

## 分类统计

| 类别 | 数量 |
| --- | ---: |
| 01-官方基座 | 1 |
| 02-Comfy官方生态重打包 | 1 |
| 03-量化与剪枝权重 | 128 |
| 04-GGUF量化 | 54 |
| 05-Turbo少步加速 | 122 |
| 06-加速LoRA-Acc | 11 |
| 07-FastH3蒸馏 | 45 |
| 08-ControlNet控制 | 6 |
| 09-风格题材LoRA | 169 |
| 10-Apple-MLX | 31 |
| 11-组件-VAE-TE-提示器 | 57 |
| 12-题材角色LoRA含NSFW | 117 |
| 13-微调合并实验 | 60 |
| 14-工作流工具箱 | 15 |
| 15-镜像转载与其它 | 218 |
| **合计** | **1035** |

## 完整分表

### 01-官方基座

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-07-28 | 3625289 | 5764 | [`MiniMaxAI/MiniMax-H3`](https://huggingface.co/MiniMaxAI/MiniMax-H3) | image-text-to-video | license:other |

### 02-Comfy官方生态重打包

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-07-30 | 21971246 | 2041 | [`Comfy-Org/MiniMax-H3`](https://huggingface.co/Comfy-Org/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 03-量化与剪枝权重

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-03 | 173251 | 239 | [`Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot`](https://huggingface.co/Abiray/Minimax-H3-nvfp4-INT4-INT8-Convrot) | image-text-to-video | quantized, comfyui, int4, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 120335 | 35 | [`xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI`](https://huggingface.co/xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI) | image-text-to-video | comfyui, int8, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, license:other |
| 2026-09-05 | 79242 | 60 | [`drbaph/Viggle-Animate-ComfyUI`](https://huggingface.co/drbaph/Viggle-Animate-ComfyUI) | video-to-video | comfyui, int8, license:other |
| 2026-08-04 | 49030 | 29 | [`coolthor/MiniMax-H3-pruned-NVFP4`](https://huggingface.co/coolthor/MiniMax-H3-pruned-NVFP4) | image-text-to-video | nvfp4, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 43284 | 27 | [`drbaph/vdn-minimax-h3-int8-convrot-comfyui`](https://huggingface.co/drbaph/vdn-minimax-h3-int8-convrot-comfyui) | minimax-h3 | comfyui, int8, quantization, license:other |
| 2026-08-04 | 37785 | 29 | [`AX1Y2JP/MiniMax-H3-W4A8-ConvRot`](https://huggingface.co/AX1Y2JP/MiniMax-H3-W4A8-ConvRot) | diffusion-single-file | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-22 | 25804 | 14 | [`Winnougan/Cobijada_Minimax-H3_Hybrid_Pruned_ComfyUI`](https://huggingface.co/Winnougan/Cobijada_Minimax-H3_Hybrid_Pruned_ComfyUI) | image-to-video | comfyui, quantization, int8, license:apache-2.0 |
| 2026-08-03 | 23335 | 28 | [`rockerBOO/minimax-h3-nvfp4-convrot`](https://huggingface.co/rockerBOO/minimax-h3-nvfp4-convrot) | text-to-video | nvfp4, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 22241 | 8 | [`koongrizzly/MiniMax_H3_int4_W4A8_ConvRot_Pruned`](https://huggingface.co/koongrizzly/MiniMax_H3_int4_W4A8_ConvRot_Pruned) | minimax-h3 | int4, quantization, license:apache-2.0 |
| 2026-08-20 | 15257 | 4 | [`MATLOWAI/minimax-h3-nvfp4`](https://huggingface.co/MATLOWAI/minimax-h3-nvfp4) | diffusion-single-file | comfyui, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-22 | 14915 | 101 | [`joeygambino/MiniMax-H3-x-Z-Image-native`](https://huggingface.co/joeygambino/MiniMax-H3-x-Z-Image-native) | text-to-video | comfyui, comfy-native, comfy-quant, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-24 | 14306 | 12 | [`hoidhxd/MiniMax-H3-x-Z-Image-hybrid`](https://huggingface.co/hoidhxd/MiniMax-H3-x-Z-Image-hybrid) | image-to-video | int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 11663 | 10 | [`berryber09/MiniMax-H3-ref2va-fl2va-hybrid-w4a8`](https://huggingface.co/berryber09/MiniMax-H3-ref2va-fl2va-hybrid-w4a8) | image-to-video | comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 7442 | 8 | [`abakanai/Minimax_h3_hybrid`](https://huggingface.co/abakanai/Minimax_h3_hybrid) | image-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-07 | 5326 | 0 | [`abenliao/minimax-h3-transformer-mxfp8`](https://huggingface.co/abenliao/minimax-h3-transformer-mxfp8) | diffusers | fp8, quantized |
| 2026-09-16 | 3810 | 5 | [`sandpies/Minimax-H3-fl2va-ref2va-hybrid-unpruned-int8`](https://huggingface.co/sandpies/Minimax-H3-fl2va-ref2va-hybrid-unpruned-int8) | minimax-h3 | comfyui, int8, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-27 | 3789 | 0 | [`fkyyy/MiniMax-H3-fp8`](https://huggingface.co/fkyyy/MiniMax-H3-fp8) | image-text-to-video | license:other |
| 2026-09-07 | 3479 | 7 | [`xtanqn/MiniMax-H3-fl2va-ref2va-b25-49-r1024-r0`](https://huggingface.co/xtanqn/MiniMax-H3-fl2va-ref2va-b25-49-r1024-r0) | minimax-h3 | fp8, license:other |
| 2026-09-10 | 3189 | 6 | [`jfar-z/MiniMax-H3-FL2VA-Ref2VA-Hybrid-NVFP4`](https://huggingface.co/jfar-z/MiniMax-H3-FL2VA-Ref2VA-Hybrid-NVFP4) | image-to-video | comfyui, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-18 | 2131 | 1 | [`t8star/Meridian-Comfy`](https://huggingface.co/t8star/Meridian-Comfy) | video-to-video | comfyui, int8, base_model:Viggle/Meridian, base_model:finetune:Viggle/Meridian, license:other |
| 2026-08-07 | 2084 | 4 | [`rzgar/minimax_h3_ref2va_fp8_e4m3fn`](https://huggingface.co/rzgar/minimax_h3_ref2va_fp8_e4m3fn) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-03 | 1978 | 23 | [`rzgar/minimax_h3_fl2va_fp8_e4m3fn`](https://huggingface.co/rzgar/minimax_h3_fl2va_fp8_e4m3fn) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-21 | 1960 | 1 | [`rockerBOO/minimax-h3-nvfp4-fp8`](https://huggingface.co/rockerBOO/minimax-h3-nvfp4-fp8) | text-to-video | nvfp4, fp8, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 1732 | 11 | [`Raretutor/vdn-minimax-h3-comfyui-int8-convrot`](https://huggingface.co/Raretutor/vdn-minimax-h3-comfyui-int8-convrot) | text-to-video | comfyui, int8, base_model:OpenVDN/vdn-minimax-h3, base_model:finetune:OpenVDN/vdn-minimax-h3, license:other |
| 2026-09-28 | 1671 | 5 | [`QuantFunc/Minimax-H3-Quantfunc-4bit`](https://huggingface.co/QuantFunc/Minimax-H3-Quantfunc-4bit) | text-to-video | quantized, int4, svdquant, comfyui, license:other |
| 2026-08-09 | 1622 | 1 | [`abenliao/minimax-h3-ref2va-transformer-mxfp8`](https://huggingface.co/abenliao/minimax-h3-ref2va-transformer-mxfp8) | diffusers |  |
| 2026-08-15 | 1495 | 2 | [`joeygambino/MiniMax-H3-comfy-native-fl2va`](https://huggingface.co/joeygambino/MiniMax-H3-comfy-native-fl2va) | text-to-video | comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-20 | 1444 | 0 | [`PulpCut/MiniMax-H3-INT8-ConvRot`](https://huggingface.co/PulpCut/MiniMax-H3-INT8-ConvRot) | minimax-h3 | int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-07 | 1430 | 8 | [`speach1sdef178/VDN-H3-INT8-ConvRot-ComfyUI`](https://huggingface.co/speach1sdef178/VDN-H3-INT8-ConvRot-ComfyUI) | minimax-h3 | comfyui, int8, license:other |
| 2026-08-18 | 1352 | 0 | [`yuivs/Minimax-H3-nvfp4-INT4-INT8-Convrot`](https://huggingface.co/yuivs/Minimax-H3-nvfp4-INT4-INT8-Convrot) | image-text-to-video | quantized, comfyui, int4, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 1316 | 1 | [`1ronman1993/MiniMax-H3-SVDQuant-fp4-pdd8`](https://huggingface.co/1ronman1993/MiniMax-H3-SVDQuant-fp4-pdd8) | minimax-h3 | svdquant, comfyui, license:apache-2.0 |
| 2026-08-11 | 611 | 1 | [`OzzyGT/MiniMax_H3_sdnq_4bit_pruned`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_4bit_pruned) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 568 | 0 | [`AcademiaSD/MiniMax-H3-NF4`](https://huggingface.co/AcademiaSD/MiniMax-H3-NF4) | diffusers |  |
| 2026-09-15 | 531 | 1 | [`wukaikevin/MiniMax-H3-Singularity-Ref2VA-NVFP4`](https://huggingface.co/wukaikevin/MiniMax-H3-Singularity-Ref2VA-NVFP4) | minimax-h3 | nvfp4, quantization, license:apache-2.0 |
| 2026-08-20 | 434 | 1 | [`ravibhai1212/MiniMax_H3_int4_W4A8_ConvRot_Pruned`](https://huggingface.co/ravibhai1212/MiniMax_H3_int4_W4A8_ConvRot_Pruned) | minimax-h3 | int4, quantization, license:apache-2.0 |
| 2026-08-03 | 336 | 1 | [`OzzyGT/MiniMax_H3_sdnq_dynamic_4bit`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_dynamic_4bit) | diffusers |  |
| 2026-08-03 | 331 | 2 | [`Ar4ikov/MiniMax-H3-transformer-W4A16-RTN`](https://huggingface.co/Ar4ikov/MiniMax-H3-transformer-W4A16-RTN) | image-text-to-video | int4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 327 | 6 | [`stdstu123/LynnReal-Onmi-flash-beta-0.1`](https://huggingface.co/stdstu123/LynnReal-Onmi-flash-beta-0.1) | diffusers | int8 |
| 2026-08-09 | 290 | 1 | [`abhishekchohan/minimax-h3-int8`](https://huggingface.co/abhishekchohan/minimax-h3-int8) | text-to-video | quantization, quantized, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 273 | 4 | [`taurusduan/MiniMax-H3-x-Z-Image-hybrid`](https://huggingface.co/taurusduan/MiniMax-H3-x-Z-Image-hybrid) | image-to-video | int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-12 | 217 | 0 | [`ibyteohdear/MiniMax-H3-Pruned-LightX8-Fused`](https://huggingface.co/ibyteohdear/MiniMax-H3-Pruned-LightX8-Fused) | image-text-to-video | license:other |
| 2026-09-01 | 217 | 1 | [`rootonchair/MiniMax-H3-nunchaku-lite-nvfp4`](https://huggingface.co/rootonchair/MiniMax-H3-nunchaku-lite-nvfp4) | diffusers | svdquant, quantized, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 182 | 0 | [`1ronman1993/MiniMax-H3-SVDQuant-int4-pdd8`](https://huggingface.co/1ronman1993/MiniMax-H3-SVDQuant-int4-pdd8) | minimax-h3 | svdquant, comfyui, license:apache-2.0 |
| 2026-09-01 | 180 | 1 | [`rootonchair/MiniMax-H3-nunchaku-lite-int4`](https://huggingface.co/rootonchair/MiniMax-H3-nunchaku-lite-int4) | diffusers | svdquant, quantized, int4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 152 | 0 | [`Papina/MiniMax-H3-ref2va-int8`](https://huggingface.co/Papina/MiniMax-H3-ref2va-int8) | image-text-to-video | quantized, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 150 | 7 | [`diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024`](https://huggingface.co/diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024) | image-text-to-video | base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-17 | 145 | 0 | [`wangpj/MiniMax-H3_fp8`](https://huggingface.co/wangpj/MiniMax-H3_fp8) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 127 | 0 | [`abhishekchohan/minimax-h3-fp8`](https://huggingface.co/abhishekchohan/minimax-h3-fp8) | text-to-video | quantization, quantized, fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 111 | 0 | [`aufjsufjaujda3/vdn-minimax-h3-int8-convrot-comfyui`](https://huggingface.co/aufjsufjaujda3/vdn-minimax-h3-int8-convrot-comfyui) | minimax-h3 | comfyui, int8, quantization, license:other |
| 2026-08-10 | 107 | 2 | [`t8star/minimax_h3_ref2va_patchin_hf102`](https://huggingface.co/t8star/minimax_h3_ref2va_patchin_hf102) | image-text-to-video | comfyui, int8-convrot, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-11 | 97 | 0 | [`OzzyGT/MiniMax_H3_sdnq_8bit_pruned`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_8bit_pruned) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 88 | 44 | [`Merserk/MiniMax-H3-INT4-ConvRot`](https://huggingface.co/Merserk/MiniMax-H3-INT4-ConvRot) | image-text-to-video | comfyui, int4, license:other |
| 2026-09-07 | 82 | 0 | [`cccian091/MiniMax-H3-T2V-NVFP4`](https://huggingface.co/cccian091/MiniMax-H3-T2V-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-19 | 77 | 0 | [`tsolful/Minimax_H3_W4A8`](https://huggingface.co/tsolful/Minimax_H3_W4A8) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 68 | 0 | [`Wesley1234/minimax_h3_ref2va_patchin_hf102`](https://huggingface.co/Wesley1234/minimax_h3_ref2va_patchin_hf102) | image-text-to-video | comfyui, int8-convrot, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-04 | 59 | 0 | [`OzzyGT/MiniMax_H3_sdnq_dynamic_8bit`](https://huggingface.co/OzzyGT/MiniMax_H3_sdnq_dynamic_8bit) | diffusers |  |
| 2026-09-28 | 56 | 8 | [`isichan-ai/MiniMax-H3-FL2VA-norefiner`](https://huggingface.co/isichan-ai/MiniMax-H3-FL2VA-norefiner) | minimax-h3 | comfyui, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-23 | 54 | 0 | [`kato96/Viggle-Animate-ComfyUI`](https://huggingface.co/kato96/Viggle-Animate-ComfyUI) | video-to-video | comfyui, int8, license:other |
| 2026-08-09 | 35 | 0 | [`CalamitousFelicitousness/MiniMax-H3-SDNQ-cb4-hadamard-dynamic`](https://huggingface.co/CalamitousFelicitousness/MiniMax-H3-SDNQ-cb4-hadamard-dynamic) | image-text-to-video | quantization, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-24 | 32 | 0 | [`aiinfluencer00/Viggle-Animate-ComfyUI`](https://huggingface.co/aiinfluencer00/Viggle-Animate-ComfyUI) | video-to-video | comfyui, int8, license:other |
| 2026-08-06 | 24 | 1 | [`noctuashap/MiniMax-H3-pruned-r16`](https://huggingface.co/noctuashap/MiniMax-H3-pruned-r16) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-12 | 22 | 0 | [`voosq/minimax-h3-nvfp4-fp8`](https://huggingface.co/voosq/minimax-h3-nvfp4-fp8) | text-to-video | nvfp4, fp8, quantized, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-25 | 14 | 0 | [`Ziyaad30/minimax-h3-fp8`](https://huggingface.co/Ziyaad30/minimax-h3-fp8) | text-to-video | quantization, quantized, fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 13 | 0 | [`abenliao/minimax-h3-conditioner-fp8`](https://huggingface.co/abenliao/minimax-h3-conditioner-fp8) |  | fp8, quantized |
| 2026-08-09 | 9 | 0 | [`abenliao/minimax-h3-conditioner-fp8-stock`](https://huggingface.co/abenliao/minimax-h3-conditioner-fp8-stock) |  |  |
| 2026-08-12 | 2 | 0 | [`Yi30/minimax_h3_mxfp8_packed_pretrained`](https://huggingface.co/Yi30/minimax_h3_mxfp8_packed_pretrained) | diffusers |  |
| 2026-08-04 | 0 | 13 | [`DiffSynth-Studio/MiniMax-H3-NF4`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-NF4) |  | license:apache-2.0 |
| 2026-08-03 | 0 | 37 | [`DmitryDB/MiniMax-H3-ComfyUI-Quants`](https://huggingface.co/DmitryDB/MiniMax-H3-ComfyUI-Quants) | image-text-to-video | comfyui, quantization, int8, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 0 | 7 | [`DmitryDB/MiniMax-H3-DynTime-sQKV`](https://huggingface.co/DmitryDB/MiniMax-H3-DynTime-sQKV) | image-text-to-video | comfyui, quantization, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-09 | 0 | 0 | [`EliovpAI/MiniMax-H3-W4A8-Paiton-RDNA4`](https://huggingface.co/EliovpAI/MiniMax-H3-W4A8-Paiton-RDNA4) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-22 | 0 | 0 | [`Felldude/QWEN_32B_Comfy_MinimaxH3_Pruned_FP32`](https://huggingface.co/Felldude/QWEN_32B_Comfy_MinimaxH3_Pruned_FP32) | text-generation | base_model:Qwen/Qwen3-32B, base_model:finetune:Qwen/Qwen3-32B, license:apache-2.0 |
| 2026-08-03 | 0 | 4 | [`FenomAI/MiniMax-H3`](https://huggingface.co/FenomAI/MiniMax-H3) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 0 | 0 | [`Frosty40/h3-spark`](https://huggingface.co/Frosty40/h3-spark) | comfyui | comfyui, nvfp4, quantization, license:other |
| 2026-08-02 | 0 | 19 | [`Gluttony10/MiniMax-H3-INT8-CONVROT`](https://huggingface.co/Gluttony10/MiniMax-H3-INT8-CONVROT) | image-text-to-video | comfyui, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-24 | 0 | 0 | [`JeffDing/MiniMax_h3_int8_demo`](https://huggingface.co/JeffDing/MiniMax_h3_int8_demo) |  |  |
| 2026-09-21 | 0 | 0 | [`JoyFusionAI/dt-minimax-h3`](https://huggingface.co/JoyFusionAI/dt-minimax-h3) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 7 | [`ModelsLab/MiniMax-H3-ref2va-NVFP4`](https://huggingface.co/ModelsLab/MiniMax-H3-ref2va-NVFP4) |  | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 0 | 0 | [`ModelsLab/MiniMax-H3-svdquant-int4_r32`](https://huggingface.co/ModelsLab/MiniMax-H3-svdquant-int4_r32) | text-to-video | svdquant, int4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 0 | 0 | [`ModelsLab/MiniMax-H3-svdquant-nvfp4_r32`](https://huggingface.co/ModelsLab/MiniMax-H3-svdquant-nvfp4_r32) | text-to-video | svdquant, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 0 | 0 | [`OpenVDN/vdn-minimax-h3-edge`](https://huggingface.co/OpenVDN/vdn-minimax-h3-edge) | text-to-video | fp8, base_model:OpenVDN/vdn-minimax-h3, base_model:finetune:OpenVDN/vdn-minimax-h3, license:other |
| 2026-08-06 | 0 | 1 | [`Rudra-ai/MiniMax-H3-NF4`](https://huggingface.co/Rudra-ai/MiniMax-H3-NF4) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-19 | 0 | 1 | [`RunningHubAI/MiniMax-H3-INT8-CONVROT`](https://huggingface.co/RunningHubAI/MiniMax-H3-INT8-CONVROT) | image-text-to-video | comfyui, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-25 | 0 | 2 | [`RunningHubAI/rh-minimax-h3-hybrid-fl2va-ref2va-b25-49-int8-r-unet`](https://huggingface.co/RunningHubAI/rh-minimax-h3-hybrid-fl2va-ref2va-b25-49-int8-r-unet) | text-to-video | comfyui |
| 2026-08-08 | 0 | 1 | [`SabiQG/minimax-h3-fp8`](https://huggingface.co/SabiQG/minimax-h3-fp8) | image-to-video | fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 0 | [`Simplismart/Minimax-H3-FL2V-NVFP4`](https://huggingface.co/Simplismart/Minimax-H3-FL2V-NVFP4) |  |  |
| 2026-08-16 | 0 | 32 | [`WarmBloodAban/Minimax_h3_ref2va_XUELUO_int8_convrot`](https://huggingface.co/WarmBloodAban/Minimax_h3_ref2va_XUELUO_int8_convrot) |  |  |
| 2026-08-03 | 0 | 27 | [`Winnougan/MiniMax-H3-INT4_Convrot_ComfyUI`](https://huggingface.co/Winnougan/MiniMax-H3-INT4_Convrot_ComfyUI) | image-to-video | comfyui, quantization, int4, license:apache-2.0 |
| 2026-08-25 | 0 | 0 | [`aaaaakkkkk/minimaxH3Remix_int8ConvrotV06`](https://huggingface.co/aaaaakkkkk/minimaxH3Remix_int8ConvrotV06) |  |  |
| 2026-09-28 | 0 | 2 | [`aireet/viggle-animate-workflow`](https://huggingface.co/aireet/viggle-animate-workflow) | image-to-video | comfyui, quantized, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-28 | 0 | 0 | [`binglingzhimeng/minimax_h3_hybrid_fl2va_ref2va_b25-49_w4a8_mixed`](https://huggingface.co/binglingzhimeng/minimax_h3_hybrid_fl2va_ref2va_b25-49_w4a8_mixed) | image-to-video | comfyui, int8, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-17 | 0 | 4 | [`cicalooo/MiniMax-H3-hybrid-b45-49-rtx3090-w4a8-int8`](https://huggingface.co/cicalooo/MiniMax-H3-hybrid-b45-49-rtx3090-w4a8-int8) | text-to-video | comfyui, quantization, int8, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diobrando0/MiniMax-H3-fl2va-ref2va-hybrids-bf16, base_model:merge:diobrando0/MiniMax-H3-fl2va-ref2va-hybrids-bf16, license:other |
| 2026-08-06 | 0 | 1 | [`cicalooo/Minimax-H3-INT8-converts`](https://huggingface.co/cicalooo/Minimax-H3-INT8-converts) | image-text-to-video | comfyui, int8, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 0 | 0 | [`corechan/MiniMax-H3_NF4`](https://huggingface.co/corechan/MiniMax-H3_NF4) | text-generation | quantized, nf4, license:other |
| 2026-08-30 | 0 | 0 | [`corechan/MiniMax-H3_nvfp4`](https://huggingface.co/corechan/MiniMax-H3_nvfp4) | text-generation | quantized, nvfp4, license:other |
| 2026-09-12 | 0 | 3 | [`corechan/MiniMax_H3_Torchao018`](https://huggingface.co/corechan/MiniMax_H3_Torchao018) | text-generation | quantized, nvfp4, int8, license:other |
| 2026-08-10 | 0 | 2 | [`deAPI-ai/minimax-h3-33b-int8`](https://huggingface.co/deAPI-ai/minimax-h3-33b-int8) | text-to-video | int8, license:other |
| 2026-08-03 | 0 | 0 | [`dimitarx/MiniMax-H3-fp8`](https://huggingface.co/dimitarx/MiniMax-H3-fp8) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-08-03 | 0 | 10 | [`dotexec/MiniMax-H3-T2V-NVFP4`](https://huggingface.co/dotexec/MiniMax-H3-T2V-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-21 | 0 | 2 | [`dreamkrate/Minimax-H3-Hybrid-BF16-Pruned`](https://huggingface.co/dreamkrate/Minimax-H3-Hybrid-BF16-Pruned) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 0 | [`endman100/MiniMax-H3-FL2VA-FP8`](https://huggingface.co/endman100/MiniMax-H3-FL2VA-FP8) |  | comfyui, fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 1 | [`endman100/MiniMax-H3-Ref2VA-FP8`](https://huggingface.co/endman100/MiniMax-H3-Ref2VA-FP8) |  | comfyui, fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 0 | [`feizhai123/MiniMax-H3-ModelOpt-Mixed9-Dynamic-FP8`](https://huggingface.co/feizhai123/MiniMax-H3-ModelOpt-Mixed9-Dynamic-FP8) | image-text-to-video | fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 1 | [`felipesztutman/MiniMax-H3-W4A4`](https://huggingface.co/felipesztutman/MiniMax-H3-W4A4) | text-to-video | quantization, svdquant, int4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 0 | [`harsh171104/MiniMax-H3-FP8`](https://huggingface.co/harsh171104/MiniMax-H3-FP8) | diffusers |  |
| 2026-09-02 | 0 | 0 | [`herb786/MiniMaxH3-acheze-int8`](https://huggingface.co/herb786/MiniMaxH3-acheze-int8) | diffusers | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-08-24 | 0 | 0 | [`hoidhxd/MiniMax-H3-x-Z-Image-bf16`](https://huggingface.co/hoidhxd/MiniMax-H3-x-Z-Image-bf16) | safetensors | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-03 | 0 | 130 | [`lilcheaty/MiniMax-H3-NVFP4`](https://huggingface.co/lilcheaty/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-13 | 0 | 0 | [`naiwen888/MiniMax-H3-NVFP4`](https://huggingface.co/naiwen888/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 0 | 3 | [`natalie5/MiniMax-H3-INT8-CONVROT`](https://huggingface.co/natalie5/MiniMax-H3-INT8-CONVROT) |  |  |
| 2026-09-27 | 0 | 0 | [`nrxdkx/minimax_h3_fl2va_pruned_int8_convrot`](https://huggingface.co/nrxdkx/minimax_h3_fl2va_pruned_int8_convrot) |  |  |
| 2026-09-02 | 0 | 2 | [`pottokao/H3-RotNVFP4-ComfyUI-Loader`](https://huggingface.co/pottokao/H3-RotNVFP4-ComfyUI-Loader) | minimax-h3 | comfyui, nvfp4, license:apache-2.0 |
| 2026-09-02 | 0 | 1 | [`pottokao/MiniMax-H3-NVFP4-rotated`](https://huggingface.co/pottokao/MiniMax-H3-NVFP4-rotated) | text-to-video | comfyui, nvfp4, quantization, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 0 | 0 | [`pottokao/minimax-h3-2x16gb`](https://huggingface.co/pottokao/minimax-h3-2x16gb) | text-to-video | nvfp4, quantized, license:other |
| 2026-08-03 | 0 | 0 | [`sekkit/MiniMax-H3-INT8-CONVROT`](https://huggingface.co/sekkit/MiniMax-H3-INT8-CONVROT) |  |  |
| 2026-08-06 | 0 | 7 | [`starsfriday/MiniMax-H3-w4a8`](https://huggingface.co/starsfriday/MiniMax-H3-w4a8) | image-text-to-video | comfyui, int4, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 0 | 0 | [`suanyu/MiniMax-H3-Star7-INT8`](https://huggingface.co/suanyu/MiniMax-H3-Star7-INT8) |  |  |
| 2026-08-29 | 0 | 0 | [`szwagros/minimax-h3-w4a8`](https://huggingface.co/szwagros/minimax-h3-w4a8) |  |  |
| 2026-08-09 | 0 | 0 | [`tomas-organization/minimax-h3-production-fp8`](https://huggingface.co/tomas-organization/minimax-h3-production-fp8) |  |  |
| 2026-09-01 | 0 | 0 | [`tomas-organization/minimax-h3-ref2va-cache-int8`](https://huggingface.co/tomas-organization/minimax-h3-ref2va-cache-int8) |  |  |
| 2026-08-03 | 0 | 38 | [`tsolful/Minimax_H3_INT4MixedConvRot`](https://huggingface.co/tsolful/Minimax_H3_INT4MixedConvRot) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 0 | 14 | [`unsloth/MiniMax-H3-FP8`](https://huggingface.co/unsloth/MiniMax-H3-FP8) | image-text-to-video | fp8, int8, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 2 | [`vonkaiser/MiniMax-H3-NVFP4`](https://huggingface.co/vonkaiser/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 0 | 0 | [`xt111/MiniMax-H3-NVFP4`](https://huggingface.co/xt111/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 0 | 0 | [`xvmrjxc/MiniMax-H3-NVFP4`](https://huggingface.co/xvmrjxc/MiniMax-H3-NVFP4) | text-to-video | comfyui, nvfp4, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 0 | [`yitongl/minimax-h3-deltaquant-nvfp4`](https://huggingface.co/yitongl/minimax-h3-deltaquant-nvfp4) |  | deltaquant, nvfp4, quantization, license:other |
| 2026-08-09 | 0 | 0 | [`yitongl/minimax-h3-deltaquant-x0-trajectory`](https://huggingface.co/yitongl/minimax-h3-deltaquant-x0-trajectory) |  | deltaquant, nvfp4, quantization, license:other |
| 2026-08-09 | 0 | 0 | [`yitongl/minimax-h3-nvfp4-lambda-modality`](https://huggingface.co/yitongl/minimax-h3-nvfp4-lambda-modality) |  | svdquant, nvfp4, quantization, license:other |
| 2026-08-12 | 0 | 1 | [`zhenshipo/MiniMax-H3-int8-models`](https://huggingface.co/zhenshipo/MiniMax-H3-int8-models) |  |  |

### 04-GGUF量化

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-07 | 1300040 | 319 | [`unsloth/MiniMax-H3-GGUF`](https://huggingface.co/unsloth/MiniMax-H3-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 804534 | 143 | [`Abiray/MiniMax-H3-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-02 | 510398 | 65 | [`DeepBeepMeep/MiniMax-H3`](https://huggingface.co/DeepBeepMeep/MiniMax-H3) | diffusion-single-file | gguf |
| 2026-08-07 | 257785 | 71 | [`Abiray/MiniMax-H3-Pruned-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-Pruned-GGUF) | image-text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 150840 | 225 | [`realrebelai/MiniMax-H3_GGUFs`](https://huggingface.co/realrebelai/MiniMax-H3_GGUFs) |  | gguf, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:unknown |
| 2026-08-03 | 139973 | 22 | [`leejet/MiniMax-H3-GGUF`](https://huggingface.co/leejet/MiniMax-H3-GGUF) | image-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3 |
| 2026-08-04 | 95351 | 13 | [`joeygambino/MiniMax-H3-encoder-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-encoder-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3 |
| 2026-08-03 | 64893 | 60 | [`molbal/MiniMax-H3-GGUF`](https://huggingface.co/molbal/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 35804 | 33 | [`nif0/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic-H3-GGUF`](https://huggingface.co/nif0/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic-H3-GGUF) |  | gguf, base_model:mradermacher/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic-i1-GGUF, base_model:quantized:mradermacher/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic-i1-GGUF, license:apache-2.0 |
| 2026-08-05 | 31006 | 8 | [`joeygambino/MiniMax-H3-curve-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-curve-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 25836 | 7 | [`pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-GGUF`](https://huggingface.co/pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-GGUF) | image-text-to-text | gguf, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-05 | 25796 | 14 | [`nif0/Qwen3-VL-32B-Instruct-MiniMax-H3-GGUF`](https://huggingface.co/nif0/Qwen3-VL-32B-Instruct-MiniMax-H3-GGUF) |  | gguf, base_model:unsloth/Qwen3-VL-32B-Instruct-GGUF, base_model:quantized:unsloth/Qwen3-VL-32B-Instruct-GGUF, license:apache-2.0 |
| 2026-09-18 | 13566 | 29 | [`Abiray/MiniMax-H3-Singularity-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-Singularity-GGUF) | image-to-video | gguf, comfyui, quantized, base_model:WarmBloodAban/Minimax-h3_Singularity, base_model:quantized:WarmBloodAban/Minimax-h3_Singularity, license:other |
| 2026-09-13 | 12489 | 11 | [`Abiray/10Eros-Max-Hybrid-Beta5-GGUF`](https://huggingface.co/Abiray/10Eros-Max-Hybrid-Beta5-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-04 | 12394 | 24 | [`vantagewithai/MiniMax-H3-comfyUI-GGUF`](https://huggingface.co/vantagewithai/MiniMax-H3-comfyUI-GGUF) | image-text-to-video | gguf, license:other |
| 2026-08-06 | 11682 | 0 | [`convertor/minimax-h3-gguf`](https://huggingface.co/convertor/minimax-h3-gguf) |  | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3 |
| 2026-08-20 | 11040 | 2 | [`PurpleBlazey/Minimax-H3-pruned-GGUF`](https://huggingface.co/PurpleBlazey/Minimax-H3-pruned-GGUF) | image-text-to-video | gguf, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-13 | 7595 | 5 | [`hoidhxd/MiniMax-H3-Hybrid-b25-49-GGUF`](https://huggingface.co/hoidhxd/MiniMax-H3-Hybrid-b25-49-GGUF) | image-to-video | gguf, comfyui, quantized, base_model:smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models, base_model:quantized:smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models |
| 2026-08-04 | 4922 | 8 | [`joeygambino/MiniMax-H3-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-22 | 4572 | 34 | [`joeygambino/MiniMax-H3-x-Z-Image-GGUF`](https://huggingface.co/joeygambino/MiniMax-H3-x-Z-Image-GGUF) | text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 3084 | 0 | [`brurpo/MiniMax-H3-NVFP4-GGUF`](https://huggingface.co/brurpo/MiniMax-H3-NVFP4-GGUF) | image-text-to-video | gguf, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 2967 | 3 | [`woodfireind/MiniMax-H3-GGUF-MiniStack`](https://huggingface.co/woodfireind/MiniMax-H3-GGUF-MiniStack) | text-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 2193 | 7 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-Omni-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-Omni-GGUF) | image-text-to-text | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni |
| 2026-08-10 | 1935 | 0 | [`MarxistLeninist/MiniMax-H3-FL2VA-Pruned-IQ1-GGUF`](https://huggingface.co/MarxistLeninist/MiniMax-H3-FL2VA-Pruned-IQ1-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-06 | 1510 | 0 | [`Raretutor/Qwen3-VL-32B-MiniMax-H3-GGUF`](https://huggingface.co/Raretutor/Qwen3-VL-32B-MiniMax-H3-GGUF) | image-text-to-text | gguf, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-09-16 | 1459 | 6 | [`Abiray/MiniMax-H3-Pruned-Ref-Delta-Fused-GGUF`](https://huggingface.co/Abiray/MiniMax-H3-Pruned-Ref-Delta-Fused-GGUF) | image-to-video | gguf, comfyui, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, base_model:quantized:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, license:other |
| 2026-08-03 | 1420 | 5 | [`FenomAI/MiniMax-H3_GGUFs`](https://huggingface.co/FenomAI/MiniMax-H3_GGUFs) | text-to-video | gguf, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:unknown |
| 2026-08-10 | 1344 | 0 | [`myhuggingbb/MiniMax-H3-GGUF`](https://huggingface.co/myhuggingbb/MiniMax-H3-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-20 | 1312 | 1 | [`eraiko/Qwen3-VL-32B-Ultra-Heretic-Minimax-H3-GGUF`](https://huggingface.co/eraiko/Qwen3-VL-32B-Ultra-Heretic-Minimax-H3-GGUF) |  | gguf |
| 2026-08-19 | 1063 | 3 | [`indhic-ai/MiniMax_H3-Prompt_Rewriter-8B-LORA-Merged-GGUF`](https://huggingface.co/indhic-ai/MiniMax_H3-Prompt_Rewriter-8B-LORA-Merged-GGUF) | image-text-to-text | gguf, lora-merge, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:merge:Qwen/Qwen3-VL-8B-Instruct, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, base_model:merge:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, license:apache-2.0 |
| 2026-08-07 | 1040 | 25 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-GGUF) | gguf | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA |
| 2026-08-18 | 918 | 3 | [`pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-8B-GGUF`](https://huggingface.co/pytraveler/MiniMax-H3-Prompt-Rewriter-LoRA-8B-GGUF) | image-text-to-text | gguf, lora, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, base_model:adapter:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B |
| 2026-08-05 | 690 | 0 | [`FenomAI/Minimax-H3-WAN2GP`](https://huggingface.co/FenomAI/Minimax-H3-WAN2GP) | diffusion-single-file | gguf |
| 2026-09-08 | 653 | 1 | [`alibaybay/MiniMax-H3-Prompt-Rewriter-GGUF`](https://huggingface.co/alibaybay/MiniMax-H3-Prompt-Rewriter-GGUF) | text-generation | gguf, base_model:Qwen/Qwen2.5-Omni-7B, base_model:quantized:Qwen/Qwen2.5-Omni-7B, license:apache-2.0 |
| 2026-08-24 | 526 | 1 | [`hoidhxd/MiniMax-H3-x-Z-Image-hybrid-GGUF`](https://huggingface.co/hoidhxd/MiniMax-H3-x-Z-Image-hybrid-GGUF) | image-to-video | gguf, base_model:hoidhxd/MiniMax-H3-x-Z-Image-hybrid, base_model:quantized:hoidhxd/MiniMax-H3-x-Z-Image-hybrid, license:apache-2.0 |
| 2026-08-24 | 519 | 0 | [`chfm/MiniMax-H3_GGUFs`](https://huggingface.co/chfm/MiniMax-H3_GGUFs) | text-to-video | gguf, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:unknown |
| 2026-08-06 | 517 | 4 | [`EllaPriest45/MinimaxH3_Checkpoints`](https://huggingface.co/EllaPriest45/MinimaxH3_Checkpoints) |  | gguf |
| 2026-08-07 | 469 | 0 | [`on-nurida-mov/My-MiniMax-H3`](https://huggingface.co/on-nurida-mov/My-MiniMax-H3) | diffusion-single-file | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-14 | 383 | 0 | [`Derdisirtlan/MiniMax-H3-GGUF`](https://huggingface.co/Derdisirtlan/MiniMax-H3-GGUF) | image-to-video | gguf, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 212 | 3 | [`EllaPriest45/MinimaxH3_base`](https://huggingface.co/EllaPriest45/MinimaxH3_base) |  | gguf |
| 2026-08-10 | 128 | 0 | [`MarxistLeninist/MiniMax-H3-LowBit-GGUF`](https://huggingface.co/MarxistLeninist/MiniMax-H3-LowBit-GGUF) | image-text-to-video | gguf, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 124 | 0 | [`electroglyph/10Eros_Max_h3_TURBO-hybrid_beta3-GGUF`](https://huggingface.co/electroglyph/10Eros_Max_h3_TURBO-hybrid_beta3-GGUF) |  | gguf |
| 2026-09-25 | 86 | 0 | [`ZawShiShawn/Gestura-MiniMax-H3-VAE-GGUF`](https://huggingface.co/ZawShiShawn/Gestura-MiniMax-H3-VAE-GGUF) | image-to-video | gguf, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-25 | 82 | 0 | [`chfm/10Eros-Max-Hybrid-Beta5-GGUF`](https://huggingface.co/chfm/10Eros-Max-Hybrid-Beta5-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-09-06 | 53 | 0 | [`EllipsesMark/MinimaxH3_Checkpoints`](https://huggingface.co/EllipsesMark/MinimaxH3_Checkpoints) |  | gguf |
| 2026-08-07 | 43 | 0 | [`sandeshrajx/MiniMax-H3-Prompt-Rewriter-LoRA-gguf`](https://huggingface.co/sandeshrajx/MiniMax-H3-Prompt-Rewriter-LoRA-gguf) | text-generation | gguf, lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B, license:apache-2.0 |
| 2026-08-09 | 25 | 1 | [`solphor/MiniMax-H3-Prompt-Rewriter-LoRA-Q8-GGUF`](https://huggingface.co/solphor/MiniMax-H3-Prompt-Rewriter-LoRA-Q8-GGUF) | peft | gguf, lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B |
| 2026-09-27 | 18 | 0 | [`Radha7/MiniMax-H3-Remix-Quantized`](https://huggingface.co/Radha7/MiniMax-H3-Remix-Quantized) |  | gguf |
| 2026-09-25 | 16 | 0 | [`ZawShiShawn/Gestura-MiniMax-H3-REF2VA-Delta`](https://huggingface.co/ZawShiShawn/Gestura-MiniMax-H3-REF2VA-Delta) | image-to-video | gguf, quantized, base_model:ChrisColeTech/minimax-h3-turbo-GGUF, base_model:quantized:ChrisColeTech/minimax-h3-turbo-GGUF, license:other |
| 2026-08-06 | 8 | 0 | [`radarer168/MinimaxH3_base`](https://huggingface.co/radarer168/MinimaxH3_base) |  | gguf |
| 2026-08-06 | 5 | 0 | [`radarer168/MinimaxH3_Checkpoints`](https://huggingface.co/radarer168/MinimaxH3_Checkpoints) |  | gguf |
| 2026-08-10 | 0 | 0 | [`MarxistLeninist/MiniMax-H3-IQ1_M-GGUF`](https://huggingface.co/MarxistLeninist/MiniMax-H3-IQ1_M-GGUF) |  |  |
| 2026-08-08 | 0 | 0 | [`The-frizzy1/Minimax-h3-gguf-workflow`](https://huggingface.co/The-frizzy1/Minimax-h3-gguf-workflow) |  |  |
| 2026-08-03 | 0 | 0 | [`liewge/MinimaxH3-GGUF-Quant`](https://huggingface.co/liewge/MinimaxH3-GGUF-Quant) |  | license:apache-2.0 |

### 05-Turbo少步加速

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-07 | 1536536 | 1012 | [`lightx2v/Minimax-h3-Turbo`](https://huggingface.co/lightx2v/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-29 | 764218 | 231 | [`MATLOWAI/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/MATLOWAI/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-06 | 218367 | 481 | [`drbaph/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/drbaph/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, turbo, pruned-model, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-05 | 215009 | 1037 | [`larryvrh/MiniMax-H3-Turbo-Lora`](https://huggingface.co/larryvrh/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-15 | 30487 | 12 | [`PulpCut/MiniMax-H3-Ref2VA-Turbo-INT8-ConvRot`](https://huggingface.co/PulpCut/MiniMax-H3-Ref2VA-Turbo-INT8-ConvRot) | minimax-h3 | int8, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 20725 | 56 | [`Robert1212star/TaoMate-H3-3Step-ComfyUI`](https://huggingface.co/Robert1212star/TaoMate-H3-3Step-ComfyUI) | minimax-h3 | comfyui, lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 19873 | 273 | [`Viggle/Viggle-Animate`](https://huggingface.co/Viggle/Viggle-Animate) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-19 | 15979 | 29 | [`drbaph/Hyperflow-Comfyui`](https://huggingface.co/drbaph/Hyperflow-Comfyui) | image-text-to-video | lora, comfyui, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 13899 | 35 | [`CZMartin22/TaoMate-H3-3step-ComfyUI`](https://huggingface.co/CZMartin22/TaoMate-H3-3step-ComfyUI) | image-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 13206 | 20 | [`ChrisColeTech/minimax-h3-turbo-GGUF`](https://huggingface.co/ChrisColeTech/minimax-h3-turbo-GGUF) | text-to-video | gguf, quantized, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 12339 | 49 | [`Abiray/MiniMax-H3-Turbo-Lora-Pruned-ComfyUI`](https://huggingface.co/Abiray/MiniMax-H3-Turbo-Lora-Pruned-ComfyUI) | image-text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-17 | 6584 | 94 | [`videorebirth/hyperflow`](https://huggingface.co/videorebirth/hyperflow) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 5472 | 2 | [`Jackxuanxuan/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/Jackxuanxuan/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-13 | 5340 | 3 | [`molbal/MiniMax-H3-Turbo-GGUF`](https://huggingface.co/molbal/MiniMax-H3-Turbo-GGUF) | image-to-video | gguf, comfyui, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-12 | 4683 | 9 | [`rzgar/minimax-h3_ref2va_8Step_motion_enhancer`](https://huggingface.co/rzgar/minimax-h3_ref2va_8Step_motion_enhancer) | image-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-11 | 3455 | 7 | [`vladmandic/MiniMax-H3-Turbo-LoRA`](https://huggingface.co/vladmandic/MiniMax-H3-Turbo-LoRA) | text-to-video | turbo, lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-08 | 3147 | 2 | [`chfm/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/chfm/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-06 | 3042 | 12 | [`infosave/MiniMax-H3-Turbo-cmf`](https://huggingface.co/infosave/MiniMax-H3-Turbo-cmf) | text-to-video | base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-30 | 2674 | 0 | [`ulifisherde/MiniMax-H3-Turbo-Lora-Pruned-Fixed`](https://huggingface.co/ulifisherde/MiniMax-H3-Turbo-Lora-Pruned-Fixed) | text-to-video | turbo, lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-13 | 2636 | 5 | [`PulpCut/MiniMax-H3-Turbo-INT8-ConvRot`](https://huggingface.co/PulpCut/MiniMax-H3-Turbo-INT8-ConvRot) | minimax-h3 | int8, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 2064 | 35 | [`JOKER141/BUNNY_H3_Conditioning_Bridge`](https://huggingface.co/JOKER141/BUNNY_H3_Conditioning_Bridge) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-25 | 2049 | 2 | [`Rkss/Minimax_h3_fl2v_lightx2v_turbo_4to8step_768p_v4_step600_dareties_native`](https://huggingface.co/Rkss/Minimax_h3_fl2v_lightx2v_turbo_4to8step_768p_v4_step600_dareties_native) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-06 | 2023 | 8 | [`InstantX/MiniMax-H3-Turbo-Lora-Diffusers`](https://huggingface.co/InstantX/MiniMax-H3-Turbo-Lora-Diffusers) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-18 | 1497 | 0 | [`chfm/TaoMate-H3-3Step-ComfyUI`](https://huggingface.co/chfm/TaoMate-H3-3Step-ComfyUI) | minimax-h3 | comfyui, lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 1236 | 0 | [`DARK-MING/MiniMax-H3-Turbo-Lora`](https://huggingface.co/DARK-MING/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-30 | 1167 | 2 | [`Halpak/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/Halpak/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, turbo, pruned-model, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-07 | 1055 | 113 | [`TaoLiveAIGC/TaoMate-H3`](https://huggingface.co/TaoLiveAIGC/TaoMate-H3) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-18 | 981 | 1 | [`cgc-0521/minimax-h3-fused-turbo-int8-convrot`](https://huggingface.co/cgc-0521/minimax-h3-fused-turbo-int8-convrot) | image-text-to-video | comfyui, int8, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, base_model:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:merge:diffusers-modular/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024, base_model:xmarre/MiniMax-H3-Pruned-Ref-Delta-Fused-r1024-ComfyUI, … |
| 2026-08-23 | 558 | 0 | [`chfm/MiniMax-H3-Turbo-Lora`](https://huggingface.co/chfm/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-25 | 486 | 31 | [`Veda-Sparse/Minimax-H3-T2VA-Veda-8NFE-600Step-Preview`](https://huggingface.co/Veda-Sparse/Minimax-H3-T2VA-Veda-8NFE-600Step-Preview) | text-to-video | fp8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 294 | 2 | [`taurusduan/Minimax-h3-Turbo`](https://huggingface.co/taurusduan/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-31 | 266 | 0 | [`mu1998/MiniMax-H3-Turbo-Lora`](https://huggingface.co/mu1998/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-10 | 254 | 0 | [`CurioSeaLab/Minimax-h3-Turbo`](https://huggingface.co/CurioSeaLab/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-20 | 210 | 0 | [`mimimi2811/MiniMax-H3-Turbo-Lora`](https://huggingface.co/mimimi2811/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-30 | 200 | 0 | [`HAOOOOOOO51/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_pruned`](https://huggingface.co/HAOOOOOOO51/Minimax_h3_fl2v_lightx2v_turbo_4to8step_v0.1-v1.0_768p_v4_step600_dareties_fro095_pruned) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-31 | 181 | 1 | [`treydonovan/Minimax-h3-Turbo`](https://huggingface.co/treydonovan/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-25 | 176 | 0 | [`Exmanq/MiniMax-H3-Turbo-Lora`](https://huggingface.co/Exmanq/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-14 | 113 | 11 | [`Asirus/TaoMate_H3_3_Step_LoRA`](https://huggingface.co/Asirus/TaoMate_H3_3_Step_LoRA) | text-to-video | comfyui, lora, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 102 | 0 | [`EllipsesMark/larryvrh-Turbo-Lora`](https://huggingface.co/EllipsesMark/larryvrh-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-23 | 84 | 0 | [`EllipsesMark/Minimax-h3-Turbo`](https://huggingface.co/EllipsesMark/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-07 | 65 | 0 | [`Drakonff1/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/Drakonff1/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, turbo, pruned-model, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-05 | 59 | 0 | [`pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-SVDQuant-vLLM-Omni`](https://huggingface.co/pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-SVDQuant-vLLM-Omni) | image-to-video | turbo, nvfp4, svdquant, license:apache-2.0 |
| 2026-08-19 | 51 | 0 | [`kai2336/Minimax-h3-Turbo`](https://huggingface.co/kai2336/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-31 | 50 | 0 | [`r3lax/MiniMax-H3-Turbo-cmf`](https://huggingface.co/r3lax/MiniMax-H3-Turbo-cmf) | text-to-video | base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-25 | 48 | 0 | [`Exmanq/Minimax-h3-Turbo`](https://huggingface.co/Exmanq/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-18 | 43 | 2 | [`Asirus/minimax_h3_fl2va_pruned_int8_convrot_taomate_8_step`](https://huggingface.co/Asirus/minimax_h3_fl2va_pruned_int8_convrot_taomate_8_step) | custom | int8, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3 |
| 2026-09-28 | 34 | 0 | [`fbjr/h3-mutant-distill`](https://huggingface.co/fbjr/h3-mutant-distill) | text-to-video | comfyui, lora, base_model:Beidouqixing/minimax-h3-4step-lora-flashgen, base_model:adapter:Beidouqixing/minimax-h3-4step-lora-flashgen, license:other |
| 2026-08-08 | 20 | 1 | [`Momoking/Minimax-h3-Turbo`](https://huggingface.co/Momoking/Minimax-h3-Turbo) | image-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-23 | 4 | 0 | [`pdmd2026/pdmd_2NFE_lora`](https://huggingface.co/pdmd2026/pdmd_2NFE_lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-19 | 0 | 2 | [`Akilad/minimax_h3_taomate_3step_clarity_extreme_no_attn`](https://huggingface.co/Akilad/minimax_h3_taomate_3step_clarity_extreme_no_attn) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-11 | 0 | 1 | [`Alberto454/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/Alberto454/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, pruned-model, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-15 | 0 | 0 | [`Asirus/MiniMax-H3-TaoMate-3Step-Fused-BF16`](https://huggingface.co/Asirus/MiniMax-H3-TaoMate-3Step-Fused-BF16) |  |  |
| 2026-08-09 | 0 | 1 | [`BennyDaBall/MiniMax-H3-Workflows`](https://huggingface.co/BennyDaBall/MiniMax-H3-Workflows) | text-to-video | comfyui, turbo, lora, license:apache-2.0 |
| 2026-08-21 | 0 | 0 | [`Codes4Fun/lightx2v_MiniMax-H3-Prompt-Rewriter-8B_ComfyUI`](https://huggingface.co/Codes4Fun/lightx2v_MiniMax-H3-Prompt-Rewriter-8B_ComfyUI) |  | base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:merge:Qwen/Qwen3-VL-8B-Instruct, base_model:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B, base_model:merge:lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B |
| 2026-08-10 | 0 | 7 | [`DarkRomeo88/MiniMax-H3-turbo-lora-comfyui`](https://huggingface.co/DarkRomeo88/MiniMax-H3-turbo-lora-comfyui) | image-text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-06 | 0 | 11 | [`HardGravy2/Minimax_H3_FLF_HardGravy_6_Step_Turbo_Merge`](https://huggingface.co/HardGravy2/Minimax_H3_FLF_HardGravy_6_Step_Turbo_Merge) |  | comfyui, license:other |
| 2026-08-06 | 0 | 14 | [`Mamad8/MiniMaxH3_R2V-PDD-Turbo-LoRA-Mamad8`](https://huggingface.co/Mamad8/MiniMaxH3_R2V-PDD-Turbo-LoRA-Mamad8) |  |  |
| 2026-08-08 | 0 | 4 | [`Momoking/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/Momoking/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, pruned-model, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-18 | 0 | 0 | [`NaukNauk/minimax-h3-turbo-fl2va-merged`](https://huggingface.co/NaukNauk/minimax-h3-turbo-fl2va-merged) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-17 | 0 | 0 | [`NaukNauk/minimax-h3-turbo-merged`](https://huggingface.co/NaukNauk/minimax-h3-turbo-merged) |  |  |
| 2026-09-04 | 0 | 0 | [`NaukNauk/minimax-h3-turbo-ref2va-merged`](https://huggingface.co/NaukNauk/minimax-h3-turbo-ref2va-merged) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 0 | 42 | [`QrusherZA/H3_Turbo_ComfyUI`](https://huggingface.co/QrusherZA/H3_Turbo_ComfyUI) |  |  |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-dmd-fl2va-8step-turbo-pruned.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-dmd-fl2va-8step-turbo-pruned.safetensors-lora) |  | comfyui, lora |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-dmd-ref2va-8step-turbo-pruned.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-dmd-ref2va-8step-turbo-pruned.safetensors-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-8step-motion-enhancer-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-8step-motion-enhancer-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 1 | [`RunningHubAI/rh-minimax-h3-fl2v-lightx2v-turbo-4step-v0.1-comfy-resized-avg-rank-21-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-lightx2v-turbo-4step-v0.1-comfy-resized-avg-rank-21-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-lightx2v-turbo-4step-v0.1-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-lightx2v-turbo-4step-v0.1-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v0.1-768p-sla-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v0.1-768p-sla-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v0.1-comfyui-t8-convert-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v0.1-comfyui-t8-convert-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.0-768p-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.0-768p-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.1-768p-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.1-768p-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.2-768p-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.2-768p-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.2-768p-comfyui-resized-avg-rank-64-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-4step-v1.2-768p-comfyui-resized-avg-rank-64-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 2 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-768p-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-768p-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-29 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2va-bf16-turbo-multistep-fro099-r144-pruned.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2va-bf16-turbo-multistep-fro099-r144-pruned.safetensors-lora) |  | comfyui, lora |
| 2026-09-25 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-hyperflow-8step-v1.0-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-hyperflow-8step-v1.0-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 3 | [`RunningHubAI/rh-minimax-h3-ref2v-turbo-4step-v0.1-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2v-turbo-4step-v0.1-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-comfyui-bf16-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-comfyui-bf16-lora) |  | comfyui, lora |
| 2026-09-20 | 0 | 2 | [`RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-09-25 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2v-turbo-8step-v1.0-768p-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-ref2va-turbo-int8-convrot-unet`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2va-turbo-int8-convrot-unet) | text-to-video | comfyui |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-4-comfyui-t8-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-4-comfyui-t8-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-4step-ckpt500-comfyui-t8-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-4step-ckpt500-comfyui-t8-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-4step-ckpt500-converted.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-4step-ckpt500-converted.safetensors-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-4step-ckpt850-t8-comfyui-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-4step-ckpt850-t8-comfyui-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-v4-step600-comfyui-t8-convert-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-v4-step600-comfyui-t8-convert-lora) |  | comfyui, lora |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-v4-step600-ema-comfyui-b-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-v4-step600-ema-comfyui-b-lora) |  | comfyui, lora |
| 2026-09-23 | 0 | 1 | [`RunningHubAI/rh-minimax-h3-turbo-v4-step600-ema-dasiwaref2vahybridv1-0-curveproj1025-compat-v001-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-v4-step600-ema-dasiwaref2vahybridv1-0-curveproj1025-compat-v001-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 1 | [`RunningHubAI/rh-minimaxh3-turbo-shenanigans-lora`](https://huggingface.co/RunningHubAI/rh-minimaxh3-turbo-shenanigans-lora) |  | comfyui, lora |
| 2026-09-27 | 0 | 0 | [`RunningHubAI/rh-taomate-h3-3step-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-taomate-h3-3step-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 1 | [`RunningHubAI/rh-taomate-h3-step3000-comfyui-bf16.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-taomate-h3-step3000-comfyui-bf16.safetensors-lora) |  | comfyui, lora |
| 2026-08-07 | 0 | 4 | [`SanDiegoDude/H3-Turbo-6-Step-LoRA-Comfy`](https://huggingface.co/SanDiegoDude/H3-Turbo-6-Step-LoRA-Comfy) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-07 | 0 | 0 | [`Scorpio1111/MiniMax-H3-Turbo-Lora`](https://huggingface.co/Scorpio1111/MiniMax-H3-Turbo-Lora) |  |  |
| 2026-08-16 | 0 | 7 | [`SpXMerlin1D/MiniMaxH3-CondBridge-Qwen3.5-4B`](https://huggingface.co/SpXMerlin1D/MiniMaxH3-CondBridge-Qwen3.5-4B) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-09-04 | 0 | 2 | [`TechnoBaptist/Viggle-Animate`](https://huggingface.co/TechnoBaptist/Viggle-Animate) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 0 | 18 | [`TenStrip/MinimaxH3-Turbo_Shenanigans`](https://huggingface.co/TenStrip/MinimaxH3-Turbo_Shenanigans) |  |  |
| 2026-08-27 | 0 | 0 | [`Wesley1234/Minimax-H3-Dasiwa-V1-Hybird-4steps`](https://huggingface.co/Wesley1234/Minimax-H3-Dasiwa-V1-Hybird-4steps) |  |  |
| 2026-08-27 | 0 | 0 | [`Wesley1234/minimax-h3-4step-turbo-loras-comfyui-exp`](https://huggingface.co/Wesley1234/minimax-h3-4step-turbo-loras-comfyui-exp) |  |  |
| 2026-08-27 | 0 | 0 | [`Wesley1234/minimax_h3_fl2v_turbo_4step_v0.1_comfyui_alpha8-T8-convert`](https://huggingface.co/Wesley1234/minimax_h3_fl2v_turbo_4step_v0.1_comfyui_alpha8-T8-convert) |  |  |
| 2026-08-07 | 0 | 0 | [`amirjan122222/MiniMax-H3-Turbo-Lora`](https://huggingface.co/amirjan122222/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-07 | 0 | 0 | [`asadkhan89/Minimax-h3-Turbo-SLA`](https://huggingface.co/asadkhan89/Minimax-h3-Turbo-SLA) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-10 | 0 | 0 | [`cokeadrink/minimax-h3-fl2va-bf16-8step`](https://huggingface.co/cokeadrink/minimax-h3-fl2va-bf16-8step) |  |  |
| 2026-09-01 | 0 | 0 | [`cokeadrink/minimax-h3-fl2va-lightning-4step`](https://huggingface.co/cokeadrink/minimax-h3-fl2va-lightning-4step) |  |  |
| 2026-08-10 | 0 | 0 | [`dadix4e/minimax_h3_turbo_lora_rank256_needs_training`](https://huggingface.co/dadix4e/minimax_h3_turbo_lora_rank256_needs_training) |  | lora, turbo, license:gpl-2.0 |
| 2026-09-10 | 0 | 0 | [`developerjeremylive/Viggle-Animate-etheroi`](https://huggingface.co/developerjeremylive/Viggle-Animate-etheroi) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 0 | 0 | [`greenslime/MiniMax-H3-Turbo-Lora-ComfyUI`](https://huggingface.co/greenslime/MiniMax-H3-Turbo-Lora-ComfyUI) | text-to-video | lora, comfyui, pruned-model, turbo, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-08 | 0 | 0 | [`inflected111/MiniMax-H3-Turbo-Lora`](https://huggingface.co/inflected111/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-10 | 0 | 66 | [`joyfox/MiniMax-H3-Turbo`](https://huggingface.co/joyfox/MiniMax-H3-Turbo) | image-to-video | comfyui, lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-08-11 | 0 | 0 | [`lasdkjf/MiniMax-H3-Turbo-Lora`](https://huggingface.co/lasdkjf/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-20 | 0 | 108 | [`lightx2v/Minimax-h3-Turbo-SLA`](https://huggingface.co/lightx2v/Minimax-h3-Turbo-SLA) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-05 | 0 | 1 | [`pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-rotated-T1`](https://huggingface.co/pottokao/MiniMax-H3-FL2VA-turbo-4step-v1.2-768p-NVFP4-rotated-T1) | image-to-video | comfyui, turbo, nvfp4, license:apache-2.0 |
| 2026-08-15 | 0 | 0 | [`rb93452/MiniMaxAI.MiniMax-H3-Turbo-Lora`](https://huggingface.co/rb93452/MiniMaxAI.MiniMax-H3-Turbo-Lora) |  | license:apache-2.0 |
| 2026-08-12 | 0 | 0 | [`seahorse12/MiniMax-H3-Turbo-Lora`](https://huggingface.co/seahorse12/MiniMax-H3-Turbo-Lora) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-10 | 0 | 0 | [`slmonker/minimax-h3-fl2v-turbo-comfyui-fp8`](https://huggingface.co/slmonker/minimax-h3-fl2v-turbo-comfyui-fp8) |  |  |
| 2026-08-10 | 0 | 0 | [`suryatmodulus/MiniMax-H3-Turbo`](https://huggingface.co/suryatmodulus/MiniMax-H3-Turbo) | image-to-video | comfyui, lora |
| 2026-08-23 | 0 | 10 | [`t8star/Minimax-H3-Dasiwa-V1-Hybird-4steps`](https://huggingface.co/t8star/Minimax-H3-Dasiwa-V1-Hybird-4steps) |  |  |
| 2026-08-06 | 0 | 61 | [`t8star/minimax-h3-4step-turbo-loras-comfyui-exp`](https://huggingface.co/t8star/minimax-h3-4step-turbo-loras-comfyui-exp) |  |  |
| 2026-08-07 | 0 | 10 | [`t8star/minimax_h3_fl2v_turbo_4step_v0.1_comfyui_alpha8-T8-convert`](https://huggingface.co/t8star/minimax_h3_fl2v_turbo_4step_v0.1_comfyui_alpha8-T8-convert) |  |  |
| 2026-09-04 | 0 | 1 | [`t8star/minimax_h3_fl2v_turbo_8step_v1.0_768p_FeiHouRemix_v0.6_compat_v001_T8`](https://huggingface.co/t8star/minimax_h3_fl2v_turbo_8step_v1.0_768p_FeiHouRemix_v0.6_compat_v001_T8) |  |  |
| 2026-09-04 | 0 | 4 | [`t8star/minimax_h3_turbo_v4_step600_ema_DasiwaREF2VAHybridV1_0_curveproj1025_compat_v001`](https://huggingface.co/t8star/minimax_h3_turbo_v4_step600_ema_DasiwaREF2VAHybridV1_0_curveproj1025_compat_v001) |  |  |
| 2026-08-27 | 0 | 0 | [`wt5719001/Minimax-H3-Dasiwa-V1-Hybird-4steps`](https://huggingface.co/wt5719001/Minimax-H3-Dasiwa-V1-Hybird-4steps) |  |  |

### 06-加速LoRA-Acc

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-26 | 83366 | 256 | [`alibaba-pai/MiniMax-H3-Acc-LoRAs`](https://huggingface.co/alibaba-pai/MiniMax-H3-Acc-LoRAs) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 40399 | 79 | [`aptech0081/MiniMax-H3-Acc-LoRAs-ComfyUI`](https://huggingface.co/aptech0081/MiniMax-H3-Acc-LoRAs-ComfyUI) | text-to-video | comfyui, lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-29 | 34645 | 8 | [`t8star/Minimax-H3-Super-Acceleration-Comfy`](https://huggingface.co/t8star/Minimax-H3-Super-Acceleration-Comfy) | minimax-h3 | comfyui |
| 2026-08-29 | 7925 | 6 | [`fbjr/MiniMax-H3-Acc-LoRAs-sidecar`](https://huggingface.co/fbjr/MiniMax-H3-Acc-LoRAs-sidecar) | text-to-video | comfyui, lora, base_model:alibaba-pai/MiniMax-H3-Acc-LoRAs, base_model:adapter:alibaba-pai/MiniMax-H3-Acc-LoRAs, license:other |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2va-acc-8step-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2va-acc-8step-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2va-acc-8step-pruned-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2va-acc-8step-pruned-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-ref2va-acc-8step-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2va-acc-8step-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-ref2va-acc-8step-pruned-comfy.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-ref2va-acc-8step-pruned-comfy.safetensors-lora) |  | comfyui, lora |
| 2026-08-27 | 0 | 1 | [`Wesley1234/MiniMax-H3-Acc-8Step-comfy`](https://huggingface.co/Wesley1234/MiniMax-H3-Acc-8Step-comfy) |  |  |
| 2026-09-14 | 0 | 0 | [`coolthor/H3-Super-Acceleration-Turing`](https://huggingface.co/coolthor/H3-Super-Acceleration-Turing) | image-to-video | comfyui, int8, quantized, license:other |
| 2026-08-26 | 0 | 5 | [`t8star/MiniMax-H3-Acc-8Step-comfy`](https://huggingface.co/t8star/MiniMax-H3-Acc-8Step-comfy) |  |  |

### 07-FastH3蒸馏

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-27 | 847908 | 316 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 273255 | 122 | [`FastVideo/FastVideo-FastH3-Comfy`](https://huggingface.co/FastVideo/FastVideo-FastH3-Comfy) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 24424 | 22 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-LoRA`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-LoRA) | minimax-h3 | lora, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 21987 | 18 | [`barelymining/ComfyUI-MiniMax-H3-FastVideo`](https://huggingface.co/barelymining/ComfyUI-MiniMax-H3-FastVideo) | diffusers | comfyui, lora, fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:adapter:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-16 | 10291 | 23 | [`realrebelai/FastH3-V2_GGUFs`](https://huggingface.co/realrebelai/FastH3-V2_GGUFs) | text-to-video | comfyui, gguf, fasth3, quantization, base_model:FastVideo/FastVideo-FastH3-8-Step-V2, base_model:quantized:FastVideo/FastVideo-FastH3-8-Step-V2, license:other |
| 2026-08-23 | 7460 | 7 | [`drozbay/MiniMax-H3-FastH3-Preview-LoRA`](https://huggingface.co/drozbay/MiniMax-H3-FastH3-Preview-LoRA) | minimax-h3 | lora, comfyui, base_model:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, base_model:adapter:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, license:other |
| 2026-09-05 | 5060 | 0 | [`zhurrka/FastVideo-FastH3-4-step-Preview-v1-LoRA`](https://huggingface.co/zhurrka/FastVideo-FastH3-4-step-Preview-v1-LoRA) | minimax-h3 | lora, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 3104 | 19 | [`realrebelai/FastH3_GGUFs`](https://huggingface.co/realrebelai/FastH3_GGUFs) | image-to-video | gguf, quantized, comfyui, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:quantized:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-04 | 3056 | 113 | [`FastVideo/FastVideo-FastH3-8-Step-V2`](https://huggingface.co/FastVideo/FastVideo-FastH3-8-Step-V2) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-02 | 2285 | 4 | [`vantagewithai/FastVideo-FastH3-8-Step-V2-ComfyUI-GGUF`](https://huggingface.co/vantagewithai/FastVideo-FastH3-8-Step-V2-ComfyUI-GGUF) | text-to-video | gguf, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 1263 | 1 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1900`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1900) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-23 | 1157 | 32 | [`FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2`](https://huggingface.co/FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-07 | 994 | 2 | [`zerubroberts/MiniMax-H3-FastH3-v1-dense-datafree-ComfyUI`](https://huggingface.co/zerubroberts/MiniMax-H3-FastH3-v1-dense-datafree-ComfyUI) | minimax-h3 | lora, comfyui, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-27 | 846 | 2 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-15 | 788 | 7 | [`rzgar/FastVideo-FastH3-Motion-Enhanced-Comfy`](https://huggingface.co/rzgar/FastVideo-FastH3-Motion-Enhanced-Comfy) | image-to-video | base_model:FastVideo/FastVideo-FastH3-Comfy, base_model:finetune:FastVideo/FastVideo-FastH3-Comfy, license:other |
| 2026-08-29 | 397 | 0 | [`Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-Q8`](https://huggingface.co/Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-Q8) | text-to-video | mlx, license:other |
| 2026-09-14 | 317 | 0 | [`yniw/MiniMax-H3-mmh3`](https://huggingface.co/yniw/MiniMax-H3-mmh3) | text-to-video | fasth3, lora, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:adapter:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-08-29 | 299 | 1 | [`Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-BF16`](https://huggingface.co/Sawfwair/MiniMax-H3-FastH3-VSA-DataFree-MLX-BF16) | text-to-video | mlx, fasth3, license:other |
| 2026-09-25 | 294 | 0 | [`ZawShiShawn/Gestura-FastH3-GGUF`](https://huggingface.co/ZawShiShawn/Gestura-FastH3-GGUF) | text-to-video | gguf, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:quantized:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-11 | 70 | 0 | [`KyleNeverGivesUp/FastH3-text-encoder-nvfp4`](https://huggingface.co/KyleNeverGivesUp/FastH3-text-encoder-nvfp4) | fastvideo | fasth3, nvfp4, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:quantized:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-25 | 23 | 0 | [`ZawShiShawn/Gestura-FastH3-LiteRT`](https://huggingface.co/ZawShiShawn/Gestura-FastH3-LiteRT) | text-to-video | quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-08-27 | 20 | 2 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1300`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-Synthetic-Step1300) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-23 | 14 | 0 | [`gurujack/splashspeed-FastH3-8-Step-V2`](https://huggingface.co/gurujack/splashspeed-FastH3-8-Step-V2) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 13 | 3 | [`FastVideo/FastVideo-Minimax-FastH3-Preview-v0.1`](https://huggingface.co/FastVideo/FastVideo-Minimax-FastH3-Preview-v0.1) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-22 | 12 | 0 | [`FanzCEO/FastVideo-FastH3-8-Step-V2`](https://huggingface.co/FanzCEO/FastVideo-FastH3-8-Step-V2) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 3 | 0 | [`KyleNeverGivesUp/FastH3-Preview-v0.2-r16`](https://huggingface.co/KyleNeverGivesUp/FastH3-Preview-v0.2-r16) | text-to-video | fasth3, base_model:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, base_model:finetune:FastVideo/FastVideo-Minimax-FastH3-Preview-v0.2, license:other |
| 2026-09-01 | 0 | 4 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4) | text-to-video | mlx, fasth3, quantized, int4, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-01 | 0 | 0 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT6`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT6) | text-to-video | mlx, fasth3, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-09-01 | 0 | 3 | [`FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT8`](https://huggingface.co/FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT8) | text-to-video | mlx, fasth3, quantized, int8, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-08-29 | 0 | 2 | [`KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16`](https://huggingface.co/KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16) | text-to-video | fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-24 | 0 | 0 | [`KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16-int8`](https://huggingface.co/KyleNeverGivesUp/FastH3-4-step-Preview-v1-r16-int8) | text-to-video | fasth3, int8, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:quantized:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-02 | 0 | 1 | [`LoboForge/minimax-h3-fastvideo-nvfp4`](https://huggingface.co/LoboForge/minimax-h3-fastvideo-nvfp4) | text-to-video | comfyui, fasth3, nvfp4, quantization, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-01 | 0 | 0 | [`MaximMerk/fasth3-v0.2-int8-convrot`](https://huggingface.co/MaximMerk/fasth3-v0.2-int8-convrot) |  |  |
| 2026-09-02 | 0 | 0 | [`MrMofer/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4`](https://huggingface.co/MrMofer/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree-MLX-INT4) | text-to-video | mlx, fasth3, quantized, int4, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-Dense-DataFree, license:other |
| 2026-08-30 | 0 | 5 | [`PulpCut/FastH3-VSA-INT8-ConvRot`](https://huggingface.co/PulpCut/FastH3-VSA-INT8-ConvRot) | text-to-video | int8, fasth3, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-16 | 0 | 1 | [`QrusherZA/FastH3_V2-LoRA-Experimental`](https://huggingface.co/QrusherZA/FastH3_V2-LoRA-Experimental) |  |  |
| 2026-08-28 | 0 | 0 | [`TechnoBaptist/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree`](https://huggingface.co/TechnoBaptist/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-01 | 0 | 1 | [`kevin-mi/FastH3-4step-Preview-overlay`](https://huggingface.co/kevin-mi/FastH3-4step-Preview-overlay) | sglang-diffusion | fasth3 |
| 2026-09-04 | 0 | 1 | [`lpiao3825/FastH3-ComfyUI-Community-Workflow`](https://huggingface.co/lpiao3825/FastH3-ComfyUI-Community-Workflow) |  |  |
| 2026-09-02 | 0 | 5 | [`pottokao/MiniMax-H3-FastH3-NVFP4-rotated`](https://huggingface.co/pottokao/MiniMax-H3-FastH3-NVFP4-rotated) | text-to-video | comfyui, nvfp4, quantization, fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 0 | 0 | [`sarthakraj9032/Futhelavideogenerator`](https://huggingface.co/sarthakraj9032/Futhelavideogenerator) | text-to-video | fasth3, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 0 | 0 | [`skx618/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree-NVFP4`](https://huggingface.co/skx618/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree-NVFP4) | text-to-video | fasth3, nvfp4, quantized, base_model:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, base_model:finetune:FastVideo/FastVideo-FastH3-4-step-Preview-v1-VSA-DataFree, license:other |
| 2026-09-16 | 0 | 3 | [`skx618/FastVideo-FastH3-8-Step-V2-NVFP4`](https://huggingface.co/skx618/FastVideo-FastH3-8-Step-V2-NVFP4) | text-to-video | fasth3, nvfp4, quantized, base_model:FastVideo/FastVideo-FastH3-8-Step-V2, base_model:finetune:FastVideo/FastVideo-FastH3-8-Step-V2, license:other |
| 2026-09-17 | 0 | 0 | [`vanch007/FastVideo-FastH3-8-Step-V2-MLX-INT6`](https://huggingface.co/vanch007/FastVideo-FastH3-8-Step-V2-MLX-INT6) | text-to-video | mlx, license:apache-2.0 |
| 2026-09-17 | 0 | 0 | [`vanch007/FastVideo-FastH3-8-Step-V2-MLX-INT8`](https://huggingface.co/vanch007/FastVideo-FastH3-8-Step-V2-MLX-INT8) | text-to-video | mlx, license:apache-2.0 |

### 08-ControlNet控制

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-24 | 13023 | 195 | [`alibaba-pai/MiniMax-H3-Fun-Controlnet-Union`](https://huggingface.co/alibaba-pai/MiniMax-H3-Fun-Controlnet-Union) | text-to-video | controlnet, license:other |
| 2026-09-22 | 7049 | 53 | [`alibaba-pai/MiniMax-H3-Fun-Controlnet-Union-2.0`](https://huggingface.co/alibaba-pai/MiniMax-H3-Fun-Controlnet-Union-2.0) | text-to-video | controlnet, controlnet-union, license:other |
| 2026-09-10 | 1087 | 2 | [`berryber09/MiniMax-H3-Fun-Controlnet-Union-w4a8`](https://huggingface.co/berryber09/MiniMax-H3-Fun-Controlnet-Union-w4a8) | minimax-h3 | controlnet, comfyui, quantized, base_model:alibaba-pai/MiniMax-H3-Fun-Controlnet-Union, base_model:adapter:alibaba-pai/MiniMax-H3-Fun-Controlnet-Union, license:other |
| 2026-08-24 | 39 | 0 | [`TechnoBaptist/MiniMax-H3-Fun-Controlnet-Union`](https://huggingface.co/TechnoBaptist/MiniMax-H3-Fun-Controlnet-Union) | text-to-video | controlnet, license:other |
| 2026-08-24 | 0 | 0 | [`GJuarez67/MiniMax-H3-Fun-Controlnet-Union-Demo`](https://huggingface.co/GJuarez67/MiniMax-H3-Fun-Controlnet-Union-Demo) | video-to-video | controlnet |
| 2026-08-06 | 0 | 127 | [`javawock7618/comfy-MiniMax-H3-workflows`](https://huggingface.co/javawock7618/comfy-MiniMax-H3-workflows) | image-to-video | comfyui, controlnet, controlnet-union, int8, turbo-lora, quantization |

### 09-风格题材LoRA

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-10 | 72968 | 434 | [`fal/MiniMax-H3-Realism-People-LoRA`](https://huggingface.co/fal/MiniMax-H3-Realism-People-LoRA) | image-text-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-06 | 52170 | 313 | [`Alissonerdx/Minimax-H3-ComfyUI`](https://huggingface.co/Alissonerdx/Minimax-H3-ComfyUI) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 27601 | 122 | [`Jojocodex/minimax-h3-spatial-physics-lora`](https://huggingface.co/Jojocodex/minimax-h3-spatial-physics-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 20849 | 73 | [`Jojocodex/minimax-h3-Camera-Motion-lora`](https://huggingface.co/Jojocodex/minimax-h3-Camera-Motion-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-08 | 18037 | 5 | [`rzgar/minimax_h3_fl2v_lightx2v_4step_int8-convrot_comfy`](https://huggingface.co/rzgar/minimax_h3_fl2v_lightx2v_4step_int8-convrot_comfy) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-30 | 17630 | 49 | [`Jojocodex/wushu-action-v7-minimax-h3-fl2va-ref2va-lora`](https://huggingface.co/Jojocodex/wushu-action-v7-minimax-h3-fl2va-ref2va-lora) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-04 | 15034 | 47 | [`rzgar/minimax-h3_fl2v_8Step_motion_enhancer`](https://huggingface.co/rzgar/minimax-h3_fl2v_8Step_motion_enhancer) | image-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-21 | 14016 | 0 | [`NTU-yiwen/awm-minimax-h3-new1344-lora-checkpoints`](https://huggingface.co/NTU-yiwen/awm-minimax-h3-new1344-lora-checkpoints) | minimax-h3 | lora |
| 2026-08-31 | 8599 | 60 | [`prithivMLmods/MiniMax-H3-Facial-Realism-CloseUp`](https://huggingface.co/prithivMLmods/MiniMax-H3-Facial-Realism-CloseUp) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-01 | 8428 | 36 | [`JOKER141/MiniMax-H3-Combat-Base-V2`](https://huggingface.co/JOKER141/MiniMax-H3-Combat-Base-V2) | minimax-h3 | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-09-25 | 5890 | 142 | [`akatz-ai/MiniMax-H3-Character-Swap-LoRA`](https://huggingface.co/akatz-ai/MiniMax-H3-Character-Swap-LoRA) | video-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-16 | 5799 | 0 | [`KENIC-1/Comfy-Org-MiniMax-H3-loras`](https://huggingface.co/KENIC-1/Comfy-Org-MiniMax-H3-loras) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 5447 | 61 | [`Jojocodex/minimax-h3-wushu-action-lora`](https://huggingface.co/Jojocodex/minimax-h3-wushu-action-lora) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-15 | 4814 | 28 | [`MATLOWAI/MiniMax-H3-Motion-Adapter`](https://huggingface.co/MATLOWAI/MiniMax-H3-Motion-Adapter) | image-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-08-27 | 4472 | 32 | [`siraxe/H3_slider_experiments`](https://huggingface.co/siraxe/H3_slider_experiments) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-05 | 4360 | 92 | [`speach1sdef178/MiniMax-H3-Semantic-Bridge`](https://huggingface.co/speach1sdef178/MiniMax-H3-Semantic-Bridge) | minimax-h3 | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 4109 | 57 | [`KennethFal/vh5tape-vhs-lora-minimax-h3`](https://huggingface.co/KennethFal/vh5tape-vhs-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 3514 | 3 | [`poopooness/H3-Loras`](https://huggingface.co/poopooness/H3-Loras) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-04 | 3022 | 35 | [`JOKER141/MiniMax-H3-Weapon-Combat-LoRA`](https://huggingface.co/JOKER141/MiniMax-H3-Weapon-Combat-LoRA) | minimax-h3 | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-24 | 2931 | 26 | [`Beidouqixing/minimax-h3-4step-lora-flashgen`](https://huggingface.co/Beidouqixing/minimax-h3-4step-lora-flashgen) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-25 | 2917 | 74 | [`lovis93/studio-1939-old-animation-lora-minimax-h3`](https://huggingface.co/lovis93/studio-1939-old-animation-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-17 | 2300 | 5 | [`t8star/Semantic-Bridge-Comfy`](https://huggingface.co/t8star/Semantic-Bridge-Comfy) | minimax-h3 | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-17 | 2243 | 21 | [`WarmBloodAban/Minimax_H3_LoRAs`](https://huggingface.co/WarmBloodAban/Minimax_H3_LoRAs) | image-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-20 | 2212 | 69 | [`Cseti/MiniMax-H3_Ref2VA-LoRA-CrossView-Warp_v1`](https://huggingface.co/Cseti/MiniMax-H3_Ref2VA-LoRA-CrossView-Warp_v1) | minimax-h3 | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 2096 | 3 | [`multimodalart/MiniMax-H3-Pruned`](https://huggingface.co/multimodalart/MiniMax-H3-Pruned) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 1613 | 26 | [`prithivMLmods/MiniMax-H3-I2V-Anime-Motion-LoRA`](https://huggingface.co/prithivMLmods/MiniMax-H3-I2V-Anime-Motion-LoRA) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 1364 | 1 | [`masafy/minimax-h3-masafy-lora`](https://huggingface.co/masafy/minimax-h3-masafy-lora) | image-to-video | lora, character-lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-10 | 1271 | 2 | [`Efficient-Large-Model/H3-to-LTX-Latent-Adapter`](https://huggingface.co/Efficient-Large-Model/H3-to-LTX-Latent-Adapter) | minimax-h3 |  |
| 2026-08-15 | 1156 | 0 | [`xalexmoon/hmpussy_v6_epoch30.safetensors`](https://huggingface.co/xalexmoon/hmpussy_v6_epoch30.safetensors) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:unknown |
| 2026-09-16 | 1129 | 20 | [`JOKER141/MiniMaxH3-GunFu-Gunfight-LORA`](https://huggingface.co/JOKER141/MiniMaxH3-GunFu-Gunfight-LORA) | minimax-h3 | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-20 | 1014 | 13 | [`neph1/1980s_horror_movies_minimax_h3`](https://huggingface.co/neph1/1980s_horror_movies_minimax_h3) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-27 | 755 | 56 | [`pablodawson/MiniMax-H3-360-Orbit-LoRA`](https://huggingface.co/pablodawson/MiniMax-H3-360-Orbit-LoRA) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-17 | 722 | 18 | [`KennethFal/16bit-pixel-lora-minimax-h3`](https://huggingface.co/KennethFal/16bit-pixel-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-20 | 713 | 10 | [`ostris/minimax_h3_ref2va_jacked_lora`](https://huggingface.co/ostris/minimax_h3_ref2va_jacked_lora) | video-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-07 | 661 | 35 | [`vpakarinen/natural-face-speech-h3-lora`](https://huggingface.co/vpakarinen/natural-face-speech-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-16 | 651 | 11 | [`KennethFal/retro-toon-70s-lora-minimax-h3`](https://huggingface.co/KennethFal/retro-toon-70s-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 624 | 1 | [`B4100/vh5tape-vhs-lora-minimax-h3`](https://huggingface.co/B4100/vh5tape-vhs-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 489 | 2 | [`taurusduan/MiniMax-H3-Realism-People-LoRA`](https://huggingface.co/taurusduan/MiniMax-H3-Realism-People-LoRA) | image-text-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-02 | 459 | 70 | [`vpakarinen/better-human-motion-h3-lora`](https://huggingface.co/vpakarinen/better-human-motion-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-25 | 431 | 2 | [`suryatmodulus/studio-1939-old-animation-lora-minimax-h3`](https://huggingface.co/suryatmodulus/studio-1939-old-animation-lora-minimax-h3) | text-to-video | lora |
| 2026-08-06 | 419 | 2 | [`kabachuha/mh3-morphing-helper`](https://huggingface.co/kabachuha/mh3-morphing-helper) | image-text-to-video | lora, template:diffusion-lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-16 | 405 | 18 | [`siraxe/3d_to_real_detail_slider_H3`](https://huggingface.co/siraxe/3d_to_real_detail_slider_H3) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-04 | 393 | 2 | [`t8star/Minimax-H3-World-Comfy`](https://huggingface.co/t8star/Minimax-H3-World-Comfy) | image-to-video | comfyui, lora, license:apache-2.0 |
| 2026-09-17 | 384 | 25 | [`vpakarinen/asmr-trigger-audio-h3-lora`](https://huggingface.co/vpakarinen/asmr-trigger-audio-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-19 | 358 | 5 | [`neph1/1950sScifiMinimaxH3`](https://huggingface.co/neph1/1950sScifiMinimaxH3) | text-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-26 | 331 | 12 | [`neph1/minimax_h3_handheld_shaky_camera`](https://huggingface.co/neph1/minimax_h3_handheld_shaky_camera) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-02 | 299 | 42 | [`vpakarinen/insta-tiktok-aesthetics-h3-lora`](https://huggingface.co/vpakarinen/insta-tiktok-aesthetics-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-16 | 297 | 1 | [`KennethFal/low-poly-lora-minimax-h3`](https://huggingface.co/KennethFal/low-poly-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-19 | 259 | 5 | [`prithivMLmods/MiniMax-H3-Rough-2D-Cartoon-Illustration`](https://huggingface.co/prithivMLmods/MiniMax-H3-Rough-2D-Cartoon-Illustration) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 238 | 0 | [`pmczip/MiniMaxH3_LoRAs`](https://huggingface.co/pmczip/MiniMaxH3_LoRAs) | text-to-image | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 226 | 0 | [`sonnybox/MiniMax-H3_experimental`](https://huggingface.co/sonnybox/MiniMax-H3_experimental) | image-text-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-02 | 222 | 1 | [`B4100/MiniMax-H3-Facial-Realism-CloseUp`](https://huggingface.co/B4100/MiniMax-H3-Facial-Realism-CloseUp) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-25 | 215 | 21 | [`Ashmotv/transformation_lora`](https://huggingface.co/Ashmotv/transformation_lora) | image-to-video | lora, license:other |
| 2026-09-27 | 190 | 7 | [`SOLRICKS/3D-Animation-Style-MiniMax-H3`](https://huggingface.co/SOLRICKS/3D-Animation-Style-MiniMax-H3) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 189 | 0 | [`TheMindExpansionNetwork/swingusinnerz_t2v_minimax_h3_v1`](https://huggingface.co/TheMindExpansionNetwork/swingusinnerz_t2v_minimax_h3_v1) | text-to-video | lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3 |
| 2026-08-12 | 121 | 3 | [`kabachuha/mh3-r2va-claymation-transformation`](https://huggingface.co/kabachuha/mh3-r2va-claymation-transformation) | image-text-to-video | lora, template:diffusion-lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-13 | 104 | 0 | [`MelloModels/mellos_definitive_zootopia_lora_minimax`](https://huggingface.co/MelloModels/mellos_definitive_zootopia_lora_minimax) | text-to-video | lora, license:other |
| 2026-08-31 | 96 | 0 | [`lokitsar/RHC-H3V2`](https://huggingface.co/lokitsar/RHC-H3V2) | minimax-h3 | lora, comfyui |
| 2026-09-26 | 83 | 3 | [`neph1/minimax_h3_headmounted_fpv_cam`](https://huggingface.co/neph1/minimax_h3_headmounted_fpv_cam) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 71 | 0 | [`pharaouk/awm-minimax-h3-new1344-lora-checkpoints`](https://huggingface.co/pharaouk/awm-minimax-h3-new1344-lora-checkpoints) | minimax-h3 | lora |
| 2026-08-09 | 66 | 5 | [`siraxe/Venom_transformation_H3`](https://huggingface.co/siraxe/Venom_transformation_H3) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-28 | 63 | 7 | [`MATLOWAI/MiniMax-H3-ORB360-CardSpin`](https://huggingface.co/MATLOWAI/MiniMax-H3-ORB360-CardSpin) | image-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-12 | 47 | 0 | [`Shriramnag/Shiv-AI-Motion-Enhancer`](https://huggingface.co/Shriramnag/Shiv-AI-Motion-Enhancer) | image-to-video | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-26 | 45 | 0 | [`zzzDDs/MiniMax-H3_experimental`](https://huggingface.co/zzzDDs/MiniMax-H3_experimental) | image-text-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-26 | 43 | 3 | [`neph1/1920s_horror_movies_minimax_h3`](https://huggingface.co/neph1/1920s_horror_movies_minimax_h3) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-23 | 35 | 1 | [`Leon1000/16bit-pixel-lora-minimax-h3`](https://huggingface.co/Leon1000/16bit-pixel-lora-minimax-h3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 31 | 2 | [`siraxe/vault_dweller_H3_slider`](https://huggingface.co/siraxe/vault_dweller_H3_slider) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-09-08 | 28 | 0 | [`concil859856/natural-face-speech-h3-lora`](https://huggingface.co/concil859856/natural-face-speech-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-07 | 26 | 0 | [`woodfireind/H3-ScriptGen`](https://huggingface.co/woodfireind/H3-ScriptGen) | text-generation | lora, base_model:Qwen/Qwen3.5-0.8B, base_model:adapter:Qwen/Qwen3.5-0.8B, license:apache-2.0 |
| 2026-09-13 | 23 | 3 | [`talos414/Paint-on-glass-LoRA`](https://huggingface.co/talos414/Paint-on-glass-LoRA) | minimax-h3 | lora |
| 2026-09-19 | 22 | 1 | [`TechnoBaptist/asmr-trigger-audio-h3-lora`](https://huggingface.co/TechnoBaptist/asmr-trigger-audio-h3-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-29 | 22 | 0 | [`nikomateos/minimax-h3-project-lora`](https://huggingface.co/nikomateos/minimax-h3-project-lora) | minimax-h3 | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-28 | 20 | 5 | [`neph1/1980s_scifi_movies_minimax_h3`](https://huggingface.co/neph1/1980s_scifi_movies_minimax_h3) | text-to-image | lora, template:diffusion-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-28 | 18 | 0 | [`muhammad-taqi512/SLORA-MAX`](https://huggingface.co/muhammad-taqi512/SLORA-MAX) | text-to-video | license:mit |
| 2026-09-28 | 15 | 0 | [`Kobe202455/MiniMax-H3-Character-Swap-LoRA`](https://huggingface.co/Kobe202455/MiniMax-H3-Character-Swap-LoRA) | video-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-15 | 0 | 2 | [`0xJuicybear/H3LoRA`](https://huggingface.co/0xJuicybear/H3LoRA) |  | license:mit |
| 2026-08-07 | 0 | 0 | [`AdwolfCzar/h3_test_lora1`](https://huggingface.co/AdwolfCzar/h3_test_lora1) |  |  |
| 2026-09-04 | 0 | 3 | [`Alex995647/loras-minimax-h3`](https://huggingface.co/Alex995647/loras-minimax-h3) | diffusers | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-15 | 0 | 5 | [`ApacheOne/H3_loras`](https://huggingface.co/ApacheOne/H3_loras) |  |  |
| 2026-09-18 | 0 | 0 | [`Boerboer/H3_LoRAs`](https://huggingface.co/Boerboer/H3_LoRAs) |  | license:apache-2.0 |
| 2026-09-19 | 0 | 0 | [`Buattensorart2/ostris_minimaxh3_loras_yy`](https://huggingface.co/Buattensorart2/ostris_minimaxh3_loras_yy) |  |  |
| 2026-08-06 | 0 | 3 | [`ComfyCloudModel/MinimaxH3-Loras`](https://huggingface.co/ComfyCloudModel/MinimaxH3-Loras) |  | license:apache-2.0 |
| 2026-09-28 | 0 | 0 | [`Cufuudsa/h3-loras`](https://huggingface.co/Cufuudsa/h3-loras) |  |  |
| 2026-08-31 | 0 | 93 | [`DANNY621/H3-World`](https://huggingface.co/DANNY621/H3-World) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 0 | 1 | [`DIE2025/MiniMaxH3Loras`](https://huggingface.co/DIE2025/MiniMaxH3Loras) |  |  |
| 2026-08-14 | 0 | 16 | [`DiffSynth-Studio/MiniMax-H3-LoRA-LineartAnime`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-LoRA-LineartAnime) |  | license:apache-2.0 |
| 2026-09-08 | 0 | 1 | [`EllipsesMark/Minimax-h3_Singularity-Lora`](https://huggingface.co/EllipsesMark/Minimax-h3_Singularity-Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 0 | 10 | [`EllipsesMark/minimax-h3-vr180-sbs-lora`](https://huggingface.co/EllipsesMark/minimax-h3-vr180-sbs-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-27 | 0 | 0 | [`Fasces/H3-LoraVault`](https://huggingface.co/Fasces/H3-LoraVault) |  |  |
| 2026-09-01 | 0 | 59 | [`JOKER141/MiniMax-H3-General-Motion-Continuity-Repair`](https://huggingface.co/JOKER141/MiniMax-H3-General-Motion-Continuity-Repair) |  | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3 |
| 2026-08-22 | 0 | 5 | [`Jojocodex/mslc-h3-lora`](https://huggingface.co/Jojocodex/mslc-h3-lora) |  |  |
| 2026-09-16 | 0 | 5 | [`KennethFal/hand-drawn-lora-minimax-h3`](https://huggingface.co/KennethFal/hand-drawn-lora-minimax-h3) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 0 | 15 | [`LeechTM/SMACK`](https://huggingface.co/LeechTM/SMACK) |  | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-17 | 0 | 1 | [`MachineDelusions/Minimax-H3-LoRas`](https://huggingface.co/MachineDelusions/Minimax-H3-LoRas) |  |  |
| 2026-09-14 | 0 | 0 | [`NaukNauk/minimax-h3-ref2va-larry-v4-strength-0.7`](https://huggingface.co/NaukNauk/minimax-h3-ref2va-larry-v4-strength-0.7) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-15 | 0 | 0 | [`NaukNauk/minimax-h3-ref2va-larry-v4-strength-1.3`](https://huggingface.co/NaukNauk/minimax-h3-ref2va-larry-v4-strength-1.3) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-15 | 0 | 0 | [`NaukNauk/minimax-h3-ref2va-larry-v4-strength-1.7`](https://huggingface.co/NaukNauk/minimax-h3-ref2va-larry-v4-strength-1.7) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-15 | 0 | 2 | [`NaukNauk/minimax-h3-ref2va-larry-v4-strength-2.0`](https://huggingface.co/NaukNauk/minimax-h3-ref2va-larry-v4-strength-2.0) | image-text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-06 | 0 | 7 | [`Nebsh/Snorricam_H3_LORA`](https://huggingface.co/Nebsh/Snorricam_H3_LORA) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-16 | 0 | 0 | [`Patarapoom/H3_lora`](https://huggingface.co/Patarapoom/H3_lora) |  |  |
| 2026-08-30 | 0 | 26 | [`Plaguekind/H3-Lora`](https://huggingface.co/Plaguekind/H3-Lora) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-14 | 0 | 0 | [`Plaguekind/H3-Loras`](https://huggingface.co/Plaguekind/H3-Loras) |  | license:mit |
| 2026-09-27 | 0 | 0 | [`RunningHubAI/rh-h3-faster-anime-edition-lora`](https://huggingface.co/RunningHubAI/rh-h3-faster-anime-edition-lora) |  | comfyui, lora |
| 2026-09-23 | 0 | 0 | [`RunningHubAI/rh-h3-faster-harder-shake-harder-lora`](https://huggingface.co/RunningHubAI/rh-h3-faster-harder-shake-harder-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-h3-lora`](https://huggingface.co/RunningHubAI/rh-h3-lora) |  | comfyui, lora |
| 2026-09-25 | 0 | 0 | [`RunningHubAI/rh-h3-lora-2089619072047755266`](https://huggingface.co/RunningHubAI/rh-h3-lora-2089619072047755266) |  | comfyui, lora |
| 2026-09-25 | 0 | 0 | [`RunningHubAI/rh-h3-lora-2092624415427637249`](https://huggingface.co/RunningHubAI/rh-h3-lora-2092624415427637249) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-h3-lora-2095419813689593858`](https://huggingface.co/RunningHubAI/rh-h3-lora-2095419813689593858) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-h3-lora-2097123433183518722`](https://huggingface.co/RunningHubAI/rh-h3-lora-2097123433183518722) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-h3-lora-2097509723998736385`](https://huggingface.co/RunningHubAI/rh-h3-lora-2097509723998736385) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-h3-lora-h3-ending-reaction-booster-lora`](https://huggingface.co/RunningHubAI/rh-h3-lora-h3-ending-reaction-booster-lora) |  | comfyui, lora |
| 2026-09-25 | 0 | 4 | [`RunningHubAI/rh-h3-speed-slider-1.1-lora`](https://huggingface.co/RunningHubAI/rh-h3-speed-slider-1.1-lora) |  | comfyui, lora |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-h3realismolora-lora`](https://huggingface.co/RunningHubAI/rh-h3realismolora-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-lora-h3-lora`](https://huggingface.co/RunningHubAI/rh-lora-h3-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-five-view-512-s1500.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-five-view-512-s1500.safetensors-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-five-view-512-s400-instruct.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-five-view-512-s400-instruct.safetensors-lora) |  | comfyui, lora |
| 2026-09-27 | 0 | 1 | [`RunningHubAI/rh-minimax-h3-lms-v1.0-r64-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-lms-v1.0-r64-lora) |  | comfyui, lora |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-lms-v1.0-r64.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-lms-v1.0-r64.safetensors-lora) |  | comfyui, lora |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-third-person-view.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-third-person-view.safetensors-lora) |  | comfyui, lora |
| 2026-09-25 | 0 | 0 | [`RunningHubAI/rh-minimax-h3v0.1-feihouremix-v0.6-compat-v001.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3v0.1-feihouremix-v0.6-compat-v001.safetensors-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 1 | [`SicariusSicariiStuff/Minimax_H3_LoRAs`](https://huggingface.co/SicariusSicariiStuff/Minimax_H3_LoRAs) | text-to-video | license:other |
| 2026-09-22 | 0 | 0 | [`Teddooo/Minimaxh3loras`](https://huggingface.co/Teddooo/Minimaxh3loras) |  |  |
| 2026-08-14 | 0 | 5 | [`TenStrip/Anima-H3-Booster-Lora`](https://huggingface.co/TenStrip/Anima-H3-Booster-Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 0 | 18 | [`TenStrip/Krea2-H3-Style-Lora`](https://huggingface.co/TenStrip/Krea2-H3-Style-Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 0 | 28 | [`TenStrip/Minimax-h3_Singularity-Lora`](https://huggingface.co/TenStrip/Minimax-h3_Singularity-Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 26 | [`TenStrip/Wan2.2_H3_Motion_Lora`](https://huggingface.co/TenStrip/Wan2.2_H3_Motion_Lora) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-14 | 0 | 91 | [`Viggle/Meridian`](https://huggingface.co/Viggle/Meridian) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-11 | 0 | 2 | [`Wanamingo/MiniMax-H3-LoRAs`](https://huggingface.co/Wanamingo/MiniMax-H3-LoRAs) |  |  |
| 2026-08-25 | 0 | 0 | [`adehong/minimax-h3-ntt-lora`](https://huggingface.co/adehong/minimax-h3-ntt-lora) |  |  |
| 2026-08-03 | 0 | 4 | [`aimalias/h3-loras`](https://huggingface.co/aimalias/h3-loras) |  |  |
| 2026-08-14 | 0 | 19 | [`alvdansen/h3-keyframe-animation`](https://huggingface.co/alvdansen/h3-keyframe-animation) | image-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-26 | 0 | 0 | [`azjkjkkjdkjsd/h3zero-loras`](https://huggingface.co/azjkjkkjdkjsd/h3zero-loras) |  |  |
| 2026-09-10 | 0 | 23 | [`circlestone-labs/MiniMax-H3-Image-Training-Adapter`](https://huggingface.co/circlestone-labs/MiniMax-H3-Image-Training-Adapter) |  | license:other |
| 2026-08-17 | 0 | 0 | [`cjab05/MiniMaxH3Lora`](https://huggingface.co/cjab05/MiniMaxH3Lora) |  |  |
| 2026-08-19 | 0 | 12 | [`diffusers-modular/minimax-h3-inpainting`](https://huggingface.co/diffusers-modular/minimax-h3-inpainting) | video-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-25 | 0 | 0 | [`elliotcareydev/minimax-h3-loras`](https://huggingface.co/elliotcareydev/minimax-h3-loras) |  |  |
| 2026-08-09 | 0 | 15 | [`ethanfel/MiniMax-H3-Pruned-Ref2VA-Delta-LoRAs-Experimental`](https://huggingface.co/ethanfel/MiniMax-H3-Pruned-Ref2VA-Delta-LoRAs-Experimental) |  | comfyui, lora, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-11 | 0 | 0 | [`gg64537334/MiniMax-H3-Whip-LoRA`](https://huggingface.co/gg64537334/MiniMax-H3-Whip-LoRA) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-26 | 0 | 0 | [`gregt/fincher35look-h3-lora`](https://huggingface.co/gregt/fincher35look-h3-lora) |  |  |
| 2026-08-07 | 0 | 5 | [`iamgroot1212/minimax-h3-loras`](https://huggingface.co/iamgroot1212/minimax-h3-loras) |  | license:apache-2.0 |
| 2026-09-29 | 0 | 0 | [`kaibara/MiniMax_H3_lora`](https://huggingface.co/kaibara/MiniMax_H3_lora) |  |  |
| 2026-09-03 | 0 | 0 | [`kakkkarotto/H3_loras`](https://huggingface.co/kakkkarotto/H3_loras) |  |  |
| 2026-08-28 | 0 | 2 | [`matheus58457/minimax-h3-loras`](https://huggingface.co/matheus58457/minimax-h3-loras) |  |  |
| 2026-08-08 | 0 | 36 | [`matlod/minimax-h3-turnaround`](https://huggingface.co/matlod/minimax-h3-turnaround) |  | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 0 | 1 | [`musafa901/Minimax_H3-Age_Slider`](https://huggingface.co/musafa901/Minimax_H3-Age_Slider) |  | license:apache-2.0 |
| 2026-08-18 | 0 | 87 | [`mvp-lab/MiniMax-H3-RAVEN-Streaming-LoRA`](https://huggingface.co/mvp-lab/MiniMax-H3-RAVEN-Streaming-LoRA) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-12 | 0 | 5 | [`nikdevs/minimax-h3-loras`](https://huggingface.co/nikdevs/minimax-h3-loras) |  |  |
| 2026-08-11 | 0 | 6 | [`nynxz/H3_Loras`](https://huggingface.co/nynxz/H3_Loras) |  |  |
| 2026-08-06 | 0 | 25 | [`ostris/minimax_h3_training_adapter`](https://huggingface.co/ostris/minimax_h3_training_adapter) |  |  |
| 2026-09-25 | 0 | 0 | [`piefke123/h3loras`](https://huggingface.co/piefke123/h3loras) |  |  |
| 2026-09-03 | 0 | 39 | [`rehan-fal/minimax-h3-vr180-sbs-lora`](https://huggingface.co/rehan-fal/minimax-h3-vr180-sbs-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 0 | 0 | [`russgilbert/providence-bassey-h3-lora`](https://huggingface.co/russgilbert/providence-bassey-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-bose-h3-lora`](https://huggingface.co/russgilbert/providence-bose-h3-lora) |  |  |
| 2026-08-28 | 0 | 0 | [`russgilbert/providence-choi-h3-lora`](https://huggingface.co/russgilbert/providence-choi-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-hala-h3-lora`](https://huggingface.co/russgilbert/providence-hala-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-kaminski-h3-lora`](https://huggingface.co/russgilbert/providence-kaminski-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-paran-h3-lora`](https://huggingface.co/russgilbert/providence-paran-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-rivera-h3-lora`](https://huggingface.co/russgilbert/providence-rivera-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-taddeo-h3-lora`](https://huggingface.co/russgilbert/providence-taddeo-h3-lora) |  |  |
| 2026-08-30 | 0 | 0 | [`russgilbert/providence-torin-h3-lora`](https://huggingface.co/russgilbert/providence-torin-h3-lora) |  |  |
| 2026-09-23 | 0 | 0 | [`rvhfxb/minimax-h3-vnloras`](https://huggingface.co/rvhfxb/minimax-h3-vnloras) |  |  |
| 2026-09-04 | 0 | 23 | [`shamanic/minimax-h3-equi360-lora`](https://huggingface.co/shamanic/minimax-h3-equi360-lora) | text-to-video | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 0 | 0 | [`sintecs/minimax_h3_loras`](https://huggingface.co/sintecs/minimax_h3_loras) |  |  |
| 2026-08-29 | 0 | 0 | [`techbot911/H3_Loras`](https://huggingface.co/techbot911/H3_Loras) |  |  |
| 2026-08-09 | 0 | 19 | [`tutututututu/Tutu-MiniMax-H3-AudioVideo-20to8-NFE-LoRA`](https://huggingface.co/tutututututu/Tutu-MiniMax-H3-AudioVideo-20to8-NFE-LoRA) | image-text-to-video | lora, comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 0 | 0 | [`xcmsubs/arnld-h3-lora`](https://huggingface.co/xcmsubs/arnld-h3-lora) |  |  |
| 2026-09-11 | 0 | 0 | [`yichengup/MiniMax-H3-LoRAs`](https://huggingface.co/yichengup/MiniMax-H3-LoRAs) |  | license:mit |
| 2026-08-10 | 0 | 0 | [`yitongl/minimax-h3-nvfp4-lora-recovery`](https://huggingface.co/yitongl/minimax-h3-nvfp4-lora-recovery) |  | nvfp4, quantization, lora, post-training-quantization, license:other |
| 2026-08-30 | 0 | 0 | [`zeruel0413/h3-loras`](https://huggingface.co/zeruel0413/h3-loras) |  |  |

### 10-Apple-MLX

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-03 | 3861 | 10 | [`pipenetwork/MiniMax-H3-MLX-8bit`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-8bit) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 3213 | 16 | [`ddalcu/MiniMax-H3-FL2VA-MLX-Serve-8bit`](https://huggingface.co/ddalcu/MiniMax-H3-FL2VA-MLX-Serve-8bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 2228 | 9 | [`ddalcu/MiniMax-H3-FL2VA-MLX-Serve-4bit`](https://huggingface.co/ddalcu/MiniMax-H3-FL2VA-MLX-Serve-4bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 1363 | 6 | [`pipenetwork/MiniMax-H3-MLX-4bit`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-4bit) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 850 | 8 | [`pipenetwork/MiniMax-H3-MLX-bf16`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-bf16) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 741 | 3 | [`water1234/MiniMax-H3-MLX-Argus-Calibrated-INT8`](https://huggingface.co/water1234/MiniMax-H3-MLX-Argus-Calibrated-INT8) | text-to-video | mlx, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-07 | 480 | 4 | [`antocorr/MiniMax-H3-FL2VA-MLX-Serve-2bit-text-encoder`](https://huggingface.co/antocorr/MiniMax-H3-FL2VA-MLX-Serve-2bit-text-encoder) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 460 | 0 | [`ddalcu/MiniMax-H3-REF2VA-MLX-Serve-8bit`](https://huggingface.co/ddalcu/MiniMax-H3-REF2VA-MLX-Serve-8bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 381 | 2 | [`pipenetwork/MiniMax-H3-MLX-6bit`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-6bit) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 337 | 3 | [`Sawfwair/MiniMax-H3-FL2VA-MLX-4bit`](https://huggingface.co/Sawfwair/MiniMax-H3-FL2VA-MLX-4bit) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 280 | 1 | [`gabrielrocco/MiniMax-H3-Ref2VA-MLX-Serve-4bit`](https://huggingface.co/gabrielrocco/MiniMax-H3-Ref2VA-MLX-Serve-4bit) | image-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 253 | 0 | [`Sawfwair/MiniMax-H3-FL2VA-MLX-8bit`](https://huggingface.co/Sawfwair/MiniMax-H3-FL2VA-MLX-8bit) | text-to-video | mlx, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 216 | 0 | [`Sawfwair/MiniMax-H3-FL2VA-MLX-BF16`](https://huggingface.co/Sawfwair/MiniMax-H3-FL2VA-MLX-BF16) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 148 | 0 | [`pipenetwork/MiniMax-H3-MLX-f32`](https://huggingface.co/pipenetwork/MiniMax-H3-MLX-f32) | image-text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 131 | 0 | [`gabrielrocco/MiniMax-H3-Ref2VA-MLX-Serve-8bit`](https://huggingface.co/gabrielrocco/MiniMax-H3-Ref2VA-MLX-Serve-8bit) | image-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-10 | 128 | 0 | [`Sawfwair/MiniMax-H3-Ref2VA-MLX-8bit`](https://huggingface.co/Sawfwair/MiniMax-H3-Ref2VA-MLX-8bit) | image-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 81 | 0 | [`finbase0530/MiniMax-H3-FL2VA-MLX-Serve-8bit`](https://huggingface.co/finbase0530/MiniMax-H3-FL2VA-MLX-Serve-8bit) | text-to-video | mlx, mlx-serve, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 40 | 0 | [`Vayden/MiniMax-H3-MLX-q8-extended-paged`](https://huggingface.co/Vayden/MiniMax-H3-MLX-q8-extended-paged) | text-to-video | mlx, comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 26 | 0 | [`Vayden/Qwen3-VL-32B-H3-MLX-q8-paged`](https://huggingface.co/Vayden/Qwen3-VL-32B-H3-MLX-q8-paged) | mlx | mlx, comfyui, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:other |
| 2026-09-09 | 15 | 0 | [`Vayden/Qwen3-VL-32B-H3-MLX-q8-vision-paged`](https://huggingface.co/Vayden/Qwen3-VL-32B-H3-MLX-q8-vision-paged) | mlx | mlx, comfyui, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:other |
| 2026-09-09 | 5 | 0 | [`Vayden/MiniMax-H3-Ref2VA-MLX-q8-extended-paged`](https://huggingface.co/Vayden/MiniMax-H3-Ref2VA-MLX-q8-extended-paged) | mlx | mlx, comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-17 | 0 | 2 | [`MrMofer/MiniMax-H3-MLX-8bit`](https://huggingface.co/MrMofer/MiniMax-H3-MLX-8bit) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-12 | 0 | 0 | [`SceneWorks/minimax-h3-mlx`](https://huggingface.co/SceneWorks/minimax-h3-mlx) | diffusers |  |
| 2026-08-08 | 0 | 1 | [`Vayden/MiniMax-H3-Video-VAE-MLX-Q8`](https://huggingface.co/Vayden/MiniMax-H3-Video-VAE-MLX-Q8) | mlx | mlx, comfyui, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 0 | 4 | [`appautomaton/minimax-h3-base-8bit-mlx`](https://huggingface.co/appautomaton/minimax-h3-base-8bit-mlx) | text-to-video | mlx, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-10 | 0 | 0 | [`nanguoyu/MiniMax-H3-minirun`](https://huggingface.co/nanguoyu/MiniMax-H3-minirun) | diffusers | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:quantized:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 0 | 0 | [`shadow/mmh3turbo-bundles`](https://huggingface.co/shadow/mmh3turbo-bundles) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-08-10 | 0 | 1 | [`uetuluk2/minimax-h3-mlx-rebuild`](https://huggingface.co/uetuluk2/minimax-h3-mlx-rebuild) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-08-11 | 0 | 2 | [`water1234/MiniMax-H3-Turbo-v4-step600-EMA-MLX`](https://huggingface.co/water1234/MiniMax-H3-Turbo-v4-step600-EMA-MLX) | text-to-video | mlx, lora, turbo, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-08-07 | 0 | 0 | [`yunfengwang/mmh3turbo-bundles`](https://huggingface.co/yunfengwang/mmh3turbo-bundles) | text-to-video | mlx, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-09-09 | 0 | 0 | [`yvankob/minimax-h3-base-8bit-mlx-by-appautomaton`](https://huggingface.co/yvankob/minimax-h3-base-8bit-mlx-by-appautomaton) | text-to-video | mlx, quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 11-组件-VAE-TE-提示器

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-17 | 237109 | 362 | [`LBH-123-AI/Minimax_h3_latent_Upscaler`](https://huggingface.co/LBH-123-AI/Minimax_h3_latent_Upscaler) | minimax-h3 | comfyui, license:apache-2.0 |
| 2026-08-20 | 16859 | 55 | [`iamkaikai/MiniMax-H3-Single-Frame-VAE-500K`](https://huggingface.co/iamkaikai/MiniMax-H3-Single-Frame-VAE-500K) | diffusers | base_model:Mamad8/MiniMax-H3-Image-VAE, base_model:finetune:Mamad8/MiniMax-H3-Image-VAE |
| 2026-08-23 | 4391 | 3 | [`fbjr/qwen3-vl-32b-W4A16-AWQ-H3`](https://huggingface.co/fbjr/qwen3-vl-32b-W4A16-AWQ-H3) | minimax-h3 | comfyui, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-09-18 | 2921 | 1 | [`t8star/Taeh3-Comfy`](https://huggingface.co/t8star/Taeh3-Comfy) | minimax-h3 | comfyui, license:other |
| 2026-09-25 | 2611 | 0 | [`ZawShiShawn/Gestura-MiniMax-H3-VAE-LiteRT`](https://huggingface.co/ZawShiShawn/Gestura-MiniMax-H3-VAE-LiteRT) | image-to-video | quantized, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 925 | 0 | [`6block/MiniMax-H3-Qwen3-VL-NVFP4`](https://huggingface.co/6block/MiniMax-H3-Qwen3-VL-NVFP4) | text-to-video | nvfp4, comfyui, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-26 | 532 | 50 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-Omni) | text-generation | lora, base_model:Qwen/Qwen2.5-Omni-7B, base_model:adapter:Qwen/Qwen2.5-Omni-7B, license:other |
| 2026-08-18 | 440 | 45 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA-8B) | image-text-to-text | lora, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:adapter:Qwen/Qwen3-VL-8B-Instruct |
| 2026-08-07 | 313 | 187 | [`lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA`](https://huggingface.co/lightx2v/MiniMax-H3-Prompt-Rewriter-LoRA) | peft | lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B |
| 2026-08-20 | 304 | 2 | [`nynxz/Qwen3-VL-8B-ComfyUI`](https://huggingface.co/nynxz/Qwen3-VL-8B-ComfyUI) | image-text-to-text | comfyui, lora, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:adapter:Qwen/Qwen3-VL-8B-Instruct, license:apache-2.0 |
| 2026-09-02 | 299 | 30 | [`Asirus/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY`](https://huggingface.co/Asirus/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY) |  | comfyui, requantization, base_model:LBH-123-AI/Minimax_h3_latent_Upscaler, base_model:finetune:LBH-123-AI/Minimax_h3_latent_Upscaler, license:apache-2.0 |
| 2026-09-05 | 285 | 2 | [`pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-NVFP4-AWQ`](https://huggingface.co/pottokao/MiniMax-H3-TextEncoder-Qwen3VL-32B-abliterated-NVFP4-AWQ) | image-text-to-text | nvfp4, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-09-07 | 229 | 2 | [`PuppetVision/qwen3vl-32b-minimax-h3-amd-rocm-optimized-comfy-triton`](https://huggingface.co/PuppetVision/qwen3vl-32b-minimax-h3-amd-rocm-optimized-comfy-triton) | minimax-h3 | comfyui, int8, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:finetune:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-19 | 165 | 1 | [`qtum/MiniMax-H3-Qwen3-VL-NVFP4`](https://huggingface.co/qtum/MiniMax-H3-Qwen3-VL-NVFP4) | text-to-video | nvfp4, comfyui, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-23 | 133 | 0 | [`b-rosel/Minimax_h3_latent_Upscaler`](https://huggingface.co/b-rosel/Minimax_h3_latent_Upscaler) | minimax-h3 | comfyui, license:apache-2.0 |
| 2026-08-06 | 115 | 2 | [`rockerBOO/qwen3-vl-32b-h3-tail-nvfp4`](https://huggingface.co/rockerBOO/qwen3-vl-32b-h3-tail-nvfp4) | image-text-to-text | comfyui, nvfp4, quantized, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-16 | 85 | 1 | [`valarauca1/qwen3-vl-25m-stitched-8bL16-to-32bL29`](https://huggingface.co/valarauca1/qwen3-vl-25m-stitched-8bL16-to-32bL29) | feature-extraction | base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:merge:Qwen/Qwen3-VL-32B-Instruct, base_model:Qwen/Qwen3-VL-8B-Instruct, base_model:merge:Qwen/Qwen3-VL-8B-Instruct, license:apache-2.0 |
| 2026-09-24 | 57 | 0 | [`FinancialSupport/vr180-poc-clips-3s-lora`](https://huggingface.co/FinancialSupport/vr180-poc-clips-3s-lora) | minimax-h3 | lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 51 | 5 | [`rzgar/qwen3-vl-32b-minimax-h3-fp8-comfyui`](https://huggingface.co/rzgar/qwen3-vl-32b-minimax-h3-fp8-comfyui) | image-text-to-text | base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-08-19 | 34 | 1 | [`moonzerokevin/qwen3vl-32b-minimax-h3-nf4`](https://huggingface.co/moonzerokevin/qwen3vl-32b-minimax-h3-nf4) | image-text-to-text | nf4, base_model:Qwen/Qwen3-VL-32B-Instruct, base_model:quantized:Qwen/Qwen3-VL-32B-Instruct, license:apache-2.0 |
| 2026-09-28 | 30 | 0 | [`mcbibi/Minimax_h3_latent_Upscaler`](https://huggingface.co/mcbibi/Minimax_h3_latent_Upscaler) | minimax-h3 | comfyui, license:apache-2.0 |
| 2026-09-19 | 20 | 2 | [`ygugyg/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY`](https://huggingface.co/ygugyg/Minimax-H3-Latent-Upscaler-BF16-MAXQUALITY) |  | comfyui, requantization, base_model:LBH-123-AI/Minimax_h3_latent_Upscaler, base_model:finetune:LBH-123-AI/Minimax_h3_latent_Upscaler, license:apache-2.0 |
| 2026-08-10 | 13 | 2 | [`StellarVoyager/H3-IR-Qwen3.6-27B-LoRA`](https://huggingface.co/StellarVoyager/H3-IR-Qwen3.6-27B-LoRA) | image-text-to-text | lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B, license:apache-2.0 |
| 2026-08-08 | 5 | 0 | [`Momoking/MiniMax-H3-Prompt-Rewriter-LoRA`](https://huggingface.co/Momoking/MiniMax-H3-Prompt-Rewriter-LoRA) | peft | lora, base_model:Qwen/Qwen3.6-27B, base_model:adapter:Qwen/Qwen3.6-27B |
| 2026-09-29 | 4 | 0 | [`zhangccccc/Minimax_h3_latent_Upscaler`](https://huggingface.co/zhangccccc/Minimax_h3_latent_Upscaler) | minimax-h3 | comfyui, license:apache-2.0 |
| 2026-08-20 | 0 | 14 | [`Alissonerdx/MiniMax-H3-Single-Frame-VAE-500K-Comfy`](https://huggingface.co/Alissonerdx/MiniMax-H3-Single-Frame-VAE-500K-Comfy) |  |  |
| 2026-09-07 | 0 | 0 | [`Allen987/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Allen987/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-14 | 0 | 6 | [`DiffSynth-Studio/MiniMax-H3-Text-Embeddings`](https://huggingface.co/DiffSynth-Studio/MiniMax-H3-Text-Embeddings) |  | license:apache-2.0 |
| 2026-09-03 | 0 | 1 | [`GuangyuanSD/minimax_h3_video_vae_int8_convrot`](https://huggingface.co/GuangyuanSD/minimax_h3_video_vae_int8_convrot) |  | license:apache-2.0 |
| 2026-09-08 | 0 | 0 | [`Jackxuanxuan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Jackxuanxuan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-27 | 0 | 0 | [`Jamphus/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Jamphus/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-29 | 0 | 3 | [`Konteni2/Minimax_h3_latent_Upscaler`](https://huggingface.co/Konteni2/Minimax_h3_latent_Upscaler) |  |  |
| 2026-08-08 | 0 | 11 | [`Mamad8/H3-Latent-Upscaler-2x`](https://huggingface.co/Mamad8/H3-Latent-Upscaler-2x) |  | comfyui |
| 2026-08-08 | 0 | 91 | [`Mamad8/MiniMax-H3-Image-VAE`](https://huggingface.co/Mamad8/MiniMax-H3-Image-VAE) |  | comfyui |
| 2026-08-08 | 0 | 0 | [`Momoking/MiniMax-H3-TAE`](https://huggingface.co/Momoking/MiniMax-H3-TAE) |  | license:apache-2.0 |
| 2026-08-07 | 0 | 265 | [`Momoking/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/Momoking/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-09 | 0 | 163 | [`NicoLab28/ClipProj-MiniMax-H3`](https://huggingface.co/NicoLab28/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-04 | 0 | 16 | [`OTMFLY/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot`](https://huggingface.co/OTMFLY/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot) | image-text-to-text | comfyui, int8, quantized, base_model:llmfan46/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic, base_model:finetune:llmfan46/Qwen3-VL-32B-Instruct-ultra-uncensored-heretic, license:apache-2.0 |
| 2026-08-31 | 0 | 0 | [`PixelAlchemist123/Minimax_h3_latent_Upscaler`](https://huggingface.co/PixelAlchemist123/Minimax_h3_latent_Upscaler) |  |  |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-lsfqwen3vl-32b-minimax-h3-ultra-uncensored-heretic-int8-convrot.safetensors-checkpoint`](https://huggingface.co/RunningHubAI/rh-lsfqwen3vl-32b-minimax-h3-ultra-uncensored-heretic-int8-convrot.safetensors-checkpoint) | text-to-image | comfyui |
| 2026-09-21 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-qwen3vl32b-prompt-generation-overlay-polaris-r16-plus-heretic-v2.safetensors-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-qwen3vl32b-prompt-generation-overlay-polaris-r16-plus-heretic-v2.safetensors-lora) |  | comfyui, lora |
| 2026-08-13 | 0 | 2 | [`SearchingMan/MiniMax-H3-Text-Encoders`](https://huggingface.co/SearchingMan/MiniMax-H3-Text-Encoders) | text-to-video | comfyui, int8, nvfp4, license:apache-2.0 |
| 2026-08-30 | 0 | 0 | [`cjpgxm/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/cjpgxm/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-09 | 0 | 0 | [`cuifurong/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/cuifurong/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-09 | 0 | 0 | [`disguisequence/ClipProj-MiniMax-H3`](https://huggingface.co/disguisequence/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-09-14 | 0 | 3 | [`fretdr/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/fretdr/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-29 | 0 | 1 | [`jackieccwu/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/jackieccwu/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-16 | 0 | 2 | [`jhong520/ClipProj-MiniMax-H3`](https://huggingface.co/jhong520/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-09-12 | 0 | 0 | [`lansen97/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/lansen97/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-09-01 | 0 | 25 | [`lihaoyun6/MiniMax-H3-VAE-ONNX`](https://huggingface.co/lihaoyun6/MiniMax-H3-VAE-ONNX) |  | base_model:Comfy-Org/MiniMax-H3, base_model:quantized:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-05 | 0 | 48 | [`linjian257/qwen3vl_32b_minimax_h3_int8_convrot_uncensored-by-linjian257`](https://huggingface.co/linjian257/qwen3vl_32b_minimax_h3_int8_convrot_uncensored-by-linjian257) |  | comfyui, int8, quantized, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-22 | 0 | 11 | [`misstoyou/ClipProj-MiniMax-H3`](https://huggingface.co/misstoyou/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-04 | 0 | 224 | [`sakamakismile/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/sakamakismile/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-MiniMax-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-10 | 0 | 1 | [`suryatmodulus/ClipProj-MiniMax-H3`](https://huggingface.co/suryatmodulus/ClipProj-MiniMax-H3) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-09-27 | 0 | 3 | [`t8star/MinimaxH3-HyperVae-V2`](https://huggingface.co/t8star/MinimaxH3-HyperVae-V2) |  |  |
| 2026-08-31 | 0 | 0 | [`taurusduan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/taurusduan/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |
| 2026-08-17 | 0 | 0 | [`xdkings/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4`](https://huggingface.co/xdkings/Qwen3-VL-32B-Heretic-MiniMax-H3-NVFP4) | comfyui | comfyui, nvfp4, base_model:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, base_model:quantized:ethanfel/Qwen3-VL-32B-Ultra-Heretic-H3-ComfyUI-INT8-ConvRot, license:apache-2.0 |

### 12-题材角色LoRA含NSFW

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-09-04 | 56649 | 11 | [`brurpo/DaSiWa-MiniMax-H3-Hybrid`](https://huggingface.co/brurpo/DaSiWa-MiniMax-H3-Hybrid) | image-text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 39518 | 44 | [`Hearmeman/minimax-h3-loras`](https://huggingface.co/Hearmeman/minimax-h3-loras) | text-to-video | lora, comfyui, nsfw, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 26124 | 2 | [`lynaNSFW/DaSiWa_MiniMax_H3`](https://huggingface.co/lynaNSFW/DaSiWa_MiniMax_H3) | text-to-image | lora, template:diffusion-lora, base_model:lynaNSFW/minimaxH3_Collection, base_model:adapter:lynaNSFW/minimaxH3_Collection |
| 2026-08-30 | 8817 | 9 | [`berryber09/10Eros-Max-h3-turbo-hybrid-beta4-w4a8`](https://huggingface.co/berryber09/10Eros-Max-h3-turbo-hybrid-beta4-w4a8) | text-to-video | comfyui, quantized, turbo, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-26 | 4108 | 5 | [`lynaNSFW/minimaxH3_Collection`](https://huggingface.co/lynaNSFW/minimaxH3_Collection) | text-to-image | lora, template:diffusion-lora, base_model:pmczip/MiniMaxH3_LoRAs, base_model:adapter:pmczip/MiniMaxH3_LoRAs |
| 2026-08-29 | 2292 | 9 | [`LokkenJP/10Eros_Max_optimized_w4a8_exp_learned`](https://huggingface.co/LokkenJP/10Eros_Max_optimized_w4a8_exp_learned) | image-text-to-video | comfyui, int8, quantization, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-21 | 1761 | 12 | [`Abiray/10Eros-Max-fl2va-Beta2-GGUF`](https://huggingface.co/Abiray/10Eros-Max-fl2va-Beta2-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-27 | 1529 | 0 | [`Wesley1234/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8`](https://huggingface.co/Wesley1234/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |
| 2026-08-23 | 1488 | 7 | [`Abiray/10Eros-Max-ref2va-Beta2-GGUF`](https://huggingface.co/Abiray/10Eros-Max-ref2va-Beta2-GGUF) | image-text-to-video | gguf, comfyui, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-08-16 | 1215 | 22 | [`sakamakismile/10Eros-Max-beta2-NVFP4`](https://huggingface.co/sakamakismile/10Eros-Max-beta2-NVFP4) | image-to-video | nvfp4, comfyui, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-20 | 1182 | 0 | [`vasilerosca891/MiniMax-H3`](https://huggingface.co/vasilerosca891/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-25 | 1006 | 3 | [`berryber09/10Eros-Max-h3-turbo-hybrid-beta3-w4a8`](https://huggingface.co/berryber09/10Eros-Max-h3-turbo-hybrid-beta3-w4a8) | text-to-video | comfyui, quantized, turbo, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-14 | 891 | 134 | [`Smite79/MiniMax-H3-Longvideos`](https://huggingface.co/Smite79/MiniMax-H3-Longvideos) | text-to-video | comfyui, comfyui-nodes, license:other |
| 2026-08-18 | 834 | 186 | [`SexGod1979/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/SexGod1979/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-08-05 | 755 | 420 | [`SexGod1979/PinkCherry_MiniMax-H3`](https://huggingface.co/SexGod1979/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-11 | 219 | 1 | [`ibyteohdear/10Eros-Max-Transformer_TURBO-hybrid_beta5-pruned`](https://huggingface.co/ibyteohdear/10Eros-Max-Transformer_TURBO-hybrid_beta5-pruned) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-07 | 203 | 66 | [`SexGod1979/NaughtyTimes-MiniMax-H3`](https://huggingface.co/SexGod1979/NaughtyTimes-MiniMax-H3) |  | license:apache-2.0 |
| 2026-09-25 | 157 | 0 | [`kalyaskye/h3-loras`](https://huggingface.co/kalyaskye/h3-loras) | minimax-h3 | lora |
| 2026-08-05 | 153 | 100 | [`SexGod1979/PinkFluffyBunny-MiniMax-H3`](https://huggingface.co/SexGod1979/PinkFluffyBunny-MiniMax-H3) |  | license:apache-2.0 |
| 2026-08-22 | 96 | 0 | [`RareConcepts/soad-h3-xm-20260822`](https://huggingface.co/RareConcepts/soad-h3-xm-20260822) | text-to-video | lora, template:sd-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 84 | 0 | [`SimpleTuner/minimaxh3-suno-reggae-rank128`](https://huggingface.co/SimpleTuner/minimaxh3-suno-reggae-rank128) | text-to-video | lora, template:sd-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-21 | 73 | 2 | [`chfm/10Eros-Max-beta2-NVFP4`](https://huggingface.co/chfm/10Eros-Max-beta2-NVFP4) | image-to-video | nvfp4, comfyui, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-09-12 | 64 | 1 | [`ibyteohdear/10Eros-Max-Transformer_TURBO-hybrid_beta5`](https://huggingface.co/ibyteohdear/10Eros-Max-Transformer_TURBO-hybrid_beta5) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-22 | 53 | 0 | [`RareConcepts/soad-h3-nextlat-20260822`](https://huggingface.co/RareConcepts/soad-h3-nextlat-20260822) | text-to-video | lora, template:sd-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-22 | 48 | 0 | [`RareConcepts/soad-h3-nextlat-xm-20260822`](https://huggingface.co/RareConcepts/soad-h3-nextlat-xm-20260822) | text-to-video | lora, template:sd-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-25 | 31 | 0 | [`sisniha/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/sisniha/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-08-22 | 28 | 0 | [`RareConcepts/soad-h3-vanilla-20260822`](https://huggingface.co/RareConcepts/soad-h3-vanilla-20260822) | text-to-video | lora, template:sd-lora, base_model:MiniMaxAI/MiniMax-H3, base_model:adapter:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-13 | 25 | 1 | [`dubUhoo/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/dubUhoo/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-09-19 | 22 | 0 | [`Scorpio1111/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/Scorpio1111/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-09-16 | 20 | 0 | [`coeboy/PinkCherry_MiniMax-H3`](https://huggingface.co/coeboy/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-21 | 20 | 1 | [`sasimi/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/sasimi/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-09-16 | 18 | 0 | [`concil859856/MiniMax-H3-Longvideos`](https://huggingface.co/concil859856/MiniMax-H3-Longvideos) | text-to-video | comfyui, comfyui-nodes, license:other |
| 2026-09-24 | 16 | 1 | [`Imfiilthyfrankdead/AfterMidnight-MiniMax-H3-NSFW`](https://huggingface.co/Imfiilthyfrankdead/AfterMidnight-MiniMax-H3-NSFW) |  | license:apache-2.0 |
| 2026-08-26 | 8 | 0 | [`tonorth1/PinkCherry_MiniMax-H3`](https://huggingface.co/tonorth1/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-08 | 7 | 0 | [`disguisequence/PinkFluffyBunny-MiniMax-H3`](https://huggingface.co/disguisequence/PinkFluffyBunny-MiniMax-H3) |  | license:apache-2.0 |
| 2026-08-11 | 6 | 0 | [`ghjk654/PinkCherry_MiniMax-H3`](https://huggingface.co/ghjk654/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-06 | 5 | 0 | [`TopgunM/PinkFluffyBunny-MiniMax-H3`](https://huggingface.co/TopgunM/PinkFluffyBunny-MiniMax-H3) |  | lora, license:apache-2.0 |
| 2026-08-10 | 5 | 1 | [`erueye/PinkFluffyBunny-MiniMax-H3`](https://huggingface.co/erueye/PinkFluffyBunny-MiniMax-H3) |  | license:apache-2.0 |
| 2026-08-19 | 4 | 0 | [`Jeet070/PinkCherry_MiniMax-H3`](https://huggingface.co/Jeet070/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-13 | 3 | 0 | [`romonlyme/PinkCherry_MiniMax-H3`](https://huggingface.co/romonlyme/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-08 | 0 | 0 | [`1dk123456/PinkCherry_MiniMax-H3`](https://huggingface.co/1dk123456/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-15 | 0 | 2 | [`AiAngelGallery/AiAngelH3`](https://huggingface.co/AiAngelGallery/AiAngelH3) | image-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-23 | 0 | 0 | [`AliceThirty/PinkCherry_MiniMax-H3_pruned_int8_convrot`](https://huggingface.co/AliceThirty/PinkCherry_MiniMax-H3_pruned_int8_convrot) |  | base_model:SexGod1979/PinkCherry_MiniMax-H3, base_model:finetune:SexGod1979/PinkCherry_MiniMax-H3 |
| 2026-09-05 | 0 | 0 | [`Appeltaartman/Minimax_H3-Margot_Robbie`](https://huggingface.co/Appeltaartman/Minimax_H3-Margot_Robbie) |  | license:apache-2.0 |
| 2026-08-08 | 0 | 0 | [`DBPEnAhTR8r/PinkCherry_MiniMax-H3`](https://huggingface.co/DBPEnAhTR8r/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-06 | 0 | 0 | [`DearAzrael/PinkCherry_MiniMax-H3`](https://huggingface.co/DearAzrael/PinkCherry_MiniMax-H3) |  | license:apache-2.0 |
| 2026-09-26 | 0 | 0 | [`DevXCoder2025/10Eros-Max`](https://huggingface.co/DevXCoder2025/10Eros-Max) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 4 | [`DmitryDB/MiniMax-H3-10Eros-Max-DT-sQKV`](https://huggingface.co/DmitryDB/MiniMax-H3-10Eros-Max-DT-sQKV) | image-text-to-video | comfyui, quantization, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 22 | [`DmitryDB/MiniMax-H3-10Eros-Max-Quants`](https://huggingface.co/DmitryDB/MiniMax-H3-10Eros-Max-Quants) | image-text-to-video | comfyui, quantization, int8, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-08 | 0 | 0 | [`EllipsesMark/eromacks`](https://huggingface.co/EllipsesMark/eromacks) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-25 | 0 | 2 | [`JCorcho/10Eros-Max-TURBO-hybrid-beta3-ComfyUI-Quants`](https://huggingface.co/JCorcho/10Eros-Max-TURBO-hybrid-beta3-ComfyUI-Quants) | image-to-video | comfyui, nvfp4, fp8, quantization, nsfw, base_model:TenStrip/10Eros-Max, base_model:quantized:TenStrip/10Eros-Max, license:other |
| 2026-09-09 | 0 | 0 | [`Jhjhhkj65/Minimax_H3-Sydney_Sweeney`](https://huggingface.co/Jhjhhkj65/Minimax_H3-Sydney_Sweeney) |  |  |
| 2026-08-06 | 0 | 0 | [`Kerochake/MiniMax-H3-10Eros-Max-DT-sQKV`](https://huggingface.co/Kerochake/MiniMax-H3-10Eros-Max-DT-sQKV) | image-text-to-video | comfyui, quantization, int8, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 0 | 1 | [`Momoking/PinkCherry_MiniMax-H3`](https://huggingface.co/Momoking/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-14 | 0 | 14 | [`NeuralDreamer/h3ErosMax_beta5_turbo_lora`](https://huggingface.co/NeuralDreamer/h3ErosMax_beta5_turbo_lora) |  |  |
| 2026-08-07 | 0 | 7 | [`Playtime-AI/Minimax-H3_Showcase`](https://huggingface.co/Playtime-AI/Minimax-H3_Showcase) |  | license:apache-2.0 |
| 2026-09-07 | 0 | 3 | [`Playtime-AI/Minimax_H3-Ace_Ventura`](https://huggingface.co/Playtime-AI/Minimax_H3-Ace_Ventura) |  | license:apache-2.0 |
| 2026-09-10 | 0 | 39 | [`Playtime-AI/Minimax_H3-Age_Slider`](https://huggingface.co/Playtime-AI/Minimax_H3-Age_Slider) |  | license:apache-2.0 |
| 2026-09-05 | 0 | 5 | [`Playtime-AI/Minimax_H3-Alan_Rickman`](https://huggingface.co/Playtime-AI/Minimax_H3-Alan_Rickman) |  | license:apache-2.0 |
| 2026-08-31 | 0 | 23 | [`Playtime-AI/Minimax_H3-Anya_Taylor_Joy`](https://huggingface.co/Playtime-AI/Minimax_H3-Anya_Taylor_Joy) |  | license:apache-2.0 |
| 2026-08-29 | 0 | 9 | [`Playtime-AI/Minimax_H3-Ariana_Grande`](https://huggingface.co/Playtime-AI/Minimax_H3-Ariana_Grande) |  | license:apache-2.0 |
| 2026-09-05 | 0 | 2 | [`Playtime-AI/Minimax_H3-Betty_Gilpin`](https://huggingface.co/Playtime-AI/Minimax_H3-Betty_Gilpin) |  | license:apache-2.0 |
| 2026-08-27 | 0 | 4 | [`Playtime-AI/Minimax_H3-Dolly_Parton`](https://huggingface.co/Playtime-AI/Minimax_H3-Dolly_Parton) |  | license:apache-2.0 |
| 2026-08-25 | 0 | 10 | [`Playtime-AI/Minimax_H3-Jennifer_Connelly`](https://huggingface.co/Playtime-AI/Minimax_H3-Jennifer_Connelly) |  | license:apache-2.0 |
| 2026-08-31 | 0 | 3 | [`Playtime-AI/Minimax_H3-Kiernan_Shipka`](https://huggingface.co/Playtime-AI/Minimax_H3-Kiernan_Shipka) |  | license:apache-2.0 |
| 2026-08-26 | 0 | 24 | [`Playtime-AI/Minimax_H3-Margot_Robbie`](https://huggingface.co/Playtime-AI/Minimax_H3-Margot_Robbie) |  | license:apache-2.0 |
| 2026-08-29 | 0 | 57 | [`Playtime-AI/Minimax_H3-Megan_Fox`](https://huggingface.co/Playtime-AI/Minimax_H3-Megan_Fox) |  | license:apache-2.0 |
| 2026-09-07 | 0 | 9 | [`Playtime-AI/Minimax_H3-Mia_Goth`](https://huggingface.co/Playtime-AI/Minimax_H3-Mia_Goth) |  | license:apache-2.0 |
| 2026-08-22 | 0 | 8 | [`Playtime-AI/Minimax_H3-Mila_Kunis`](https://huggingface.co/Playtime-AI/Minimax_H3-Mila_Kunis) |  | license:apache-2.0 |
| 2026-08-31 | 0 | 10 | [`Playtime-AI/Minimax_H3-Millie_Bobby_Brown`](https://huggingface.co/Playtime-AI/Minimax_H3-Millie_Bobby_Brown) |  | license:apache-2.0 |
| 2026-08-31 | 0 | 6 | [`Playtime-AI/Minimax_H3-Milly_Alcock`](https://huggingface.co/Playtime-AI/Minimax_H3-Milly_Alcock) |  | license:apache-2.0 |
| 2026-09-04 | 0 | 3 | [`Playtime-AI/Minimax_H3-Ricky_Gervais`](https://huggingface.co/Playtime-AI/Minimax_H3-Ricky_Gervais) |  | license:apache-2.0 |
| 2026-08-28 | 0 | 10 | [`Playtime-AI/Minimax_H3-Sadie_S`](https://huggingface.co/Playtime-AI/Minimax_H3-Sadie_S) |  | license:apache-2.0 |
| 2026-08-24 | 0 | 11 | [`Playtime-AI/Minimax_H3-Salma_Hayek`](https://huggingface.co/Playtime-AI/Minimax_H3-Salma_Hayek) |  | license:apache-2.0 |
| 2026-09-04 | 0 | 14 | [`Playtime-AI/Minimax_H3-Sasha_Grey`](https://huggingface.co/Playtime-AI/Minimax_H3-Sasha_Grey) |  | license:apache-2.0 |
| 2026-08-24 | 0 | 111 | [`Playtime-AI/Minimax_H3-Sydney_Sweeney`](https://huggingface.co/Playtime-AI/Minimax_H3-Sydney_Sweeney) |  | license:apache-2.0 |
| 2026-09-03 | 0 | 4 | [`Playtime-AI/Minimax_H3-The_Dude-Jeff_Bridges`](https://huggingface.co/Playtime-AI/Minimax_H3-The_Dude-Jeff_Bridges) |  | license:apache-2.0 |
| 2026-09-01 | 0 | 14 | [`Playtime-AI/Minimax_H3-Titty_Drop`](https://huggingface.co/Playtime-AI/Minimax_H3-Titty_Drop) |  | license:apache-2.0 |
| 2026-08-28 | 0 | 8 | [`Playtime-AI/Minimax_H3-Titty_Drop_I2V`](https://huggingface.co/Playtime-AI/Minimax_H3-Titty_Drop_I2V) |  | license:apache-2.0 |
| 2026-08-27 | 0 | 13 | [`Playtime-AI/Minimax_H3-Zendaya`](https://huggingface.co/Playtime-AI/Minimax_H3-Zendaya) |  | license:apache-2.0 |
| 2026-08-09 | 0 | 0 | [`Rb227715/PinkCherry_MiniMax-H3`](https://huggingface.co/Rb227715/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-23 | 0 | 0 | [`RunningHubAI/rh-10eros-max-h3-fl2va-beta1-pruned-unet`](https://huggingface.co/RunningHubAI/rh-10eros-max-h3-fl2va-beta1-pruned-unet) |  |  |
| 2026-09-24 | 0 | 0 | [`RunningHubAI/rh-10eros-max-h3-fl2va-pruned-int8-convrot-unet`](https://huggingface.co/RunningHubAI/rh-10eros-max-h3-fl2va-pruned-int8-convrot-unet) | text-to-video | comfyui |
| 2026-09-29 | 0 | 0 | [`RunningHubAI/rh-10eros-max-h3-turbo-hybrid-beta3-int8-convrot-unet`](https://huggingface.co/RunningHubAI/rh-10eros-max-h3-turbo-hybrid-beta3-int8-convrot-unet) | text-to-video | comfyui |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-h3jiggle-tit-physics-lora`](https://huggingface.co/RunningHubAI/rh-h3jiggle-tit-physics-lora) |  | comfyui, lora |
| 2026-09-23 | 0 | 0 | [`RunningHubAI/rh-h3nsfwlora-lora`](https://huggingface.co/RunningHubAI/rh-h3nsfwlora-lora) |  | comfyui, lora |
| 2026-09-26 | 0 | 0 | [`RunningHubAI/rh-h3nsfwlora-lora-2096782313941434370`](https://huggingface.co/RunningHubAI/rh-h3nsfwlora-lora-2096782313941434370) |  | comfyui, lora |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-astro-nsfw-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-astro-nsfw-lora) |  | comfyui, lora |
| 2026-09-23 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-10erosmax-beta1-pruned-compat-v001-t8-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-fl2v-turbo-8step-v1.0-10erosmax-beta1-pruned-compat-v001-t8-lora) |  | comfyui, lora |
| 2026-09-23 | 0 | 0 | [`RunningHubAI/rh-minimax-h3-turbo-4step-10erosmax-test4-pruned-curveproj1025-exp-v001-t8-lora`](https://huggingface.co/RunningHubAI/rh-minimax-h3-turbo-4step-10erosmax-test4-pruned-curveproj1025-exp-v001-t8-lora) |  | comfyui, lora |
| 2026-09-28 | 0 | 0 | [`RunningHubAI/rh-minimaxh3-dasiwa-10eros-hybird-8steps-turbo-lora`](https://huggingface.co/RunningHubAI/rh-minimaxh3-dasiwa-10eros-hybird-8steps-turbo-lora) |  | comfyui, lora |
| 2026-08-18 | 0 | 4 | [`Stuubs/10eros_Max_Ref2va`](https://huggingface.co/Stuubs/10eros_Max_Ref2va) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 0 | 703 | [`TenStrip/10Eros-Max`](https://huggingface.co/TenStrip/10Eros-Max) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 0 | 0 | [`Zxsry/PinkCherry_MiniMax-H3`](https://huggingface.co/Zxsry/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-23 | 0 | 1 | [`chfm/10Eros-Max-h3-int8-convrot`](https://huggingface.co/chfm/10Eros-Max-h3-int8-convrot) | comfyui | comfyui, int8, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-14 | 0 | 130 | [`cicalooo/10Eros-Max-h3-int8-convrot`](https://huggingface.co/cicalooo/10Eros-Max-h3-int8-convrot) | comfyui | comfyui, int8, base_model:TenStrip/10Eros-Max, base_model:finetune:TenStrip/10Eros-Max, license:other |
| 2026-08-05 | 0 | 2 | [`disguisequence/MiniMax-H3-10Eros-Max-Quants`](https://huggingface.co/disguisequence/MiniMax-H3-10Eros-Max-Quants) | image-text-to-video | comfyui, quantization, int8, nvfp4, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 0 | 1 | [`disguisequence/PinkCherry_MiniMax-H3`](https://huggingface.co/disguisequence/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-08 | 0 | 0 | [`h35656566/10Eros-Max`](https://huggingface.co/h35656566/10Eros-Max) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-25 | 0 | 2 | [`h35656566/10Eros-Max-old1`](https://huggingface.co/h35656566/10Eros-Max-old1) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 0 | 0 | [`hollyw12xw3f/PinkCherry_MiniMax-H3`](https://huggingface.co/hollyw12xw3f/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-04 | 0 | 0 | [`kunalmiind/10Eros-Max`](https://huggingface.co/kunalmiind/10Eros-Max) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-09 | 0 | 1 | [`laoda/DasiwaMinimaxH3_dasiwaHybrid8turboV1`](https://huggingface.co/laoda/DasiwaMinimaxH3_dasiwaHybrid8turboV1) | text-to-video | comfyui |
| 2026-08-08 | 0 | 0 | [`lessxc/PinkCherry_MiniMax-H3-backup`](https://huggingface.co/lessxc/PinkCherry_MiniMax-H3-backup) | text-to-video | license:apache-2.0 |
| 2026-09-16 | 0 | 0 | [`marin73tomas/minimax-h3-teneros-faststart-20260916`](https://huggingface.co/marin73tomas/minimax-h3-teneros-faststart-20260916) |  |  |
| 2026-08-06 | 0 | 1 | [`maximsobolev275/PinkCherry-H3-lora-r768-convrot`](https://huggingface.co/maximsobolev275/PinkCherry-H3-lora-r768-convrot) |  |  |
| 2026-08-07 | 0 | 1 | [`maximsobolev275/PinkCherry-a3-H3-lora-r256-convrot`](https://huggingface.co/maximsobolev275/PinkCherry-a3-H3-lora-r256-convrot) |  |  |
| 2026-08-09 | 0 | 0 | [`maximsobolev275/PinkCherry-a5-H3-lora-r768-convrot`](https://huggingface.co/maximsobolev275/PinkCherry-a5-H3-lora-r768-convrot) |  |  |
| 2026-08-13 | 0 | 2 | [`maximsobolev275/PinkCherry-b6-H3-lora-r768-convrot`](https://huggingface.co/maximsobolev275/PinkCherry-b6-H3-lora-r768-convrot) |  |  |
| 2026-08-22 | 0 | 0 | [`musafa901/10Eros-Max`](https://huggingface.co/musafa901/10Eros-Max) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-01 | 0 | 2 | [`nutboyai/minimaxH3-NSFW`](https://huggingface.co/nutboyai/minimaxH3-NSFW) |  |  |
| 2026-08-30 | 0 | 3 | [`nutboyai/minimaxH3-loras-NSFW`](https://huggingface.co/nutboyai/minimaxH3-loras-NSFW) |  |  |
| 2026-09-23 | 0 | 0 | [`rdvl89/blowjob-minimaxh3`](https://huggingface.co/rdvl89/blowjob-minimaxh3) |  | license:apache-2.0 |
| 2026-08-09 | 0 | 0 | [`sSANCHESs/PinkCherry_MiniMax-H3`](https://huggingface.co/sSANCHESs/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-08-08 | 0 | 1 | [`sandaisnot/PinkCherry_MiniMax-H3`](https://huggingface.co/sandaisnot/PinkCherry_MiniMax-H3) | text-to-video | license:apache-2.0 |
| 2026-09-04 | 0 | 6 | [`t8star/MinimaxH3-Dasiwa-10eros-hybird-8steps-turbo`](https://huggingface.co/t8star/MinimaxH3-Dasiwa-10eros-hybird-8steps-turbo) |  |  |
| 2026-08-10 | 0 | 18 | [`t8star/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8`](https://huggingface.co/t8star/minimax_h3_turbo_4step_10ErosMax_test4_pruned_curveproj1025_T8) | text-to-video | lora, comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:adapter:Comfy-Org/MiniMax-H3, license:other |

### 13-微调合并实验

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-09-05 | 462956 | 698 | [`WarmBloodAban/Minimax-h3_Singularity`](https://huggingface.co/WarmBloodAban/Minimax-h3_Singularity) | image-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:apache-2.0 |
| 2026-09-03 | 29469 | 21 | [`t8star/Vdn-Minimax-H3-Comfy`](https://huggingface.co/t8star/Vdn-Minimax-H3-Comfy) | text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-31 | 5226 | 3 | [`taurusduan/MiniMax-H3`](https://huggingface.co/taurusduan/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-02 | 1531 | 319 | [`OpenVDN/vdn-minimax-h3`](https://huggingface.co/OpenVDN/vdn-minimax-h3) | text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 1307 | 13 | [`Hippotes/MiniMax-H3-Experiments`](https://huggingface.co/Hippotes/MiniMax-H3-Experiments) | diffusers | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-11 | 1163 | 0 | [`EllipsesMark/Minimax-h3_Singularity`](https://huggingface.co/EllipsesMark/Minimax-h3_Singularity) | image-to-video | comfyui, license:apache-2.0 |
| 2026-09-02 | 804 | 0 | [`wsxxxx/MiniMax-H3`](https://huggingface.co/wsxxxx/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-03 | 623 | 0 | [`kevin-mi/VDN-H3-overlay`](https://huggingface.co/kevin-mi/VDN-H3-overlay) | minimax-h3 | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 529 | 0 | [`Zidane29/MiniMax-H3`](https://huggingface.co/Zidane29/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 489 | 0 | [`comfy-playflock/MiniMax-H3`](https://huggingface.co/comfy-playflock/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-18 | 483 | 0 | [`wangpj/MiniMax-H3_dit_bf16`](https://huggingface.co/wangpj/MiniMax-H3_dit_bf16) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 405 | 0 | [`KENIC-1/Comfy-Org-MiniMax-H3`](https://huggingface.co/KENIC-1/Comfy-Org-MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-05 | 392 | 0 | [`EllipsesMark/MiniMax-H3-ComfyUI`](https://huggingface.co/EllipsesMark/MiniMax-H3-ComfyUI) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-24 | 340 | 0 | [`TechnoBaptist/MiniMax-H3-x-Z-Image-native`](https://huggingface.co/TechnoBaptist/MiniMax-H3-x-Z-Image-native) | text-to-video | comfyui, comfy-native, comfy-quant, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-29 | 243 | 0 | [`exefg/hypium-h3-ref2va-prod-v1`](https://huggingface.co/exefg/hypium-h3-ref2va-prod-v1) | minimax-h3 | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-23 | 220 | 0 | [`Gyvin/MiniMax-H3`](https://huggingface.co/Gyvin/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-18 | 218 | 0 | [`fkyyy/MiniMax-H3-comfy-slim`](https://huggingface.co/fkyyy/MiniMax-H3-comfy-slim) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-06 | 181 | 0 | [`sunnyyy/MiniMax-H3`](https://huggingface.co/sunnyyy/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-30 | 170 | 0 | [`serieuxalphonse/MiniMax-H3`](https://huggingface.co/serieuxalphonse/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-10 | 156 | 0 | [`terryway246/MiniMax-H3`](https://huggingface.co/terryway246/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-10 | 123 | 1 | [`ibyteohdear/MiniMax-H3-LightX8-Fused-fl2v`](https://huggingface.co/ibyteohdear/MiniMax-H3-LightX8-Fused-fl2v) | image-text-to-video | license:other |
| 2026-08-13 | 113 | 0 | [`Fanw/MiniMax-H3`](https://huggingface.co/Fanw/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-26 | 109 | 0 | [`Lei0513abc/MiniMax-H3`](https://huggingface.co/Lei0513abc/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-16 | 100 | 1 | [`musafa901/MiniMax-H3-Comfy_20260816`](https://huggingface.co/musafa901/MiniMax-H3-Comfy_20260816) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-08 | 88 | 0 | [`gigafreeze/MiniMax-H3`](https://huggingface.co/gigafreeze/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-19 | 86 | 0 | [`musafa901/MiniMax-H3-Comfy_20260820`](https://huggingface.co/musafa901/MiniMax-H3-Comfy_20260820) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 79 | 0 | [`qb1222090/MiniMax-H3`](https://huggingface.co/qb1222090/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-12 | 63 | 0 | [`kotoriri/MiniMax-H3`](https://huggingface.co/kotoriri/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-18 | 60 | 0 | [`keyyj/MiniMax-H3`](https://huggingface.co/keyyj/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-09 | 48 | 2 | [`tiny-random/minimax-h3`](https://huggingface.co/tiny-random/minimax-h3) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-08-09 | 33 | 1 | [`yujiepan/minimax-h3-tiny-random`](https://huggingface.co/yujiepan/minimax-h3-tiny-random) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-09-14 | 23 | 0 | [`Stonerao/MiniMax-H3`](https://huggingface.co/Stonerao/MiniMax-H3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 10 | 2 | [`WaveCut/MiniMax-H3-OrbitQuant-W4A4`](https://huggingface.co/WaveCut/MiniMax-H3-OrbitQuant-W4A4) | image-text-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-03 | 6 | 0 | [`ovedrive/MiniMax-H3-generator-bf16`](https://huggingface.co/ovedrive/MiniMax-H3-generator-bf16) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-16 | 2 | 181 | [`XGENlabs/XGEN-JING`](https://huggingface.co/XGENlabs/XGEN-JING) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 1 | [`7FSxDjZMUR/gogo-meme-minimax-h3-comfy-bundle`](https://huggingface.co/7FSxDjZMUR/gogo-meme-minimax-h3-comfy-bundle) |  | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-28 | 0 | 0 | [`EllipsesMark/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/EllipsesMark/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-25 | 0 | 28 | [`FX-FeiHou/MiniMax-H3-Remix`](https://huggingface.co/FX-FeiHou/MiniMax-H3-Remix) | image-to-video | comfyui, license:other |
| 2026-08-11 | 0 | 77 | [`Inner-Reflections/MiniMax-H3-Looping-Sketch-Anime`](https://huggingface.co/Inner-Reflections/MiniMax-H3-Looping-Sketch-Anime) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3 |
| 2026-09-08 | 0 | 0 | [`Jackxuanxuan/MiniMax-H3-experimental`](https://huggingface.co/Jackxuanxuan/MiniMax-H3-experimental) |  |  |
| 2026-08-08 | 0 | 0 | [`Momoking/MiniMax-H3-experimental`](https://huggingface.co/Momoking/MiniMax-H3-experimental) |  |  |
| 2026-08-19 | 0 | 2 | [`OREDDoug18792/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/OREDDoug18792/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-03 | 0 | 82 | [`Plaguekind/Minimax-H3`](https://huggingface.co/Plaguekind/Minimax-H3) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:mit |
| 2026-08-29 | 0 | 0 | [`PlatypusDevice/minimax-h3-ref2va-runtime`](https://huggingface.co/PlatypusDevice/minimax-h3-ref2va-runtime) | image-to-video | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-09-28 | 0 | 0 | [`SEVUNX/minimax_H3_merged`](https://huggingface.co/SEVUNX/minimax_H3_merged) |  |  |
| 2026-08-23 | 0 | 5 | [`Smite79/MiniMax-H3-Tape-FX`](https://huggingface.co/Smite79/MiniMax-H3-Tape-FX) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:mit |
| 2026-08-08 | 0 | 0 | [`aria220/MiniMax-H3-experimental`](https://huggingface.co/aria220/MiniMax-H3-experimental) |  |  |
| 2026-09-01 | 0 | 5 | [`diobrando0/MiniMax-H3-fl2va-ref2va-hybrids-bf16`](https://huggingface.co/diobrando0/MiniMax-H3-fl2va-ref2va-hybrids-bf16) | text-to-video | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:merge:Comfy-Org/MiniMax-H3, base_model:MiniMaxAI/MiniMax-H3, base_model:merge:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-05 | 0 | 0 | [`drowzeys/keys-heretic-MiniMax-H3-sol-engine-more-DGX-Spark-weights`](https://huggingface.co/drowzeys/keys-heretic-MiniMax-H3-sol-engine-more-DGX-Spark-weights) |  | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-08-07 | 0 | 0 | [`gmpNora/MMH3`](https://huggingface.co/gmpNora/MMH3) | diffusion-single-file | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-12 | 0 | 6 | [`lihaoyun6/MiniMax-H3-Ref-Patch`](https://huggingface.co/lihaoyun6/MiniMax-H3-Ref-Patch) |  | base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:apache-2.0 |
| 2026-09-20 | 0 | 0 | [`liskasYR/XGEN-JING`](https://huggingface.co/liskasYR/XGEN-JING) | image-text-to-video | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-11 | 0 | 4 | [`model-hub-nd/h3-merged`](https://huggingface.co/model-hub-nd/h3-merged) |  | comfyui, base_model:Comfy-Org/MiniMax-H3, base_model:finetune:Comfy-Org/MiniMax-H3, license:other |
| 2026-09-12 | 0 | 1 | [`qq2845547190/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/qq2845547190/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-11 | 0 | 308 | [`smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/smhfacct/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-04 | 0 | 1 | [`ssjenforcer191/Homelander_Minimax_H3_experimental`](https://huggingface.co/ssjenforcer191/Homelander_Minimax_H3_experimental) |  |  |
| 2026-08-15 | 0 | 3 | [`taxexempt/Custom-MiniMaX-H3-mixed-quants`](https://huggingface.co/taxexempt/Custom-MiniMaX-H3-mixed-quants) |  | base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3 |
| 2026-09-10 | 0 | 0 | [`tttaini/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/tttaini/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-09-03 | 0 | 1 | [`yantongrui/Minimax-H3-fl2va-ref2va-hybrid-models`](https://huggingface.co/yantongrui/Minimax-H3-fl2va-ref2va-hybrid-models) | text-to-video | license:other |
| 2026-08-05 | 0 | 0 | [`yemsrach3723/MiniMax-H3`](https://huggingface.co/yemsrach3723/MiniMax-H3) |  | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |

### 14-工作流工具箱

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-08-04 | 241 | 77 | [`joeygambino/MiniMax-H3-Multishot-Workflow`](https://huggingface.co/joeygambino/MiniMax-H3-Multishot-Workflow) | text-to-video | comfyui, license:apache-2.0 |
| 2026-09-19 | 48 | 11 | [`LaDruid/MiniMax-H3-Multishot-Workflow`](https://huggingface.co/LaDruid/MiniMax-H3-Multishot-Workflow) | text-to-video | comfyui, license:apache-2.0 |
| 2026-08-05 | 0 | 1 | [`Cybronya/minimax-h3-toolkit`](https://huggingface.co/Cybronya/minimax-h3-toolkit) |  | license:apache-2.0 |
| 2026-09-12 | 0 | 0 | [`Jackxuanxuan/minimax-h3-toolkit`](https://huggingface.co/Jackxuanxuan/minimax-h3-toolkit) |  | license:apache-2.0 |
| 2026-08-07 | 0 | 1 | [`JahJedi/MiniMax-H3-QJ-Riverfield-Workflow`](https://huggingface.co/JahJedi/MiniMax-H3-QJ-Riverfield-Workflow) |  |  |
| 2026-08-09 | 0 | 195 | [`PoopMan333/H3_Character_Sheet_Generator`](https://huggingface.co/PoopMan333/H3_Character_Sheet_Generator) | image-to-image | comfyui, license:other |
| 2026-09-02 | 0 | 22 | [`PoopMan333/H3_Easy_Ref2V_Workflow`](https://huggingface.co/PoopMan333/H3_Easy_Ref2V_Workflow) | video-to-video | comfyui, license:other |
| 2026-08-13 | 0 | 2 | [`QrusherZA/MiniMax-H3-Workflow`](https://huggingface.co/QrusherZA/MiniMax-H3-Workflow) |  |  |
| 2026-08-28 | 0 | 32 | [`RuneXX/Minimax-H3-Workflows`](https://huggingface.co/RuneXX/Minimax-H3-Workflows) | image-to-video | comfy, comfyui |
| 2026-08-27 | 0 | 2 | [`StefanFalkok/Minimax_H3_Workflows`](https://huggingface.co/StefanFalkok/Minimax_H3_Workflows) |  | license:apache-2.0 |
| 2026-08-25 | 0 | 2 | [`SwagMessiah100/H3_Character_Sheet_Generator`](https://huggingface.co/SwagMessiah100/H3_Character_Sheet_Generator) | image-to-image | comfyui, license:other |
| 2026-09-07 | 0 | 2 | [`jayseanbrambila/minimax-h3-prompt-workflow-toolkit`](https://huggingface.co/jayseanbrambila/minimax-h3-prompt-workflow-toolkit) | image-to-video | license:apache-2.0 |
| 2026-08-05 | 0 | 4 | [`joeygambino/MiniMax-H3-HardMode-Workflow`](https://huggingface.co/joeygambino/MiniMax-H3-HardMode-Workflow) |  | comfyui, base_model:MiniMaxAI/MiniMax-H3, base_model:finetune:MiniMaxAI/MiniMax-H3, license:other |
| 2026-08-04 | 0 | 3 | [`reverentelusarca/minimax-h3-comfyui-workflows`](https://huggingface.co/reverentelusarca/minimax-h3-comfyui-workflows) |  | license:other |
| 2026-08-15 | 0 | 0 | [`zuanfilm/H3_Minimax_res2s_rkmk2e_Workflow`](https://huggingface.co/zuanfilm/H3_Minimax_res2s_rkmk2e_Workflow) | image-to-video | comfyui, license:mit |

### 15-镜像转载与其它

| 创建日 | 下载量 | Likes | 仓库 | 管线/库 | 标签摘要 |
| --- | ---: | ---: | --- | --- | --- |
| 2026-09-17 | 159281 | 0 | [`AiAngelGallery/ComfyPod-Models`](https://huggingface.co/AiAngelGallery/ComfyPod-Models) | minimax-h3 | comfyui, license:other |
| 2026-08-21 | 4765 | 8 | [`jasperz111/redcraft-minimax-h3-a2a-redmix`](https://huggingface.co/jasperz111/redcraft-minimax-h3-a2a-redmix) | minimax-h3 | comfyui |
| 2026-08-30 | 2041 | 1 | [`beike97/MiniMax-H3`](https://huggingface.co/beike97/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-27 | 2001 | 0 | [`ljt520lxy/MiniMax-H3`](https://huggingface.co/ljt520lxy/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-21 | 1641 | 0 | [`Aun1236/MiniMax-H3`](https://huggingface.co/Aun1236/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-02 | 1339 | 0 | [`star08/MiniMax-H3`](https://huggingface.co/star08/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-24 | 1223 | 0 | [`hjshus/MiniMax-H3`](https://huggingface.co/hjshus/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-23 | 1167 | 0 | [`shablyx666/MiniMax-H3`](https://huggingface.co/shablyx666/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-11 | 1162 | 0 | [`jon52638973/MiniMax-H3`](https://huggingface.co/jon52638973/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-09 | 1158 | 1 | [`Rurbino/MiniMax-H3`](https://huggingface.co/Rurbino/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-23 | 964 | 0 | [`Royalrajat1230/MiniMax-H3`](https://huggingface.co/Royalrajat1230/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-24 | 923 | 0 | [`fkyyy/MiniMax-H3-slim`](https://huggingface.co/fkyyy/MiniMax-H3-slim) | image-text-to-video | license:other |
| 2026-09-05 | 904 | 0 | [`xiaogongshou/MiniMax-H3`](https://huggingface.co/xiaogongshou/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-27 | 886 | 0 | [`Deepdive404-3/MiniMax-H3`](https://huggingface.co/Deepdive404-3/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-01 | 646 | 0 | [`skySakir/MiniMax-H3`](https://huggingface.co/skySakir/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-01 | 632 | 0 | [`saluca-labs/MiniMax-H3`](https://huggingface.co/saluca-labs/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-15 | 624 | 0 | [`MHWJJ/MiniMax-H3`](https://huggingface.co/MHWJJ/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-27 | 509 | 0 | [`mrlol123/MiniMax-H3`](https://huggingface.co/mrlol123/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-03 | 496 | 1 | [`wudingdeet/MiniMax-H3`](https://huggingface.co/wudingdeet/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 491 | 0 | [`A1Azmi/MiniMax-H3`](https://huggingface.co/A1Azmi/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-13 | 462 | 0 | [`burningfeet/MiniMax-H3`](https://huggingface.co/burningfeet/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-31 | 430 | 0 | [`nyxtesla/MiniMax-H3`](https://huggingface.co/nyxtesla/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-16 | 381 | 1 | [`musafa901/MiniMax-H3_20260816`](https://huggingface.co/musafa901/MiniMax-H3_20260816) | image-text-to-video | license:other |
| 2026-08-27 | 262 | 1 | [`BIGJUTT/MiniMax-H3`](https://huggingface.co/BIGJUTT/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-15 | 237 | 0 | [`JNcharkey1/MiniMax-H3`](https://huggingface.co/JNcharkey1/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-22 | 230 | 0 | [`FrankensteinSim/MiniMax-H3`](https://huggingface.co/FrankensteinSim/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-30 | 227 | 0 | [`CosminDM/MiniMax-H3`](https://huggingface.co/CosminDM/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-22 | 219 | 0 | [`misstoyou/MiniMax-H3`](https://huggingface.co/misstoyou/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 207 | 0 | [`Stim748/MiniMax-H3`](https://huggingface.co/Stim748/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-18 | 205 | 0 | [`LILUMY/MiniMax-H3`](https://huggingface.co/LILUMY/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-22 | 191 | 0 | [`zhanglangdawang/MiniMax-H3`](https://huggingface.co/zhanglangdawang/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-18 | 180 | 0 | [`lin929/MiniMax-H3`](https://huggingface.co/lin929/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-27 | 174 | 0 | [`aleksyuk/h3-comfy-video`](https://huggingface.co/aleksyuk/h3-comfy-video) | minimax-h3 | comfyui, license:other |
| 2026-08-26 | 170 | 0 | [`puterijessica/MiniMax-H3`](https://huggingface.co/puterijessica/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-19 | 169 | 0 | [`Nadun29/MiniMax-H3`](https://huggingface.co/Nadun29/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-14 | 163 | 0 | [`Lite01385/MiniMax-H3`](https://huggingface.co/Lite01385/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-16 | 147 | 0 | [`Wvkmsv/MiniMax-H3`](https://huggingface.co/Wvkmsv/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 134 | 0 | [`abenliao/minimax-h3-ref2va-transformer-bf16`](https://huggingface.co/abenliao/minimax-h3-ref2va-transformer-bf16) | diffusers |  |
| 2026-08-28 | 132 | 0 | [`Archfiendgaming/MiniMax-H3`](https://huggingface.co/Archfiendgaming/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-26 | 127 | 0 | [`jinjiyoshi/MiniMax-H3`](https://huggingface.co/jinjiyoshi/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 125 | 23 | [`unsloth/MiniMax-H3`](https://huggingface.co/unsloth/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-25 | 119 | 0 | [`Exmanq/MiniMax-H3`](https://huggingface.co/Exmanq/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-18 | 119 | 0 | [`baselquants/MiniMax-H3`](https://huggingface.co/baselquants/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-21 | 112 | 0 | [`CRullo/MiniMax-H3`](https://huggingface.co/CRullo/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-21 | 104 | 0 | [`saramara/MiniMax-H3`](https://huggingface.co/saramara/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-28 | 83 | 0 | [`alexterieur2026/MiniMax-H3`](https://huggingface.co/alexterieur2026/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-24 | 79 | 0 | [`1ST-PLACE-WINNER/MiniMax-H3`](https://huggingface.co/1ST-PLACE-WINNER/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-01 | 74 | 0 | [`diffusers-internal-dev/tiny-minimax-h3-modular-pipe`](https://huggingface.co/diffusers-internal-dev/tiny-minimax-h3-modular-pipe) | diffusers |  |
| 2026-09-25 | 53 | 0 | [`baharedorsa/MiniMax-H3`](https://huggingface.co/baharedorsa/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-26 | 49 | 0 | [`Zane91/MiniMax-H3`](https://huggingface.co/Zane91/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 29 | 0 | [`AgentAnon/MiniMax-H3`](https://huggingface.co/AgentAnon/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-12 | 26 | 0 | [`vs4vijay/MiniMax-H3`](https://huggingface.co/vs4vijay/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-08 | 22 | 0 | [`laoK888/MiniMax-H3`](https://huggingface.co/laoK888/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 19 | 0 | [`MJlohfg/MiniMax-H3`](https://huggingface.co/MJlohfg/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 19 | 0 | [`kg1965/MiniMax-H3`](https://huggingface.co/kg1965/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 18 | 1 | [`Inkdhostile/MiniMax-H3`](https://huggingface.co/Inkdhostile/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 17 | 0 | [`Xdp99/MiniMax-H3`](https://huggingface.co/Xdp99/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 16 | 0 | [`Athena1433/MiniMax-H3`](https://huggingface.co/Athena1433/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 16 | 0 | [`gubernac/MiniMax-H3`](https://huggingface.co/gubernac/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-06 | 16 | 0 | [`marchkamal51/MiniMax-H3`](https://huggingface.co/marchkamal51/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-12 | 16 | 0 | [`wo1808401/MiniMax-H3`](https://huggingface.co/wo1808401/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-10 | 15 | 0 | [`DeepDive404-2/MiniMax-H3`](https://huggingface.co/DeepDive404-2/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-05 | 15 | 0 | [`rayrickypp/MiniMax-H3`](https://huggingface.co/rayrickypp/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-28 | 14 | 0 | [`Efficient-Large-Model/SoL-Refiner-LTX-2.5-for-MiniMax-H3`](https://huggingface.co/Efficient-Large-Model/SoL-Refiner-LTX-2.5-for-MiniMax-H3) | diffusers |  |
| 2026-08-08 | 14 | 0 | [`ZIYOU99/MiniMax-H3`](https://huggingface.co/ZIYOU99/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 14 | 0 | [`alituvalu/MiniMax-H3`](https://huggingface.co/alituvalu/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-03 | 13 | 0 | [`LinYunPRO/MiniMax-H3`](https://huggingface.co/LinYunPRO/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-06 | 13 | 0 | [`Obong128/MiniMax-H3`](https://huggingface.co/Obong128/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-10 | 13 | 0 | [`anlessparky/MiniMax-H3`](https://huggingface.co/anlessparky/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-04 | 13 | 0 | [`multimodalart/minimax-h3-aoti`](https://huggingface.co/multimodalart/minimax-h3-aoti) | minimax-h3 | license:other |
| 2026-08-12 | 12 | 0 | [`Elitetotem/MiniMax-H3`](https://huggingface.co/Elitetotem/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 12 | 0 | [`QVQsdaa/MiniMax-H3`](https://huggingface.co/QVQsdaa/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 12 | 0 | [`Xxjbn/MiniMax-H3`](https://huggingface.co/Xxjbn/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-11 | 12 | 0 | [`astonzhang/MiniMax-H3`](https://huggingface.co/astonzhang/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-09 | 12 | 0 | [`johnsonhuggingapi/MiniMax-H3`](https://huggingface.co/johnsonhuggingapi/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 12 | 0 | [`kingsoul0018/MiniMax-H3`](https://huggingface.co/kingsoul0018/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-11 | 11 | 0 | [`Zain0611/MiniMax-H3`](https://huggingface.co/Zain0611/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-08 | 11 | 0 | [`chiharoong/MiniMax-H3`](https://huggingface.co/chiharoong/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-08 | 11 | 0 | [`hvcgvvgg7/MiniMax-H3`](https://huggingface.co/hvcgvvgg7/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-06 | 11 | 0 | [`maplewoohoooyeah/MiniMax-H3`](https://huggingface.co/maplewoohoooyeah/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-12 | 10 | 0 | [`AnnaRa/MiniMax-H3`](https://huggingface.co/AnnaRa/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-05 | 10 | 0 | [`Terminus404/MiniMax-H3`](https://huggingface.co/Terminus404/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-11 | 10 | 0 | [`liskasYR/MiniMax-H3`](https://huggingface.co/liskasYR/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-10 | 10 | 0 | [`nahxa/MiniMax-H3`](https://huggingface.co/nahxa/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-05 | 10 | 0 | [`yemsrach3723/MiniMax-H3-new`](https://huggingface.co/yemsrach3723/MiniMax-H3-new) | image-text-to-video | license:other |
| 2026-08-25 | 9 | 0 | [`Exmanq/minimax-h3-aoti`](https://huggingface.co/Exmanq/minimax-h3-aoti) | minimax-h3 | license:other |
| 2026-08-11 | 9 | 0 | [`damiang/minimax-h3-ref2va-runpod`](https://huggingface.co/damiang/minimax-h3-ref2va-runpod) | image-text-to-video | license:other |
| 2026-08-05 | 9 | 0 | [`qqceqqq/MiniMax-H3`](https://huggingface.co/qqceqqq/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-02 | 8 | 0 | [`TheMindExpansionNetwork/m1nd3xp4nd3r_Minimax_H3_T2V`](https://huggingface.co/TheMindExpansionNetwork/m1nd3xp4nd3r_Minimax_H3_T2V) |  |  |
| 2026-08-03 | 7 | 0 | [`paulcoronel/MiniMax-H3`](https://huggingface.co/paulcoronel/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-03 | 7 | 0 | [`thanyathon/MiniMax-H3`](https://huggingface.co/thanyathon/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-02 | 6 | 0 | [`TheMindExpansionNetwork/BudNSpud_T2V_Minimax_H3_v1`](https://huggingface.co/TheMindExpansionNetwork/BudNSpud_T2V_Minimax_H3_v1) |  |  |
| 2026-09-03 | 6 | 0 | [`TheMindExpansionNetwork/fyr3_t2v_minimax_h3_v2`](https://huggingface.co/TheMindExpansionNetwork/fyr3_t2v_minimax_h3_v2) |  |  |
| 2026-09-03 | 6 | 0 | [`TheMindExpansionNetwork/worldweaver_t2v_Minimax_H3_v2`](https://huggingface.co/TheMindExpansionNetwork/worldweaver_t2v_Minimax_H3_v2) |  |  |
| 2026-08-03 | 6 | 0 | [`greenslime/MiniMax-H3`](https://huggingface.co/greenslime/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-03 | 5 | 0 | [`Simplismart/MiniMax-H3`](https://huggingface.co/Simplismart/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-03 | 5 | 0 | [`TheMindExpansionNetwork/stawberryman_t2v_Minimax_H3_v2`](https://huggingface.co/TheMindExpansionNetwork/stawberryman_t2v_Minimax_H3_v2) |  |  |
| 2026-09-28 | 2 | 0 | [`ZeyuLing/HFTrainer-MiniMax-H3-Base-FL2VA`](https://huggingface.co/ZeyuLing/HFTrainer-MiniMax-H3-Base-FL2VA) | text-to-video | license:other |
| 2026-08-21 | 0 | 1 | [`0v0o0w0/MinimaxH3_Actions`](https://huggingface.co/0v0o0w0/MinimaxH3_Actions) |  |  |
| 2026-08-03 | 0 | 0 | [`727dcdxd/minimax-h3`](https://huggingface.co/727dcdxd/minimax-h3) |  | license:mit |
| 2026-08-05 | 0 | 34 | [`AiNinja94/MiniMax-H3`](https://huggingface.co/AiNinja94/MiniMax-H3) |  |  |
| 2026-09-20 | 0 | 0 | [`Andri1987/FaceSwap_MiniMaxH3_REF2VA`](https://huggingface.co/Andri1987/FaceSwap_MiniMaxH3_REF2VA) |  | license:apache-2.0 |
| 2026-08-17 | 0 | 1 | [`Bolt-367/minimax-h3-serverless`](https://huggingface.co/Bolt-367/minimax-h3-serverless) |  |  |
| 2026-08-15 | 0 | 0 | [`Buonomo/MiniMax-H3-Slim`](https://huggingface.co/Buonomo/MiniMax-H3-Slim) |  |  |
| 2026-08-27 | 0 | 1 | [`Dcbuilder831/MiniMax-H3-Longvideos`](https://huggingface.co/Dcbuilder831/MiniMax-H3-Longvideos) | text-to-video | comfyui |
| 2026-08-06 | 0 | 62 | [`EllaPriest45/MinimaxH3_Actions`](https://huggingface.co/EllaPriest45/MinimaxH3_Actions) |  |  |
| 2026-08-18 | 0 | 3 | [`EllaPriest45/MinimaxH3_Characters`](https://huggingface.co/EllaPriest45/MinimaxH3_Characters) |  |  |
| 2026-08-06 | 0 | 14 | [`EllaPriest45/MinimaxH3_Styles`](https://huggingface.co/EllaPriest45/MinimaxH3_Styles) |  |  |
| 2026-09-15 | 0 | 0 | [`EllipsesMark/MiniMax-H3_comfy`](https://huggingface.co/EllipsesMark/MiniMax-H3_comfy) |  |  |
| 2026-08-18 | 0 | 0 | [`EllipsesMark/Sheet_Generator_H3_PoopMan333`](https://huggingface.co/EllipsesMark/Sheet_Generator_H3_PoopMan333) | image-to-image | comfyui, license:other |
| 2026-09-19 | 0 | 1 | [`EllipsesMark/minimaxh3_characters`](https://huggingface.co/EllipsesMark/minimaxh3_characters) |  | license:apache-2.0 |
| 2026-09-25 | 0 | 1 | [`Georgiy1108/Georgiy-Max-H3`](https://huggingface.co/Georgiy1108/Georgiy-Max-H3) |  |  |
| 2026-08-22 | 0 | 0 | [`GingerLabsPlatform/MiniMax-H3-D10000-T2V-Runtime`](https://huggingface.co/GingerLabsPlatform/MiniMax-H3-D10000-T2V-Runtime) |  |  |
| 2026-08-22 | 0 | 0 | [`GingerLabsPlatform/MiniMax-H3-Voice-Preprocessor-Runtime`](https://huggingface.co/GingerLabsPlatform/MiniMax-H3-Voice-Preprocessor-Runtime) |  |  |
| 2026-09-15 | 0 | 1 | [`Gonzaluigi/minimax-h3-refmods`](https://huggingface.co/Gonzaluigi/minimax-h3-refmods) |  |  |
| 2026-09-04 | 0 | 0 | [`Heouzen/minimax-h3_sks_noel`](https://huggingface.co/Heouzen/minimax-h3_sks_noel) |  |  |
| 2026-09-04 | 0 | 0 | [`Heouzen/minimax-h3_sks_rikel_r16`](https://huggingface.co/Heouzen/minimax-h3_sks_rikel_r16) |  |  |
| 2026-09-18 | 0 | 0 | [`Hoaschen06135/MINIMAXH3V3_Yz_tar`](https://huggingface.co/Hoaschen06135/MINIMAXH3V3_Yz_tar) |  |  |
| 2026-09-23 | 0 | 0 | [`Hoaschen06135/Minimaxh3HyLan`](https://huggingface.co/Hoaschen06135/Minimaxh3HyLan) |  |  |
| 2026-08-11 | 0 | 0 | [`Ivan12191812/MiniMax-H3`](https://huggingface.co/Ivan12191812/MiniMax-H3) |  |  |
| 2026-08-10 | 0 | 23 | [`JahJedi/MiniMax-H3-Character-Sheet`](https://huggingface.co/JahJedi/MiniMax-H3-Character-Sheet) |  | comfyui, license:apache-2.0 |
| 2026-09-22 | 0 | 1 | [`Jojocodex/ComfyUI-H3-WushuBridge`](https://huggingface.co/Jojocodex/ComfyUI-H3-WushuBridge) | other | comfyui, license:apache-2.0 |
| 2026-09-25 | 0 | 0 | [`Jojocodex/H3-Wushu-Fight-Simulator`](https://huggingface.co/Jojocodex/H3-Wushu-Fight-Simulator) | minimax-h3 |  |
| 2026-08-18 | 0 | 0 | [`K3NK/MiniMax_H3`](https://huggingface.co/K3NK/MiniMax_H3) |  | license:unknown |
| 2026-09-19 | 0 | 0 | [`KazumaSensei/MiniMax-H3`](https://huggingface.co/KazumaSensei/MiniMax-H3) |  |  |
| 2026-08-04 | 0 | 176 | [`Kijai/MiniMax-H3-TAE`](https://huggingface.co/Kijai/MiniMax-H3-TAE) |  | license:apache-2.0 |
| 2026-08-05 | 0 | 510 | [`Kijai/MiniMax-H3-experimental`](https://huggingface.co/Kijai/MiniMax-H3-experimental) |  |  |
| 2026-08-07 | 0 | 475 | [`Kijai/MiniMax-H3_comfy`](https://huggingface.co/Kijai/MiniMax-H3_comfy) |  |  |
| 2026-08-19 | 0 | 0 | [`LIQI5134/minimax-h3-t2v`](https://huggingface.co/LIQI5134/minimax-h3-t2v) |  |  |
| 2026-09-25 | 0 | 14 | [`LiseTY/Minimax-H3-ref2v_Anime_2_Realism`](https://huggingface.co/LiseTY/Minimax-H3-ref2v_Anime_2_Realism) |  | license:other |
| 2026-08-08 | 0 | 0 | [`Momoking/MiniMax-H3_comfy`](https://huggingface.co/Momoking/MiniMax-H3_comfy) |  |  |
| 2026-08-06 | 0 | 0 | [`NazGulation/comfyui_model_minimaxH3`](https://huggingface.co/NazGulation/comfyui_model_minimaxH3) |  |  |
| 2026-09-11 | 0 | 0 | [`Raretutor/Minimax-H3-Prompts-ComfyUI`](https://huggingface.co/Raretutor/Minimax-H3-Prompts-ComfyUI) |  | license:apache-2.0 |
| 2026-08-04 | 0 | 0 | [`Rudra-ai/MiniMax-H3`](https://huggingface.co/Rudra-ai/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-10 | 0 | 0 | [`Simplismart/Minimax-H3-FL2VA-Photon`](https://huggingface.co/Simplismart/Minimax-H3-FL2VA-Photon) |  |  |
| 2026-08-10 | 0 | 0 | [`Simplismart/Minimax-H3-Ref2VA-Photon`](https://huggingface.co/Simplismart/Minimax-H3-Ref2VA-Photon) |  |  |
| 2026-08-03 | 0 | 0 | [`TechnoBaptist/MiniMax-H3`](https://huggingface.co/TechnoBaptist/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-24 | 0 | 0 | [`Teddooo/MinimaxH3I2V`](https://huggingface.co/Teddooo/MinimaxH3I2V) |  |  |
| 2026-09-06 | 0 | 0 | [`Unicuser/minimaxh3`](https://huggingface.co/Unicuser/minimaxh3) |  | license:apache-2.0 |
| 2026-09-15 | 0 | 121 | [`UntMods/FaceSwap_MiniMaxH3_REF2VA`](https://huggingface.co/UntMods/FaceSwap_MiniMaxH3_REF2VA) |  | license:apache-2.0 |
| 2026-09-23 | 0 | 0 | [`Varlan97/minimaxh3`](https://huggingface.co/Varlan97/minimaxh3) |  | license:unknown |
| 2026-09-20 | 0 | 0 | [`WanApp/MinimaxH3`](https://huggingface.co/WanApp/MinimaxH3) |  | license:apache-2.0 |
| 2026-08-14 | 0 | 0 | [`YZisM3/MinimaxH3`](https://huggingface.co/YZisM3/MinimaxH3) |  |  |
| 2026-08-04 | 0 | 1 | [`acckpoot/MiniMax-H3`](https://huggingface.co/acckpoot/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-23 | 0 | 0 | [`adilkoray/minimax-h3-runpod-cache-lite`](https://huggingface.co/adilkoray/minimax-h3-runpod-cache-lite) |  | license:other |
| 2026-08-05 | 0 | 0 | [`alpaguyavuz/minimax-h3-l40s`](https://huggingface.co/alpaguyavuz/minimax-h3-l40s) |  |  |
| 2026-08-28 | 0 | 0 | [`altctrl/minimax-h3-sglang-vendor`](https://huggingface.co/altctrl/minimax-h3-sglang-vendor) |  | license:apache-2.0 |
| 2026-08-22 | 0 | 0 | [`amitat44/comic-minimax-h3-video`](https://huggingface.co/amitat44/comic-minimax-h3-video) |  |  |
| 2026-08-10 | 0 | 0 | [`anlessparky/minimax-h3-aoti`](https://huggingface.co/anlessparky/minimax-h3-aoti) |  | license:other |
| 2026-09-22 | 0 | 0 | [`boffee/MiniMax-H3-Piper`](https://huggingface.co/boffee/MiniMax-H3-Piper) |  |  |
| 2026-09-17 | 0 | 0 | [`bumasura/minimax-h3`](https://huggingface.co/bumasura/minimax-h3) |  |  |
| 2026-09-16 | 0 | 0 | [`carrot124/minimaxh3`](https://huggingface.co/carrot124/minimaxh3) |  |  |
| 2026-09-17 | 0 | 0 | [`carrot124/minimaxh3-i2v`](https://huggingface.co/carrot124/minimaxh3-i2v) |  |  |
| 2026-09-17 | 0 | 1 | [`carrot124/minimaxh3-r2v`](https://huggingface.co/carrot124/minimaxh3-r2v) |  |  |
| 2026-09-27 | 0 | 0 | [`cglearned/Minimax_H3_Face_Cut`](https://huggingface.co/cglearned/Minimax_H3_Face_Cut) |  |  |
| 2026-09-27 | 0 | 0 | [`chengxi1014/minimax-h3-comfyui-slim`](https://huggingface.co/chengxi1014/minimax-h3-comfyui-slim) |  | license:other |
| 2026-09-08 | 0 | 0 | [`chfm/redcraft-minimax-h3`](https://huggingface.co/chfm/redcraft-minimax-h3) |  |  |
| 2026-08-22 | 0 | 0 | [`clayshoaf/minimax-h3-runpod`](https://huggingface.co/clayshoaf/minimax-h3-runpod) |  |  |
| 2026-08-03 | 0 | 0 | [`cusiman/MiniMax-H3`](https://huggingface.co/cusiman/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-19 | 0 | 0 | [`dani444444el/MiniMax-H3-ComfyUI-Slim`](https://huggingface.co/dani444444el/MiniMax-H3-ComfyUI-Slim) |  |  |
| 2026-08-15 | 0 | 0 | [`dci05049/h3-minimax`](https://huggingface.co/dci05049/h3-minimax) |  |  |
| 2026-08-05 | 0 | 0 | [`demlog/minimax-h3-ref2va-worker`](https://huggingface.co/demlog/minimax-h3-ref2va-worker) |  |  |
| 2026-08-08 | 0 | 0 | [`djessica/minimax-h3-aoti`](https://huggingface.co/djessica/minimax-h3-aoti) |  | license:other |
| 2026-09-11 | 0 | 2 | [`drawthingsai/MiniMax-H3`](https://huggingface.co/drawthingsai/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-11 | 0 | 2 | [`drowzeys/keys-2k-MiniMax-H3-Parallel-Two-DGX-Sparks`](https://huggingface.co/drowzeys/keys-2k-MiniMax-H3-Parallel-Two-DGX-Sparks) | text-to-video | comfyui, license:other |
| 2026-08-24 | 0 | 48 | [`ethanfel/H3_Cinematic_Multishot_Coverage`](https://huggingface.co/ethanfel/H3_Cinematic_Multishot_Coverage) | image-to-video | comfyui, license:other |
| 2026-08-20 | 0 | 0 | [`f5aiteam/Minimax-H3`](https://huggingface.co/f5aiteam/Minimax-H3) |  |  |
| 2026-08-07 | 0 | 0 | [`fei567/open-video`](https://huggingface.co/fei567/open-video) | text-to-video | comfyui, license:apache-2.0 |
| 2026-08-03 | 0 | 2 | [`h35656566/MiniMax-H3`](https://huggingface.co/h35656566/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-20 | 0 | 1 | [`hainan88/minimax-h3-demo`](https://huggingface.co/hainan88/minimax-h3-demo) |  |  |
| 2026-09-07 | 0 | 1 | [`honeysandhu/MinimaxH3`](https://huggingface.co/honeysandhu/MinimaxH3) |  |  |
| 2026-08-09 | 0 | 0 | [`huggsaa/m4`](https://huggingface.co/huggsaa/m4) | text-to-video | license:apache-2.0 |
| 2026-08-14 | 0 | 0 | [`illusion-of-life/style-max-minimax-h3-fl2va`](https://huggingface.co/illusion-of-life/style-max-minimax-h3-fl2va) |  | license:other |
| 2026-08-17 | 0 | 2 | [`jasperz111/redcraft-minimax-h3`](https://huggingface.co/jasperz111/redcraft-minimax-h3) |  |  |
| 2026-08-08 | 0 | 3 | [`jayseanbrambila/MiniMax-H3-AI-Video-Generator`](https://huggingface.co/jayseanbrambila/MiniMax-H3-AI-Video-Generator) | image-to-video | comfyui, license:mit |
| 2026-08-29 | 0 | 0 | [`jayseanbrambila/minimax-h3-video`](https://huggingface.co/jayseanbrambila/minimax-h3-video) | image-to-video | license:mit |
| 2026-08-19 | 0 | 0 | [`jekverse/minimax-h3-aoti`](https://huggingface.co/jekverse/minimax-h3-aoti) |  |  |
| 2026-09-04 | 0 | 0 | [`jinksa77/Minimax_H3`](https://huggingface.co/jinksa77/Minimax_H3) |  |  |
| 2026-08-14 | 0 | 0 | [`joeranger789/MinimaXH3All`](https://huggingface.co/joeranger789/MinimaXH3All) |  |  |
| 2026-08-13 | 0 | 2 | [`joeygambino/Dual-Engine-H3-LTX25`](https://huggingface.co/joeygambino/Dual-Engine-H3-LTX25) | text-to-video | comfyui, license:mit |
| 2026-08-24 | 0 | 0 | [`joeygambino/MiniMax-H3-ZSpatial-native`](https://huggingface.co/joeygambino/MiniMax-H3-ZSpatial-native) |  |  |
| 2026-09-03 | 0 | 12 | [`junchaoh-cs/SolarWM-H3-33B`](https://huggingface.co/junchaoh-cs/SolarWM-H3-33B) | pytorch |  |
| 2026-08-19 | 0 | 0 | [`kaiw7/Kai-JAV-MiniMax-H3`](https://huggingface.co/kaiw7/Kai-JAV-MiniMax-H3) | diffusers |  |
| 2026-09-09 | 0 | 0 | [`keyoung/MiniMaxH3_SMPL`](https://huggingface.co/keyoung/MiniMaxH3_SMPL) | diffusers |  |
| 2026-08-03 | 0 | 0 | [`khaduyen1993/minimax-h3`](https://huggingface.co/khaduyen1993/minimax-h3) |  |  |
| 2026-09-24 | 0 | 1 | [`kogehek/DaSiWa_MiniMax_H3`](https://huggingface.co/kogehek/DaSiWa_MiniMax_H3) |  | license:other |
| 2026-09-05 | 0 | 49 | [`malcolmrey/minimaxh3`](https://huggingface.co/malcolmrey/minimaxh3) |  | license:apache-2.0 |
| 2026-08-11 | 0 | 2 | [`mhnakif/minimax_h3`](https://huggingface.co/mhnakif/minimax_h3) |  |  |
| 2026-08-05 | 0 | 0 | [`mid2/MiniMax-H3-mirrors`](https://huggingface.co/mid2/MiniMax-H3-mirrors) |  |  |
| 2026-08-15 | 0 | 0 | [`minguri98/minimaxh3`](https://huggingface.co/minguri98/minimaxh3) |  |  |
| 2026-08-20 | 0 | 0 | [`mrdarkbr/minimax-h3-models-backup`](https://huggingface.co/mrdarkbr/minimax-h3-models-backup) |  |  |
| 2026-08-03 | 0 | 0 | [`nDman/MiniMax-H3`](https://huggingface.co/nDman/MiniMax-H3) |  | comfyui, license:other |
| 2026-08-19 | 0 | 0 | [`nemusugikenshin/MiniMax-H3Test`](https://huggingface.co/nemusugikenshin/MiniMax-H3Test) |  |  |
| 2026-08-12 | 0 | 0 | [`nikdevs/minimax-h3-fl2va`](https://huggingface.co/nikdevs/minimax-h3-fl2va) |  |  |
| 2026-08-12 | 0 | 0 | [`nikdevs/minimax-h3-ref2va`](https://huggingface.co/nikdevs/minimax-h3-ref2va) |  |  |
| 2026-08-31 | 0 | 11 | [`orangesouth/MinimaxH3CinematicRealism`](https://huggingface.co/orangesouth/MinimaxH3CinematicRealism) |  |  |
| 2026-08-09 | 0 | 0 | [`phaus00/MODELH3`](https://huggingface.co/phaus00/MODELH3) | text-to-video | license:apache-2.0 |
| 2026-09-13 | 0 | 1 | [`pridewar/ACT-Minimax-H3`](https://huggingface.co/pridewar/ACT-Minimax-H3) |  | license:apache-2.0 |
| 2026-09-20 | 0 | 1 | [`pridewar/BHM-Minimax-H3`](https://huggingface.co/pridewar/BHM-Minimax-H3) |  | license:apache-2.0 |
| 2026-09-13 | 0 | 1 | [`pridewar/BM-Minimax-H3`](https://huggingface.co/pridewar/BM-Minimax-H3) |  | license:apache-2.0 |
| 2026-09-12 | 0 | 1 | [`pridewar/NAFASP-Minimax-H3`](https://huggingface.co/pridewar/NAFASP-Minimax-H3) |  | license:apache-2.0 |
| 2026-09-23 | 0 | 0 | [`rdvl89/cumshot-minimaxh3`](https://huggingface.co/rdvl89/cumshot-minimaxh3) |  | license:apache-2.0 |
| 2026-08-20 | 0 | 4 | [`saejon/MinimaxH3`](https://huggingface.co/saejon/MinimaxH3) |  | license:apache-2.0 |
| 2026-08-25 | 0 | 0 | [`saejon/minimaxh32`](https://huggingface.co/saejon/minimaxh32) |  | license:apache-2.0 |
| 2026-08-03 | 0 | 0 | [`sekkit/MiniMax-H3`](https://huggingface.co/sekkit/MiniMax-H3) | image-text-to-video | license:other |
| 2026-08-07 | 0 | 86 | [`silveroxides/MiniMax-H3_tests`](https://huggingface.co/silveroxides/MiniMax-H3_tests) |  |  |
| 2026-09-08 | 0 | 1 | [`sinatra-rd/real-dream-minimax-h3`](https://huggingface.co/sinatra-rd/real-dream-minimax-h3) |  |  |
| 2026-09-08 | 0 | 1 | [`smart-bobo/MiniMax-H3`](https://huggingface.co/smart-bobo/MiniMax-H3) |  | license:cc-by-4.0 |
| 2026-09-17 | 0 | 0 | [`smith1302/Minimaxh3`](https://huggingface.co/smith1302/Minimaxh3) |  |  |
| 2026-09-07 | 0 | 0 | [`songyu123/minimax_h3_worship_it_v_0.6`](https://huggingface.co/songyu123/minimax_h3_worship_it_v_0.6) |  | license:mit |
| 2026-08-14 | 0 | 0 | [`strangevil/MiniMax-H3`](https://huggingface.co/strangevil/MiniMax-H3) | image-text-to-video | license:other |
| 2026-09-10 | 0 | 1 | [`tubbymeatball/MinimaxH3-CumWalk`](https://huggingface.co/tubbymeatball/MinimaxH3-CumWalk) |  |  |
| 2026-08-12 | 0 | 0 | [`wangpj/MiniMax-H3-FL2VA`](https://huggingface.co/wangpj/MiniMax-H3-FL2VA) |  | license:other |
| 2026-08-12 | 0 | 0 | [`wangpj/MiniMax-H3-Ref2VA`](https://huggingface.co/wangpj/MiniMax-H3-Ref2VA) |  | license:other |
| 2026-08-13 | 0 | 0 | [`wiikoo/minimax-h3`](https://huggingface.co/wiikoo/minimax-h3) |  |  |
| 2026-09-17 | 0 | 0 | [`xxx1311/minimax-h3`](https://huggingface.co/xxx1311/minimax-h3) |  |  |
| 2026-09-17 | 0 | 2 | [`yang1975/MinimaxH3_Actions`](https://huggingface.co/yang1975/MinimaxH3_Actions) |  |  |
| 2026-08-24 | 0 | 38 | [`zuanfilm/H3_HD_2K_Detailer`](https://huggingface.co/zuanfilm/H3_HD_2K_Detailer) | text-to-video | comfyui, license:mit |

## 说明

- **15-镜像转载与其它**：多为同名镜像、个人备份、或尚未细分类的仓；使用前请核对 `base_model` 与文件哈希。
- **12-题材角色 LoRA**：含 NSFW / 名人向适配器，仅作索引，不代表推荐。
- 新增仓的分类由仓名/标签关键词自动归类（上一版已收录仓沿用原分类），个别仓可能归类偏差，以卡页为准。
- 快照文件：`hf_last3m.json`（同日 API 导出，按本页分类与下载量排序）。
