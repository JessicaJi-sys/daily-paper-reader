---
title: "RouterInterp: Understanding Superposed Specialisation in Mixture of Experts Routing"
title_zh: RouterInterp：理解混合专家路由中的叠加专门化
authors: "Ilya Lasy, Nora Yinuo Cai, Kola Ayonrinde"
date: 2026-04-30
pdf: "https://openreview.net/pdf/0ae12764b6dde91958436bb97b58a24f40979ab3.pdf"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 解释MoE专家路由的叠加专门化假设
tldr: 该文质疑每个专家只专精单一领域的传统假设，指出基于该假设的可解释性研究多不成功。作者提出叠加专门化假设，认为专家实际专精于细粒度特征的并集，并据此提出RouterInterp方法，用稀疏自编码器特征识别最能预测专家路由的因素。该工作揭示了专家专门化的真实结构，对理解与设计无需人工定义语义的专家分工具有参考价值。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 传统认为专家专精单一领域，但基于该假设的可解释性研究多不成功。
method: 提出叠加专门化假设与RouterInterp，用稀疏自编码器特征解释路由。
result: 发现专家实际专精于细粒度特征并集而非单一领域。
conclusion: 揭示了专家专门化的真实结构，有助于设计无需人工语义的专家分工。
---

## Abstract
Sparse Mixture of Experts (MoE) models scale more efficiently than dense models by routing tokens to modular expert networks that are only active when relevant to the task. A leading hypothesis for the performance of MoE models is that each expert specialises in a single, coherent domain. However, interpretability efforts that assume this hypothesis have generally been unsuccessful. We propose and present evidence for an alternative account that we call the *Superposed Specialisation Hypothesis* (SSH): experts specialise in a disjoint union of fine-grained features rather than one broad domain. Leveraging the SSH, we introduce *RouterInterp*, a method for interpreting expert routing that identifies Sparse Autoencoder features most predictive of routing decisions and produces unified natural language explanations. On gpt-oss-20b, RouterInterp explains expert routing with 57% higher detection accuracy than prior token statistics based methods. This work provides a scalable method for generating concise and more accurate explanations of expert routing and increases our understanding of a previously uninterpretable component of foundation models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
解释MoE专家路由的叠加专门化假设。

### 2. 核心内容
该文质疑每个专家只专精单一领域的传统假设，指出基于该假设的可解释性研究多不成功。作者提出叠加专门化假设，认为专家实际专精于细粒度特征的并集，并据此提出RouterInterp方法，用稀疏自编码器特征识别最能预测专家路由的因素。该工作揭示了专家专门化的真实结构，对理解与设计无需人工定义语义的专家分工具有参考价值。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=rDNCWfRd69](https://openreview.net/forum?id=rDNCWfRd69)
