---
title: "SIMTurn: Lightweight Divergent Subgroup Scheduling for Intra-Warp Synchronization"
collection: publications
category: conferences
permalink: /publication/2026-simturn/
excerpt: #''
date: 2026-11-13
venue: 'Preprint, Under review.'
paperurl: 'https://arxiv.org/abs/2611.17827'
---

{% if page.paperurl %}[**Paper**]({{ page.paperurl }}){% endif %} {% if page.slidesurl %}[**Slides**]({{ page.slidesurl }}){% endif %}

## Abstract

Stack-based reconvergence enables efficient SIMT execution with a shared warp program counter and compact control-flow state. However, its fixed serialization of divergent paths can deadlock programs that rely on intra-warp synchronization: a spinning subgroup may prevent a resource-holding sibling from executing. Independent Thread Scheduling (ITS) enables finer-grained progress through per-thread execution state, but introduces additional hardware cost. We present SIMTurn, a lightweight compiler-hardware mechanism that enables forward progress among divergent subgroups while retaining stack-based reconvergence. SIMTurn combines a compiler-inserted yield instruction at potentially blocking loops with a bounded pool of resumable subgroups. The scheduler allows a waiting subgroup to yield to a sibling that can make progress, without requiring independent program counters for every thread. We implement SIMTurn in the compiler, simulator, and RTL on the open-source Vortex GPGPU and evaluate it against baseline IPDOM and per-thread ITS schemes. Across the evaluated GPU thread configurations, SIMTurn introduces only 17-24% scheduler-area overhead relative to IPDOM, compared with 39-91% for ITS, and stays within 8% of IPDOM on workloads that never need cross-subgroup progress. On kernels with genuine cross-subgroup parallelism, SIMTurn tracks ITS closely and is up to 2.7x faster than a software-serialized IPDOM baseline.

{% raw %}
```bibtex
@misc{rout2026simturn,
      title={SIMTurn: Lightweight Divergent Subgroup Scheduling for Intra-Warp Synchronization},
      author={Nikhil Rout and Joe Samuel Rosh and Blaise Tine},
      year={2026},
      eprint={2611.17827},
      archivePrefix={arXiv},
      primaryClass={cs.AR},
      url={https://arxiv.org/abs/2611.17827},
}
```
{% endraw %}
