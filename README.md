# VolMusCo: Learning Full-Body Motion Control with Volumetric Muscles

<p align="center">
  <a href="https://inckieultra.github.io/VolMusCo-Project-Page/"><strong>🌐 Project Page</strong></a> ·
  <a href="https://inckieultra.github.io/VolMusCo-Project-Page/paper/VolMusCo_arxiv.pdf"><strong>📄 Paper (PDF)</strong></a> ·
  <a href="https://inckieultra.github.io/VolMusCo-Project-Page/#video"><strong>🎬 Full Video (1080p)</strong></a> ·
  <a href="https://inckieultra.github.io/VolMusCo-Project-Page/#interactive-viewer"><strong>🔬 Interactive Mesh vs. Surface Viewer</strong></a>
</p>

<p align="center">
  <strong>Wangyingqi Ding<sup>1*</sup></strong> &emsp;
  <strong>Yusen Feng<sup>2*</sup></strong> &emsp;
  <strong>Kaibo He<sup>3</sup></strong> &emsp;
  <strong>Bingchen Han<sup>2</sup></strong> &emsp;
  <strong>Libin Liu<sup>2</sup></strong>
  <br>
  <sup>1</sup>Tsinghua University &emsp; <sup>2</sup>Peking University &emsp; <sup>3</sup>Clone Incorporated
  <br>
  <em><sup>*</sup>Equal contribution</em>
</p>

---

<p align="center">
  <img src="https://inckieultra.github.io/VolMusCo-Project-Page/assets/figures/pipeline_unified.png" alt="VolMusCo System Pipeline" width="96%">
</p>

## Overview

**VolMusCo** is a simulation and model-based reinforcement learning framework for full-body motion control driven by **284 two-way coupled volumetric muscles** (2,556 tetrahedra).

- **Two-Way Volumetric Muscle–Skeleton Coupling:** Muscle excitations drive 100 Hz quasi-static Projective Dynamics (PD) solves over deformable tetrahedral muscle bellies with bone-fixed tendon routing and cylinder wrapping, transmitting generalized reaction forces to a 1 kHz skeletal simulator (MJWarp) while skeletal motion continuously updates attachment and contact geometry.
- **Scalable GPU Throughput:** Our simplified 9-tetrahedron muscle representation matches fine 230-tet volumetric meshes within **1.87°** full-body joint RMSE while running at **815 environment steps/s** across 2,048 parallel worlds on a single RTX 4090.
- **World-Model Reinforcement Learning:** Learning a differentiable world model from physical replay transitions enables whole-body tracking on LaFAN1 with a **97.9%** success rate and **5.52 cm** mean local-body position error within **10 hours** of single-GPU training, and supports diverse skills including tennis ball returns, three-ball cascade juggling, 80 kg barbell deadlifts, sword-and-shield combat, and monocular video tracking.

---

## Code & Asset Release Plan

> **🚧 Code release is currently being prepared.** Star / watch this repository for updates!

- [x] Preprint paper & supplementary details ([PDF](https://inckieultra.github.io/VolMusCo-Project-Page/paper/VolMusCo_arxiv.pdf))
- [x] Interactive project page & full-body video gallery ([Website](https://inckieultra.github.io/VolMusCo-Project-Page/))
- [ ] Full-body 284-muscle 9-tet anatomical model & calibration scripts
- [ ] Batched GPU Projective Dynamics + MJWarp two-way coupled simulation environment
- [ ] Differentiable world-model RL training, evaluation & visualization code
- [ ] Pretrained motion-tracking & prop-interaction checkpoints

---

## Citation

```bibtex
@article{ding2026volmusco,
  title   = {VolMusCo: Learning Full-Body Motion Control with Volumetric Muscles},
  author  = {Ding, Wangyingqi and Feng, Yusen and He, Kaibo and Han, Bingchen and Liu, Libin},
  journal = {arXiv preprint},
  year    = {2026}
}
```
