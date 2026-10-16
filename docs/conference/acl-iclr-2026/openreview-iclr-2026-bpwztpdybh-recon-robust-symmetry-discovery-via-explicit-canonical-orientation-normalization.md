---
title: "RECON: Robust symmetry discovery via Explicit Canonical Orientation Normalization"
title_zh: RECON：基于显式规范方向归一化的鲁棒对称性发现
authors: "Alonso Urbano, David W. Romero, Max Zimmer, Sebastian Pokutta"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=bpWzTPDybh"
tags: ["query:ood-inv"]
score: 7.0
evidence: 类-姿态分解将不变特征与姿态解耦并检测OOD姿态
tldr: 本文针对类-姿态分解中规范坐标系依赖训练、任意且不稳定的问题，提出RECON显式规范方向归一化方法。该方法通过右平移校正任意规范系，得到与数据对齐的自然规范化表示。由此可实现实例级姿态分布的无监督发现、分布外姿态检测以及即插即用的测试时规范化，为解耦不变特征与变化特征提供了有效机制。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 类-姿态分解依赖训练相关的任意规范系，导致不变特征与姿态解耦不稳定，影响泛化与OOD检测。
method: 提出RECON规范方向归一化，通过简单右平移校正任意规范系，获得与数据对齐的自然规范化表示。
result: 方法支持实例级姿态分布的无监督发现、OOD姿态检测及即插即用测试时规范化。
conclusion: 该工作为解耦不变特征与变化因素提供了无需固定对称群的有效机制，提升了鲁棒性。
---

## Abstract
Real world data often exhibits unknown, instance-specific symmetries that rarely exactly match a transformation group $G$ fixed a priori. Class-pose decompositions aim to create disentangled representations by factoring inputs into invariant features and a pose $g\in G$ defined relative to a training-dependent, \emph{arbitrary} canonical representation. We introduce RECON, a class-pose agnostic \emph{canonical orientation normalization} that corrects arbitrary canonicals via a simple right translation, yielding \emph{natural}, data-aligned canonicalizations. This enables (i) unsupervised discovery of instance-specific pose distributions, (ii) detection of out-of-distribution poses and (iii) a plug-and-play \emph{test-time canonicalization layer}. This layer can be attached on top of any pre-trained model to infuse group invariance, improving its performance without retraining.  We validate on 2D (images) and 3D (molecular ensembles), demonstrating fine-grained, accurate pose discovery, and matching or outperforming label-supervised
canonicalizations in downstream classification.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
类-姿态分解将不变特征与姿态解耦并检测OOD姿态。

### 2. 核心内容
本文针对类-姿态分解中规范坐标系依赖训练、任意且不稳定的问题，提出RECON显式规范方向归一化方法。该方法通过右平移校正任意规范系，得到与数据对齐的自然规范化表示。由此可实现实例级姿态分布的无监督发现、分布外姿态检测以及即插即用的测试时规范化，为解耦不变特征与变化特征提供了有效机制。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=bpWzTPDybh](https://openreview.net/forum?id=bpWzTPDybh)
