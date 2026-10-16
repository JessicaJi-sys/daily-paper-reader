---
title: Soft Equivariance Regularization for Invariant Self-Supervised Learning
title_zh: 面向不变自监督学习的软等变正则化
authors: "Joohyung Lee, Changhun Kim, Hyunsu Kim, Kwanhyung Lee, Juho Lee"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=TuQW7VPfXF"
tags: ["query:ood-inv"]
score: 4.0
evidence: 表示学习中不变性与等变性的权衡
tldr: 针对自监督学习中强制不变性会抑制对几何扰动有用结构的问题，本文分析不变性与等变性联合优化的权衡现象，发现将等变正则推向深层虽提升等变分数却损害识别性能，进而提出软等变正则化方法。实验表明该策略能在保持识别精度的同时改善对几何变换的鲁棒性，为不变表示学习中的退化与权衡问题提供了新的正则化视角。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 自监督学习强制不变性会抑制对几何扰动有用的变换相关结构，导致鲁棒性与识别性能失衡。
method: 本文分析不变性与等变性联合优化的权衡，提出在合适层级施加软等变正则化以缓解耦合退化。
result: 实验显示等变正则推向深层虽提高等变分数却降低ImageNet线性评估精度，软正则可缓解该权衡。
conclusion: 研究揭示了不变表示学习中的内在权衡，为稳健表示学习提供可迁移的正则化思路。
---

## Abstract
Self-supervised learning (SSL) typically learns representations invariant to semantic-preserving augmentations (e.g., random crops and photometric jitter). While effective for recognition, enforcing strong invariance can suppress transformation-dependent structure that is useful for robustness to geometric perturbations and spatially sensitive transfer. A growing body of work, therefore, augments invariance-based SSL with equivariance objectives, but these objectives are often imposed on the same **final** (typically spatially-collapsed) representation. We empirically observe a trade-off in this coupled setting: pushing equivariance regularization toward deeper layers improves equivariance scores but degrades ImageNet-1k linear evaluation, motivating a layer-decoupled design. Motivated by this trade-off, we propose **Soft Equivariance Regularization (SER)**, a plug-in regularizer that decouples where invariance and equivariance are enforced: we keep the base SSL objective unchanged on the final embedding, while softly encouraging equivariance on an \emph{intermediate spatial token map} via analytically specified group actions $\rho_g$ (e.g., $90^{\circ}$ rotations, flips, and scaling) applied directly in feature space. SER learns/predicts no per-sample transformation codes/labels, requires no auxiliary transformation-prediction head, and adds only **1.008$\times$** training FLOPs. On ImageNet-1k ViT-S/16 pretraining, SER improves MoCo-v3 by **+0.84** Top-1 in linear evaluation under a strictly matched 2-view setting and consistently improves DINO and Barlow Twins; under matched view counts, SER achieves the best ImageNet-1k linear-eval Top-1 among the compared invariance+equivariance add-ons. SER further improves ImageNet-C/P by **+1.11/+1.22** Top-1 and frozen-backbone COCO detection by **+1.7** mAP. Finally, applying the same **layer-decoupling** recipe to existing invariance+equivariance baselines (e.g., EquiMod and AugSelf) improves their accuracy, suggesting layer decoupling as a general design principle for combining invariance and equivariance. Code is available at https://github.com/aitrics-chris/SER.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
表示学习中不变性与等变性的权衡。

### 2. 核心内容
针对自监督学习中强制不变性会抑制对几何扰动有用结构的问题，本文分析不变性与等变性联合优化的权衡现象，发现将等变正则推向深层虽提升等变分数却损害识别性能，进而提出软等变正则化方法。实验表明该策略能在保持识别精度的同时改善对几何变换的鲁棒性，为不变表示学习中的退化与权衡问题提供了新的正则化视角。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=TuQW7VPfXF](https://openreview.net/forum?id=TuQW7VPfXF)
