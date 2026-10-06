---
title: Continual Learning of Domain-Invariant Representations
title_zh: 领域不变表示的持续学习
authors: "Pascal Janetzky, Tobias Schlagenhauf, Stefan Feuerriegel"
date: 2026-04-30
pdf: "https://openreview.net/pdf/422b033d9a2957abf307769187ebc897d5ec8398.pdf"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 学习领域不变表示以泛化到未见领域
tldr: 持续学习按序在多个领域上训练模型，但现有方法只优化域内性能，容易学到领域特有的伪相关线索，导致部署后难以泛化到未见领域。本文提出一类持续学习领域不变表示的方法，通过序列化地捕捉跨领域的不变结构来保留潜在因果机制。分析表明这类不变结构可降低对领域特定线索的过拟合风险，从而提升对未见领域的泛化能力。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 持续学习只优化域内性能，易学到领域特有的伪相关线索，损害对未见领域的泛化。
method: 提出一类序列化学习领域不变表示的持续学习方法，捕捉跨领域不变结构以保留因果机制。
result: 分析显示不变结构能降低对领域特定线索的过拟合，从而改善未见领域泛化。
conclusion: 将领域不变表示引入持续学习可有效缓解捷径学习与分布偏移问题。
---

## Abstract
Continual learning (CL) aims to train models sequentially over multiple domains without forgetting previously learned knowledge. However, existing CL methods optimize for in-domain performance and are therefore prone to learning spurious, domain-specific cues ("shortcut learning"), which limits generalization to unseen domains after deployment. In this paper, we address this limitation through *continual learning of domain-invariant representation*. We introduce a broad class of CL methods that sequentially learn representations capturing invariant structures across domains. Our methods are motivated by the observation that such invariant structures often preserve the underlying causal mechanisms, which can reduce the risk of overfitting to domain-specific cues and thus offer better out-of-domain generalization. Our proposed CL methods combine replay-based training with a tailored sequential invariance alignment to learn---and preserve---invariant structures over time. We evaluate our methods under a deployment-oriented protocol that measures performance on unseen target domains. Across six benchmark and real-world datasets spanning vision, medicine, manufacturing, and ecology, our methods consistently outperform existing CL baselines in terms of generalization to unseen target domains. As an ablation, we further show that naïve extensions of sequential training with existing domain-invariant representation learning (DIRL) methods provide only limited benefits. To the best of our knowledge, this is the first work to develop domain-invariant representation methods for CL.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
学习领域不变表示以泛化到未见领域。

### 2. 核心内容
持续学习按序在多个领域上训练模型，但现有方法只优化域内性能，容易学到领域特有的伪相关线索，导致部署后难以泛化到未见领域。本文提出一类持续学习领域不变表示的方法，通过序列化地捕捉跨领域的不变结构来保留潜在因果机制。分析表明这类不变结构可降低对领域特定线索的过拟合风险，从而提升对未见领域的泛化能力。

### 3. 对应检索需求
invariant representation learning for stable drug generalization。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=EH77N5YGwV](https://openreview.net/forum?id=EH77N5YGwV)
