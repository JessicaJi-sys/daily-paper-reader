---
title: Let OOD Feature Exploring Vast Predefined Classifiers
title_zh: 让OOD特征探索大量预定义分类器
authors: "Kewen Xia, Xiaodong Yue, WeiZhipeng, Yaxin Peng, Zihao Li, Jianxiang Zhu, Jie Shi, PeilinXu"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=DtkIH5TKe6"
tags: ["query:ood-inv"]
score: 5.0
evidence: 通过预定义分类器控制OOD表示几何
tldr: 本文针对现有OOD检测方法仅强制ID与OE特征正交、忽视表示几何可控性的问题，提出Vast Predefined Classifiers方法。该方法构建预定义的正交等角特征空间，显式分离分布内与分布外表示。研究提升了OOD检测中表示几何的可控性与泛化能力，对鲁棒表示学习有参考价值，但主要面向检测而非不变特征解耦。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有基于离群暴露的OOD方法只强制特征正交，忽视了表示几何的可控性，限制检测鲁棒性。
method: 提出预定义分类器VPC，构建正交等角特征空间，显式分离分布内与分布外表示。
result: 方法在OOD检测中提升了对表示几何的控制能力与检测泛化性能。
conclusion: 该工作为通过表示几何设计增强OOD鲁棒性提供了新思路，但侧重检测任务。
---

## Abstract
Real-world out-of-distribution (OOD) data exhibit broad, continually evolving distributions, rendering reliance solely on in-distribution (ID) data insufficient for robust detection. Consequently, methods leveraging auxiliary Outlier Exposure (OE) data have emerged, substantially enhancing generalization by jointly fine-tuning models on ID and large-scale OE data. However, many existing approaches primarily enforce orthogonality between ID and OE features while pushing OE predictions toward near-uniform, low-confidence scores, thus overlooking the controllability of representation geometry. We propose Vast Predefined Classifiers (VPC), which constructs a pre-specified Orthogonal Equiangular Feature Space (OEFS) to explicitly separate ID and OOD representations while capturing the rich variability of OOD features. We employ evidential priors to align ID features with their class-specific Equiangular Basic Vectors (EBVs), thereby preserving ID performance. In parallel, a new VEBV loss encourages OE features to explore the subspace spanned by Vast EBVs (VEBVs), enabling a rich characterization of diverse OOD patterns. This dual optimization, coupled with the prescribed geometric representation space, promotes optimal orthogonality between ID and OOD representations. Furthermore, we introduce the VPC Score, a discriminative metric based on the L2 activation intensity of features over the predefined classifiers. Extensive experiments across diverse OOD settings and training paradigms on benchmarks including CIFAR-10/100 and the ImageNet-1k, demonstrate strong and robust performance, validating VPC's effectiveness. Code is available at https://github.com/eightnight2049/VPC.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过预定义分类器控制OOD表示几何。

### 2. 核心内容
本文针对现有OOD检测方法仅强制ID与OE特征正交、忽视表示几何可控性的问题，提出Vast Predefined Classifiers方法。该方法构建预定义的正交等角特征空间，显式分离分布内与分布外表示。研究提升了OOD检测中表示几何的可控性与泛化能力，对鲁棒表示学习有参考价值，但主要面向检测而非不变特征解耦。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=DtkIH5TKe6](https://openreview.net/forum?id=DtkIH5TKe6)
