---
title: Self-Supervised Learning from Structural Invariance
title_zh: 从结构不变性出发的自监督学习
authors: "Yipeng Zhang, Hafez Ghaemi, Jungyoon Lee, Shahab Bakhtiari, Eilif B. Muller, Laurent Charlin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=r3JUDAYjIH"
tags: ["query:ood-inv"]
score: 4.0
evidence: 基于数据对结构不变性的自监督表示学习
tldr: 本文针对联合嵌入自监督学习中数据对存在一对多映射、现有方法难以灵活刻画条件不确定性的问题展开研究。作者引入潜变量并对成对嵌入互信息推导变分下界，从而得到一种简洁的正则项。该方法可增强表示学习对不变性的建模能力，对鲁棒表示学习有方法层面的借鉴意义，但与DDI或环境无关不变学习关联较弱。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 联合嵌入自监督学习面临数据对一对多映射问题，现有方法难以灵活捕捉条件不确定性。
method: 引入潜变量并对成对嵌入互信息推导变分下界，得到可加于标准SSL目标的简洁正则项。
result: 实验表明该方法能更灵活地建模数据对不变性，提升表示学习效果。
conclusion: 该工作为自监督表示学习中的不变性建模提供了概率视角的通用正则方法。
---

## Abstract
Joint-embedding self-supervised learning (SSL), the key paradigm for unsupervised representation learning from visual data, learns from invariances between semantically-related data pairs.
We study the one-to-many mapping problem in SSL,
where each datum may be mapped to multiple valid targets. 
This arises when data pairs come from naturally occurring generative processes, e.g., successive video frames.
We show that existing methods struggle to flexibly capture this conditional uncertainty. As a remedy, we introduce 
a latent variable to account for this uncertainty and derive a variational lower bound on the mutual information between paired embeddings.
Our derivation yields a simple regularization term for standard SSL objectives.
The resulting method, which we call
AdaSSL, applies to both contrastive and 
distillation-based
SSL objectives, and we empirically show its versatility in
causal representation learning,
fine-grained image understanding, and world modeling on videos.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于数据对结构不变性的自监督表示学习。

### 2. 核心内容
本文针对联合嵌入自监督学习中数据对存在一对多映射、现有方法难以灵活刻画条件不确定性的问题展开研究。作者引入潜变量并对成对嵌入互信息推导变分下界，从而得到一种简洁的正则项。该方法可增强表示学习对不变性的建模能力，对鲁棒表示学习有方法层面的借鉴意义，但与DDI或环境无关不变学习关联较弱。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=r3JUDAYjIH](https://openreview.net/forum?id=r3JUDAYjIH)
