---
title: Transductive Learning for Out-of-Distribution Molecular Property Prediction
title_zh: 面向分布外分子性质预测的转导学习
authors: "Kiwoong Yoo, Hajung Kim, Soyon Park, Junseok Choe, Sunkyu Kim, Jaewoo Kang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=rmvO5WRb58"
tags: ["query:ood-inv"]
score: 7.0
evidence: 潜空间中的分布外分子性质预测
tldr: 针对分子性质预测在训练分布之外难以泛化、标准模型对新化学结构外推失败的问题，本文提出多锚点潜空间转导框架MALT，直接在已学习的潜空间中利用任意预训练分子编码器的嵌入，为查询分子选取多个相似类比进行推理。该方法突破了以往固定描述符与单锚点比较的限制。实验表明其在分布外分子性质预测任务上优于基线，为药物发现中的OOD泛化与潜表示层面的方法设计提供了重要参考。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 药物发现中分布外分子性质预测至关重要，但标准模型难以对新颖化学结构外推泛化。
method: 提出多锚点潜空间转导框架MALT，在学习到的潜空间中选取多个相似分子进行类比推理。
result: 实验显示MALT在分布外分子性质预测上优于固定描述符与单锚点的既有方法。
conclusion: 验证了直接在潜表示空间做转导推理对OOD泛化的有效性，可迁移到药物相关任务。
---

## Abstract
Predicting molecular properties outside the training data distribution (Out-of-Distribution, OOD) is critical for accelerating drug discovery. This task requires models to extrapolate beyond known property ranges and generalize to novel chemical structures—a common failure point for standard machine learning models. While transductive analogical reasoning shows promise, prior methods are often constrained by fixed descriptors and single-anchor comparisons. To overcome these limitations, we introduce Multi-Anchor Latent Transduction (MALT) framework, which operates directly within a learned latent space. MALT can leverage embeddings from any powerful, pre-trained molecular encoder to select multiple relevant analogues of query molecule. It then integrates the query and anchor embeddings to generate a final prediction. On rigorous OOD benchmarks targeting shifts in both property values and chemical features, MALT consistently improves generalization over standard inductive baselines. Notably, our framework also matches or surpasses the in-distribution performance of these base models. These findings establish multi-anchor transduction in latent space as an effective strategy to augment existing molecular encoders, enabling robust and extrapolative predictions needed to solve challenging discovery tasks.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
潜空间中的分布外分子性质预测。

### 2. 核心内容
针对分子性质预测在训练分布之外难以泛化、标准模型对新化学结构外推失败的问题，本文提出多锚点潜空间转导框架MALT，直接在已学习的潜空间中利用任意预训练分子编码器的嵌入，为查询分子选取多个相似类比进行推理。该方法突破了以往固定描述符与单锚点比较的限制。实验表明其在分布外分子性质预测任务上优于基线，为药物发现中的OOD泛化与潜表示层面的方法设计提供了重要参考。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=rmvO5WRb58](https://openreview.net/forum?id=rmvO5WRb58)
