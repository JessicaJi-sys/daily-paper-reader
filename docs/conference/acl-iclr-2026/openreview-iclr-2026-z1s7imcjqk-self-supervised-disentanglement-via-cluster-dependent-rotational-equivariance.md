---
title: Self-Supervised Disentanglement via Cluster-Dependent Rotational Equivariance
title_zh: 基于簇依赖旋转等变性的自监督解耦
authors: "Junbing Liu, Zhiming Zhou"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=Z1S7ImcjQK"
tags: ["query:ood-inv"]
score: 6.0
evidence: 通过簇依赖旋转等变性实现自监督特征空间解耦
tldr: 该文关注自监督学习中特征空间的结构控制问题，指出单纯强制增强不变性虽能得到聚类表示，却难以实现良好解耦。作者提出簇依赖旋转等变性方法，用等变预测刻画特征变换，并消除最终目标中不变性与等变性的冲突。方法避免语义簇被强制平行排列，改善了表示的解耦质量，为无监督特征解耦提供新视角。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 自监督学习强制增强不变性虽得聚类表示，但对特征空间结构控制有限、阻碍解耦。
method: 提出簇依赖旋转等变性方法，用等变预测刻画特征变换并消除不变性冲突。
result: 方法避免语义簇平行排列，改善表示解耦质量。
conclusion: 簇依赖等变性为自监督特征解耦提供有效机制。
---

## Abstract
Conventional self-supervised learning methods extract robust features by enforcing invariance to data augmentations. While effective for obtaining clustered representations, this objective provides limited control over how data variations structure the feature space, hindering disentanglement. Recent methods improve feature space structure by imposing equivariant predictability on feature transformations induced by data augmentations. However, existing approaches suffer from two significant limitations: (i) the incorporation of invariance in their final objective interferes with the learning of neat equivariance; (ii) the imposition of uniform equivariance across all samples forces semantic clusters into a parallel arrangement, leading to reduced inter-cluster distances (for features on the hypersphere). To overcome these issues, we propose in this paper Cluster-Dependent Rotational Equivariance for Disentanglement (CD-RED), a framework that enables learning neat equivariance and uniformly distributed clusters, while further supporting perfect disentanglement. Notably, CD-RED explicitly encodes variations as rotations via a direct product of $SO(2)$ groups within orthogonal hyperspherical subspaces, providing a principled mechanism for precise equivariance. We theoretically and experimentally establish that CD-RED achieves perfectly disentangled representations, suggesting a promising new direction for self-supervised disentanglement.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过簇依赖旋转等变性实现自监督特征空间解耦。

### 2. 核心内容
该文关注自监督学习中特征空间的结构控制问题，指出单纯强制增强不变性虽能得到聚类表示，却难以实现良好解耦。作者提出簇依赖旋转等变性方法，用等变预测刻画特征变换，并消除最终目标中不变性与等变性的冲突。方法避免语义簇被强制平行排列，改善了表示的解耦质量，为无监督特征解耦提供新视角。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=Z1S7ImcjQK](https://openreview.net/forum?id=Z1S7ImcjQK)
