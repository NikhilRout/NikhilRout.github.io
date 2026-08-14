---
title: "RoadBlock: Rethinking Tensor Core Microarchitecture for Emerging Microscaling Format Support on GPUs"
collection: publications
category: workshops
permalink: /publication/2026-06-28-roadblock_oscar26/
excerpt: #
date: 2026-06-28
venue: "Open-Source Computer Architecture Research (OSCAR) Workshop @ ISCA 2026"
paperurl: 'https://nikhilrout.github.io/files/roadblock_oscar26.pdf'
slidesurl: #
---

{% if page.paperurl %}[**Paper**]({{ page.paperurl }}){% endif %} {% if page.slidesurl %}[**Slides**]({{ page.slidesurl }}){% endif %}

## Abstract

Emerging microscaling (MX) formats are pushing the quantization–perplexity pareto frontier beyond industry-adopted OCP MX formats, but their hardware evaluations are often limited to MAC-unit prototypes intended for systolic-array accelerators. Meanwhile, most practical block-quantized training and inference stacks are being developed around GPU Tensor Cores. To bridge this gap, we propose RoadBlock, an open-source framework for accurate end-to-end modeling and evaluation of custom MX formats and unconventional quantization schemes in Tensor Core Units, built on the RISC-V extended Vortex GPGPU platform. RoadBlock exposes data, scale-factor and block size as configurable parameters, automatically derives tile dimensions and metadata indexing for arbitrary formats, and introduces a lightweight metadata-register TCU-SRAM duplication methodology for delivering scale-factor metadata directly to the TCU fused dot-product grid. RoadBlock also extends the Vortex WMMA ABI with MX metadata pointers and optionally supports tensor-wise scaling in the WMMA epilogue. Preliminary cycle-approximate simulator evaluation shows that while MXFP8 achieves 76–98% of its ideal 2x throughput gain over FP16/BF16, NVFP4 only recovers 70–76% of its advantage over FP8/BF8 due to tensor-wise dequantization overhead. Future work includes RTL prototyping of emerging formats for timing, power, and area characterization, warp-specialized kernels for multi-level scaling formats, and revisiting the TCU-SRAM for larger WGMMA Tensor Core tile sizes. Source code available at https://github.com/vortexgpgpu/vortex/tree/oscar-roadblock
