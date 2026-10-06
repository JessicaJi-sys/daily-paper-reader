---
title: "ASMG: Data Structure-Aware Routing via Incremental Subspace Learning for MoE"
title_zh: ASMG：面向混合专家的基于数据结构感知路由的增量子空间学习
authors: "Sumin Park, Noseong Park"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=xsqiDQjSvV"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 数据驱动的动态门控以捕获输入结构变化
tldr: 混合专家模型的性能高度依赖门控机制，但常见门控仅为浅层线性投影，难以刻画输入的结构差异，导致专家专门化不足与路由次优。本文提出自适应结构感知门控ASMG，通过广义Hebbian算法学习演化的主成分子空间，并与可学习门控矩阵动态插值。该机制增强了门控的表达能力，能根据输入结构动态路由到更合适的专家，为样本级动态专家路由提供了可迁移的方法。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 混合专家模型依赖门控进行路由，但常用门控只是浅层线性投影加激活，表达力不足，难以捕捉输入结构变化，导致专家专门化弱、路由次优。
method: 论文提出自适应结构感知门控ASMG，用广义Hebbian算法增量学习演化主成分子空间，并与标准可学习门控矩阵动态插值形成数据驱动门控。
result: 该门控机制提升了门控表达力与专家专门化质量，使路由能更好反映输入结构差异，从而改善混合专家模型的整体表现。
conclusion: 研究说明更结构感知的动态门控有助于专家专门化与样本级路由，对药物对级动态MoE路由具有方法借鉴意义。
---

## Abstract
Mixture-of-Experts (MoE) models scale model capacity efficiently by selectively
routing inputs to a subset of specialized experts. However, their performance
critically hinges on the gating mechanism, which is typically implemented as
a shallow linear projection followed by a softmax or sigmoid activation. This
minimal design lacks the representational capacity to capture structural variations
in the input, often resulting in weak expert specialization and suboptimal routing.
To address this limitation, we propose Adaptive Structure-Aware MoE Gating
(ASMG), a data-driven gating mechanism that dynamically interpolates between
a standard learnable gating matrix and an evolving principal subspace learned
via the Generalized Hebbian Algorithm (GHA). By tracking input structure with
iterative basis updates, ASMG enables the gating function to remain both task-
supervised and structure-aware throughout training. We validate our method
through (i) a highly controlled synthetic task based on multinomial HMMs and (ii)
extensive real-world benchmarks spanning multiple domains and training regimes,
including both finetuning and pretraining. Across a wide range of evaluations,
ASMG achieves consistent gains over strong MoE baselines. Moreover, optionally
enabling unsupervised GHA updates at test time further improves robustness under
distribution shifts, offering an online adaptation mechanism that enhances standard
gating with stronger OOD resilience.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
数据驱动的动态门控以捕获输入结构变化。

### 2. 核心内容
混合专家模型的性能高度依赖门控机制，但常见门控仅为浅层线性投影，难以刻画输入的结构差异，导致专家专门化不足与路由次优。本文提出自适应结构感知门控ASMG，通过广义Hebbian算法学习演化的主成分子空间，并与可学习门控矩阵动态插值。该机制增强了门控的表达能力，能根据输入结构动态路由到更合适的专家，为样本级动态专家路由提供了可迁移的方法。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=xsqiDQjSvV](https://openreview.net/forum?id=xsqiDQjSvV)
