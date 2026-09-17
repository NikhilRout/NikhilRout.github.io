---
title: "RoadBlock: Rethinking GPU Tensor Core Microarchitecture for Emerging Microscaling Format Support"
collection: publications
category: conferences
permalink: /publication/2026-roadblock/
excerpt: #
date: 2026-09-17
venue: "ACM Parallel Architectures and Compilation Techniques (PACT), 2026"
paperurl: 'https://nikhilrout.github.io/files/pact26-59.pdf'
slidesurl: #
---

{% if page.paperurl %}[**Paper**]({{ page.paperurl }}){% endif %} {% if page.slidesurl %}[**Slides**]({{ page.slidesurl }}){% endif %}

## Abstract

While multiple recent custom Microscaling (MX) format proposals preserve higher model quality over OCP MX, their hardware evaluations remain confined to standalone MAC-unit prototypes, ignoring the system-level integration overheads inside real GPU Tensor Cores. To this end, I present RoadBlock, an open-source framework for accurate end-to-end modeling of custom MX formats in a programmable Tensor Core, built on the RISC-V Vortex GPGPU. RoadBlock exposes data size, scale-factor size, and block size as configurable parameters and automatically derives per-thread metadata tiling for arbitrary formats, enabling format-specific Perplexity-PPA tradeoff evaluation before silicon commitment.

Source code available at https://github.com/vortexgpgpu/vortex/tree/roadblock
