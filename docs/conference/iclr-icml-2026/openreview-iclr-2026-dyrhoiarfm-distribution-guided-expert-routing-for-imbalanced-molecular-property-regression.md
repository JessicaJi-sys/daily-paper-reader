---
title: Distribution-Guided Expert Routing for Imbalanced Molecular Property Regression
title_zh: 面向不平衡分子性质回归的分布引导专家路由
authors: "Yan Sun, Yu Shi, Alana Deng, Zihao Jing, Carson Leung, Pingzhao Hu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=DyRhoIARfM"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 面向分子性质回归的分布感知专家路由
tldr: 分子性质回归常因目标分布不平衡而偏向密集区域，忽略稀有却关键的样本。本文提出DistRouting，一种分布感知的专家路由模块，将目标空间划分为区间并让每个专家专门负责特定区间。路由采用融合分子嵌入与理化描述符的混合机制。实验表明该模块提升了不平衡回归下的鲁棒性，为分布依赖的专家专门化与动态路由提供了可迁移范式。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 分子性质回归受目标分布不平衡困扰，标准模型易过拟合密集区域而忽视稀有样本。
method: 提出DistRouting，将目标空间分区间并为每个专家分配特定区间，路由融合分子嵌入与理化描述符。
result: 该模块在不平衡回归设置下提升了模型鲁棒性。
conclusion: 分布感知的专家专门化路由为处理不平衡与分布依赖任务提供了有效方案。
---

## Abstract
Molecular property regression often suffers from target distribution imbalance, where standard models tend to overfit to dense target regions and underperform on rare but critical ones. This limitation is particularly problematic in virtual screening, where compounds with rare property values are often of special interest. To address this challenge, we propose DistRouting, a novel distribution-aware expert routing module designed to improve model robustness under imbalanced regression settings. DistRouting partitions the target space into intervals and assigns each expert to specialize in a specific target range. Expert assignment is driven by a hybrid routing mechanism that leverages both molecular embeddings and physicochemical descriptors. To further encourage distribution-aligned representation learning, we introduce an interval-aware supervised contrastive loss that brings together samples from the same target interval and pushes apart those from different ones. Extensive experiments on multiple molecular property benchmarks show that models equipped with DistRouting consistently outperform their vanilla counterparts, especially in rare target regions. Moreover, DistRouting leads to predicted distributions that better align with the true target distributions. These findings demonstrate the effectiveness of DistRouting as a plug-in module for addressing the challenge of imbalanced molecular property regression.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向分子性质回归的分布感知专家路由。

### 2. 核心内容
分子性质回归常因目标分布不平衡而偏向密集区域，忽略稀有却关键的样本。本文提出DistRouting，一种分布感知的专家路由模块，将目标空间划分为区间并让每个专家专门负责特定区间。路由采用融合分子嵌入与理化描述符的混合机制。实验表明该模块提升了不平衡回归下的鲁棒性，为分布依赖的专家专门化与动态路由提供了可迁移范式。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=DyRhoIARfM](https://openreview.net/forum?id=DyRhoIARfM)
