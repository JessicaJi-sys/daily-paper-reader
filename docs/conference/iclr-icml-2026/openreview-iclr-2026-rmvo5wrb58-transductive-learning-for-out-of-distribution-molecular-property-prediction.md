---
title: Transductive Learning for Out-of-Distribution Molecular Property Prediction
title_zh: 面向分布外分子性质预测的转导学习
authors: "Kiwoong Yoo, Hajung Kim, Soyon Park, Junseok Choe, Sunkyu Kim, Jaewoo Kang"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=rmvO5WRb58"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 基于潜在空间转导的OOD分子性质预测
tldr: 预测训练分布之外的分子性质对药物发现至关重要，但标准模型难以外推到新化学结构。已有转导方法受限于固定描述符与单锚点比较。本文提出多锚点潜在转导框架MALT，在学到的潜在空间中为查询分子选取多个相关类似物进行推理。该框架可复用任意强预训练分子编码器，提升分布外泛化能力，为药物级OOD预测提供了可迁移方案。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 标准模型难以外推到已知性质范围之外和新化学结构，OOD预测成为药物发现的瓶颈。
method: 提出多锚点潜在转导框架MALT，在潜在空间中为查询分子选取多个类似物。
result: 该框架可复用预训练编码器并提升分布外分子性质预测表现。
conclusion: 为分布外分子性质预测提供了灵活且可扩展的转导学习思路。
---

## Abstract
Predicting molecular properties outside the training data distribution (Out-of-Distribution, OOD) is critical for accelerating drug discovery. This task requires models to extrapolate beyond known property ranges and generalize to novel chemical structures—a common failure point for standard machine learning models. While transductive analogical reasoning shows promise, prior methods are often constrained by fixed descriptors and single-anchor comparisons. To overcome these limitations, we introduce Multi-Anchor Latent Transduction (MALT) framework, which operates directly within a learned latent space. MALT can leverage embeddings from any powerful, pre-trained molecular encoder to select multiple relevant analogues of query molecule. It then integrates the query and anchor embeddings to generate a final prediction. On rigorous OOD benchmarks targeting shifts in both property values and chemical features, MALT consistently improves generalization over standard inductive baselines. Notably, our framework also matches or surpasses the in-distribution performance of these base models. These findings establish multi-anchor transduction in latent space as an effective strategy to augment existing molecular encoders, enabling robust and extrapolative predictions needed to solve challenging discovery tasks.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于潜在空间转导的OOD分子性质预测。

### 2. 核心内容
预测训练分布之外的分子性质对药物发现至关重要，但标准模型难以外推到新化学结构。已有转导方法受限于固定描述符与单锚点比较。本文提出多锚点潜在转导框架MALT，在学到的潜在空间中为查询分子选取多个相关类似物进行推理。该框架可复用任意强预训练分子编码器，提升分布外泛化能力，为药物级OOD预测提供了可迁移方案。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=rmvO5WRb58](https://openreview.net/forum?id=rmvO5WRb58)
