---
title: Load Balancing Mixture of Experts with Similarity Preserving Routers
title_zh: 基于相似度保持路由器的专家混合负载均衡
authors: "Nabil Omi, Siddhartha Sen, Ali Farhadi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=FNuvMnGAm8"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 学习型路由器为输入分配专家，相似度保持路由提升路由一致性
tldr: 稀疏专家混合模型通过路由为每个输入激活少量专家，但缺乏平衡机制时路由常塌缩至少数专家，限制模型容量并造成冗余知识。该文提出相似度保持路由器，使专家分配在训练中更一致，从而缓解路由塌缩与知识冗余问题。实验表明该路由机制在保持负载均衡的同时改善了模型性能与容量利用。其贡献在于为动态专家路由的稳定性提供了可迁移的改进方案。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 稀疏专家混合的路由器易塌缩至少数专家，限制模型容量并在训练中产生冗余知识。
method: 提出相似度保持路由器，使专家分配在训练过程中更一致，从而改进传统负载均衡机制。
result: 在保持负载均衡的同时提升了路由一致性与模型性能，缓解了专家利用不足问题。
conclusion: 为动态专家路由的稳定性与容量利用提供了可迁移的改进方案。
---

## Abstract
Sparse Mixture of Experts (MoE) models offer a scalable and efficient architecture for training large neural networks by activating only a subset of parameters (“experts”) for each input. A learned router computes a distribution over these experts, and assigns input tokens to a small subset. However, without auxiliary balancing mechanisms, routers often converge to using only a few experts, severely limiting model capacity and degrading performance. Most current load balancing mechanisms encourage a distribution over experts that resembles a roughly uniform distribution of experts per token. During training, this can result in inconsistent routing behavior, resulting in the model spending its' capacity to learn redundant knowledge. We address this by introducing a novel load balancing loss that preserves token-wise relational structure, encouraging consistent expert choices for similar inputs during training. Our experimental results show that applying our loss to the router over a popular load balancing loss results in 35% faster convergence and lower redundancy, while removing balancing hyper-parameters completely.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
学习型路由器为输入分配专家，相似度保持路由提升路由一致性。

### 2. 核心内容
稀疏专家混合模型通过路由为每个输入激活少量专家，但缺乏平衡机制时路由常塌缩至少数专家，限制模型容量并造成冗余知识。该文提出相似度保持路由器，使专家分配在训练中更一致，从而缓解路由塌缩与知识冗余问题。实验表明该路由机制在保持负载均衡的同时改善了模型性能与容量利用。其贡献在于为动态专家路由的稳定性提供了可迁移的改进方案。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=FNuvMnGAm8](https://openreview.net/forum?id=FNuvMnGAm8)
