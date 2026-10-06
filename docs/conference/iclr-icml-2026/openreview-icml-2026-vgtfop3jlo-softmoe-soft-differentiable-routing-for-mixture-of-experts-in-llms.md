---
title: "SoftMoE: Soft Differentiable Routing for Mixture-of-Experts in LLMs"
title_zh: SoftMoE：面向大语言模型混合专家的软可微路由
authors: "Mikołaj Zasada, Łukasz Struski, Jacek Tabor, Marcin Kurdziel"
date: 2026-04-30
pdf: "https://openreview.net/pdf/b4e9690299e573400b7d1f764f389f69c502e6f3.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 软可微的动态专家路由
tldr: 稀疏MoE通过top-k路由仅激活少量专家，在固定推理预算下扩展LLM参数，但离散top-k不可微，强制每个输入激活固定数量专家，造成计算利用低效。本文提出SoftMoE，用截断软top-k的LapSum松弛替代离散路由，使专家路由可基于梯度优化。该方法还参数化每层平均激活专家数并施加全局预算约束，使模型自主学习跨层的专家容量分配。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 离散top-k路由不可微，强制每个输入激活固定数量专家，导致计算利用效率低下。
method: 提出SoftMoE，用截断软top-k的LapSum松弛实现可微路由，并参数化每层专家激活数与全局预算。
result: 模型可基于梯度优化路由并自主学习跨层专家容量分配，且保持与现有架构兼容。
conclusion: 软可微路由为MoE的动态专家分配提供了更高效灵活的训练方式。
---

## Abstract
Sparse Mixture-of-Experts (MoE) architectures enable scaling LLM parameters under a fixed inference budget by activating only a small subset of experts via top-$k$ routing. While this preserves causality and suits autoregressive language models, the discrete top-$k$ operator is not differentiable, forcing a fixed number of active experts per input and resulting in inefficient use of computation. We propose SoftMoE, which replaces discrete routing with a truncated soft top-$k$ LapSum relaxation, allowing gradient-based optimization of expert routing. We further parameterize the mean number of active experts per layer and impose a global budget constraint, enabling the model to learn how to allocate expert capacity across layers. SoftMoE remains fully compatible with autoregressive modeling and achieves performance comparable to or better than sparse MoE on language modeling and downstream tasks, while activating significantly fewer experts. Notably, the learned allocation is highly non-uniform, with later layers activating more experts. The source code is publicly available$^\dagger$.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
软可微的动态专家路由。

### 2. 核心内容
稀疏MoE通过top-k路由仅激活少量专家，在固定推理预算下扩展LLM参数，但离散top-k不可微，强制每个输入激活固定数量专家，造成计算利用低效。本文提出SoftMoE，用截断软top-k的LapSum松弛替代离散路由，使专家路由可基于梯度优化。该方法还参数化每层平均激活专家数并施加全局预算约束，使模型自主学习跨层的专家容量分配。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=vGTFOp3jLO](https://openreview.net/forum?id=vGTFOp3jLO)
