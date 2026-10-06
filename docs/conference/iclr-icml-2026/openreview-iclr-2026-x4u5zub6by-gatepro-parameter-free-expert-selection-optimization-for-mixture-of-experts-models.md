---
title: "GatePro: Parameter-Free Expert Selection Optimization for Mixture-of-Experts Models"
title_zh: GatePro：面向混合专家模型的无参数专家选择优化
authors: "Chen Zheng, Yuhang Cai, Deyi Liu, Jin Ma, Yiyuan Ma, Yuan Yang, Jing Liu, Yutao Zeng, Xun Zhou, Siyuan Qiao"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=X4U5ZUB6bY"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 无参数方法提升MoE专家选择多样性与专门化
tldr: 混合专家模型常同时选中功能相似的专家，造成冗余计算并限制有效容量。作者提出GatePro，一种无参数方法，通过识别最相似专家对并引入局部竞争机制来促进专家选择多样性。评估显示该方法在保持自然专门化的同时减少了冗余专家共激活，为提升专家专门化与路由质量提供了无需训练参数的方案。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: MoE常同时选中功能相似的专家，造成冗余计算与容量浪费。
method: 提出无参数GatePro，识别相似专家对并引入局部竞争以提升选择多样性。
result: 减少冗余专家共激活，同时维持自然的专家专门化。
conclusion: 为提升专家多样性与专门化提供无需额外参数的路由优化手段。
---

## Abstract
Modern large language models leverage Mixture-of-Experts (MoE) architectures for efficient scaling, but face a critical challenge: functionally similar experts are often selected simultaneously, creating redundant computation and limiting effective model capacity. Existing auxiliary balance loss methods improve token distribution but fail to address the underlying expert diversity problem. We introduce GatePro, a novel parameter-free method that directly promotes expert selection diversity. GatePro identifies the most similar expert pairs and introduces localized competition mechanisms, preventing redundant expert co-activation while maintaining natural expert specialization. Our comprehensive evaluation demonstrates GatePro's effectiveness across model scales and benchmarks. Analysis demonstrates GatePro's ability to achieve enhanced expert diversity, where experts develop more distinct and complementary capabilities, avoiding functional redundancy. This approach can be deployed hot-swappable during any training phase without additional learnable parameters, offering a practical solution for improving MoE effectiveness.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无参数方法提升MoE专家选择多样性与专门化。

### 2. 核心内容
混合专家模型常同时选中功能相似的专家，造成冗余计算并限制有效容量。作者提出GatePro，一种无参数方法，通过识别最相似专家对并引入局部竞争机制来促进专家选择多样性。评估显示该方法在保持自然专门化的同时减少了冗余专家共激活，为提升专家专门化与路由质量提供了无需训练参数的方案。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=X4U5ZUB6bY](https://openreview.net/forum?id=X4U5ZUB6bY)
