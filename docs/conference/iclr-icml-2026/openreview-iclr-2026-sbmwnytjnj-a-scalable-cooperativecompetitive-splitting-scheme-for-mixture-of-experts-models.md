---
title: A scalable cooperative/competitive splitting scheme for mixture of experts models
title_zh: 一种可扩展的混合专家协作竞争分裂方案
authors: "Hien T. Nguyen-Vu, Alexey Voronin, Shyam Sankaran, Eric C Cyr, Nathaniel Trask"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=SbMWnYTJNj"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 含专家交互的混合专家训练方案
tldr: 分层混合专家模型训练通常依赖类别型门控，难以同时刻画专家间的全局与局部交互且并行度有限。本文提出一种概率期望最大化分裂方案，用融合协作与竞争机制的联合分布替代门控中的类别分布，使似然同时编码专家间的全局与局部交互。借助M分裂可并行求解局部专家子问题并用延迟修正处理全局耦合，结合分层嵌套网络实现快速多层级训练。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 混合专家的类别型门控难以刻画专家间全局与局部交互，且训练并行性受限。
method: 提出概率EM分裂方案，用协作竞争联合分布替代门控类别分布，并并行求解局部专家子问题。
result: 该方案揭示了可并行求解的M步，结合分层嵌套网络实现快速多层级训练。
conclusion: 协作竞争门控为混合专家提供了可扩展且并行友好的训练新途径。
---

## Abstract
We present a novel probabilistic expectation-maximization scheme for training hierarchical mixture-of-experts models that both exposes and exploits parallelism during training. By replacing the typical categorical distribution used in gating networks with a joint distribution blending cooperative and competitive mechanisms, we obtain a likelihood that encodes both global and local interactions between experts. The application of an M-splitting scheme reveals an M-step that enables the solution of localized, embarrassingly parallel subproblems governing local experts, with deferred corrections accounting for global coupling between experts. When combined with a hierarchical decomposition of nested networks, this yields a fast multi-level training scheme reminiscent of multigrid algorithms, which avoids under-utilization of experts, exposes further GPU parallelism and outperforms standard models on regression tasks. We provide experiments using a scalable GPU implementation that demonstrate rapid convergence and parallel scalability of the iterative scheme, as well as strong localization of the model for non-smooth, high-dimensional regression problems.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
含专家交互的混合专家训练方案。

### 2. 核心内容
分层混合专家模型训练通常依赖类别型门控，难以同时刻画专家间的全局与局部交互且并行度有限。本文提出一种概率期望最大化分裂方案，用融合协作与竞争机制的联合分布替代门控中的类别分布，使似然同时编码专家间的全局与局部交互。借助M分裂可并行求解局部专家子问题并用延迟修正处理全局耦合，结合分层嵌套网络实现快速多层级训练。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=SbMWnYTJNj](https://openreview.net/forum?id=SbMWnYTJNj)
