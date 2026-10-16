---
title: Unlocking Out-of-Distribution Generalization in Transformers via Latent Space Reasoning
title_zh: 通过潜在空间推理解锁Transformer的分布外泛化能力
authors: "Awni Altabaa, Siyu Chen, John Lafferty, Zhuoran Yang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=Wjgq9ISdP0"
tags: ["query:ood-inv"]
score: 5.0
evidence: 通过锚定潜在表示等架构机制提升分布外泛化
tldr: 针对Transformer在训练分布之外系统性组合泛化能力不足的问题，本文以模块化算术计算图任务为测试平台，探索四种提升OOD泛化的架构机制：输入自适应递归、算法监督、基于离散瓶颈的锚定潜在表示以及显式纠错机制。实验表明这些机制协同作用可显著增强模型的算法式组合泛化能力。该工作聚焦架构层面的OOD泛化，对理解表示稳定性与泛化关系有参考价值。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: Transformer在训练分布之外的组合泛化能力不足，成为其推理能力的关键瓶颈。
method: 以模块化算术任务为平台，引入输入自适应递归、算法监督、离散瓶颈锚定表示和显式纠错四种机制。
result: 四种机制协同提升了模型在未见组合上的算法式泛化表现。
conclusion: 架构层面的表示锚定与纠错可有效增强OOD泛化，具有方法论借鉴意义。
---

## Abstract
Systematic, compositional generalization beyond the training distribution remains a core challenge in machine learning---and a critical bottleneck for the emergent reasoning abilities of modern language models. This work investigates out-of-distribution (OOD) generalization in Transformer networks using a GSM8K-style modular arithmetic on computational graphs task as a testbed. We introduce and explore a set of four architectural mechanisms aimed at enhancing OOD algorithmic generalization: (i) input-adaptive recurrence; (ii) algorithmic supervision; (iii) anchored latent representations via a discrete bottleneck; and (iv) an explicit error-correction mechanism. Collectively, these mechanisms yield an architectural approach for native and scalable latent space reasoning in Transformer networks with robust algorithmic generalization capabilities. We complement these empirical results with a detailed mechanistic interpretability analysis that reveals how these mechanisms give rise to robust OOD generalization abilities.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过锚定潜在表示等架构机制提升分布外泛化。

### 2. 核心内容
针对Transformer在训练分布之外系统性组合泛化能力不足的问题，本文以模块化算术计算图任务为测试平台，探索四种提升OOD泛化的架构机制：输入自适应递归、算法监督、基于离散瓶颈的锚定潜在表示以及显式纠错机制。实验表明这些机制协同作用可显著增强模型的算法式组合泛化能力。该工作聚焦架构层面的OOD泛化，对理解表示稳定性与泛化关系有参考价值。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=Wjgq9ISdP0](https://openreview.net/forum?id=Wjgq9ISdP0)
