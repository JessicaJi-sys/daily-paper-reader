---
title: "DARE:Difficulty-Aware Dynamic Routing for Mixture of Experts"
title_zh: DARE：面向专家混合的难度感知动态路由
authors: "Zhou Tao, YongXiang Hua, Chaohu Liu, Shida Wang, Linli Xu"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=S7o8zBYw4V"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 依据token难度进行动态专家路由而非固定Top-K
tldr: 针对稀疏专家混合常用Top-K路由为每个token固定分配专家数、忽略样本复杂度差异，导致简单样本算力浪费而复杂样本处理不足的问题，本文提出难度感知动态路由DARE。该方法引入有原则的机制，依据token级难度显式指导专家的动态分配数量。实验表明动态调整专家数量能改善简单与复杂样本的处理，提升资源利用效率与模型性能。该工作为样本级动态路由提供新思路，对药物对级动态专家路由设计具有方法借鉴价值。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 稀疏MoE常用Top-K为每个token固定分配专家数，忽略样本复杂度差异，导致算力分配次优。
method: 提出难度感知动态路由DARE，依据token级难度显式指导每个样本的专家分配数量。
result: 动态调整专家数量，改善简单与复杂样本的处理，提升资源利用与模型整体性能。
conclusion: 表明样本级动态路由优于静态分配，对药物对级动态专家路由具有直接的方法借鉴意义。
---

## Abstract
Sparse Mixture-of-Experts (MoE) architectures have become a foundational approach for efficiently scaling Large Vision-Language Models (LVLMs), as they activate only a subset of parameters for each input. However, the commonly adopted Top-K routing strategy assigns a fixed number of experts to every token, ignoring the natural variation in token complexity. This static allocation often results in suboptimal resource utilization, where simple tokens receive excessive computation and complex tokens are insufficiently processed. While recent dynamic routing methods attempt to address this limitation, they lack principled mechanisms to explicitly guide expert allocation based on token-level difficulty, resulting in suboptimal performance in practice.
In this paper, we propose \textbf{D}ifficulty-\textbf{A}ware Dynamic \textbf{R}outing for Mixture of \textbf{E}xperts (\textbf{DARE}), a novel routing strategy that adapts expert selection according to the complexity of each token. DARE %incorporates
introduces a lightweight predictor that estimates the difficulty of individual tokens based on their log-perplexity as a theoretically grounded proxy, and employs a set of learnable thresholds to dynamically determine the appropriate number of experts to activate. This mechanism enables fine-grained and adaptive allocation of computational resources, allowing the model to devote more capacity to challenging tokens while conserving resources on easier ones. Extensive experiments on standard vision-language benchmarks demonstrate that DARE consistently outperforms both fixed Top-K routing and existing adaptive routing strategies. It achieves superior task performance while simultaneously improving computational efficiency, highlighting the effectiveness and generality of difficulty-aware routing in sparse MoE architectures for large-scale multimodal models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
依据token难度进行动态专家路由而非固定Top-K。

### 2. 核心内容
针对稀疏专家混合常用Top-K路由为每个token固定分配专家数、忽略样本复杂度差异，导致简单样本算力浪费而复杂样本处理不足的问题，本文提出难度感知动态路由DARE。该方法引入有原则的机制，依据token级难度显式指导专家的动态分配数量。实验表明动态调整专家数量能改善简单与复杂样本的处理，提升资源利用效率与模型性能。该工作为样本级动态路由提供新思路，对药物对级动态专家路由设计具有方法借鉴价值。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=S7o8zBYw4V](https://openreview.net/forum?id=S7o8zBYw4V)
