---
title: "FoldSim: Scaling Cycle-Exact RTL Simulation with Hierarchical Folding and Static Scheduling"
collection: publications
category: conferences
permalink: /publication/2026-foldsim/
excerpt: #''
date: 2026-11-19
venue: 'Preprint, Under review.'
paperurl: 'https://arxiv.org/abs/2611.26472'
---

{% if page.paperurl %}[**Paper**]({{ page.paperurl }}){% endif %} {% if page.slidesurl %}[**Slides**]({{ page.slidesurl }}){% endif %}

## Abstract

RTL simulation is essential for hardware design and verification, yet its execution time grows rapidly with design scale and complexity. CPU- and GPU-based simulators exploit parallelism to accelerate RTL evaluation, but achieving high simulation throughput for large designs remains challenging. FPGA-based simulators offer higher throughput by mapping RTL computations directly onto hardware, but their scalability is constrained by FPGA resource capacity. We present FoldSim, an automated framework that enables cycle-exact simulation of large RTL designs on a single FPGA through hierarchical folding. FoldSim maps instances across the design hierarchy onto shared logic while maintaining their independent state. Given foldable module classes, its compiler constructs a static schedule that coordinates their execution, reducing dynamic synchronization overhead and making state accesses predictable. FoldSim backs state that exceeds on-chip capacity with external memory and brings it to the shared circuits as needed. A configurable DRAM model separates target-memory timing from host delays. The compiler explores replica allocations and state placement to balance resource savings against simulation time. On one AMD Alveo V80, FoldSim runs an 8-SM GPU and a 1,024-node Rocket datacenter with 4,096 processor cores. The unfolded implementations require approximately 16x and 200x as many LUTs as FoldSim's, respectively. The datacenter keeps about 1.9 GB of state in HBM, while a 4-SM GPU completes a 1024x1024 GEMM in 4.24 seconds, versus 26 hours in software RTL simulation.

{% raw %}
```bibtex
@misc{wang2026foldsim,
      title={FoldSim: Scaling Cycle-Exact RTL Simulation with Hierarchical Folding and Static Scheduling},
      author={Chengxuan Wang and Nikhil Rout and Yang-gon Kim and Jacob Leigh and Yufan Du and Blaise Tine},
      year={2026},
      eprint={2611.26472},
      archivePrefix={arXiv},
      primaryClass={cs.AR},
      url={https://arxiv.org/abs/2611.26472},
}
```
{% endraw %}
