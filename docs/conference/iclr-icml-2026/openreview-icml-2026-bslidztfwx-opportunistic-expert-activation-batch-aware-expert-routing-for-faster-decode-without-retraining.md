---
title: "Opportunistic Expert Activation: Batch-Aware Expert Routing for Faster Decode Without Retraining"
title_zh: 机会式专家激活：无需重训的批感知专家路由以加速解码
authors: "Costin-Andrei Oncescu, Qingyang Wu, Wai Tong Chung, Tsai-chuan Wu, Bryan Dev Gopal, Junxiong Wang, Tri Dao, Ben Athiwaratkun"
date: 2026-04-30
pdf: "https://openreview.net/pdf/bc79906c3b98f546d7bc8bea98f61b105560763a.pdf"
tags: ["query:ddi-moe"]
score: 4.0
evidence: 批感知的令牌到专家动态重路由
tldr: 混合专家大模型在自回归生成时，专家平均负载增长慢于稠密层，导致中等批次下进入内存受限状态，解码延迟由激活专家数决定。本文提出一种动态重路由框架，将令牌到专家的映射重新分配，在保持生成质量的同时降低激活专家数量。其中批感知路由利用同批令牌的共享信息进一步优化路由。该工作聚焦效率而非泛化，但其动态路由机制对样本级专家调度有一定借鉴价值。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 采用混合专家的语言模型在自回归解码时易进入内存受限状态，延迟由激活专家数决定，如何在保证质量下降低激活专家数是效率瓶颈。
method: 论文提出动态重路由框架，重新分配令牌到专家的映射以减少激活专家数，并采用批感知路由让同批令牌协同决定专家选择。
result: 实验表明该方法能在保持可比生成质量的前提下降低激活专家数量，从而减少解码延迟，提升推理效率。
conclusion: 该工作提供了一种面向效率的动态专家路由机制，虽非针对泛化，但对样本级专家调度与路由设计仍有参考价值。
---

## Abstract
An increasing number of LLMs employ Mixture-of-Experts (MoE) architectures where the feed-forward layer is replaced by a pool of experts and each token only activates a small subset of them. During autoregressive generation, these models often enter a memory-bound regime even for moderate batch sizes because the average expert load grows more slowly than in an equivalent dense feedforward layer. Consequently, MoE latency is governed by the number of activated experts. We introduce a framework for $\textbf{dynamically}$ re-routing token-to-expert mapping to lower this number (and thus, the decode latency) while preserving a comparable quality. Our best results use a $\textbf{batch-aware routing}$ that works by having tokens $\textbf{piggyback}$ experts that have already been loaded into memory due to being crucial to other tokens within the same batch. At batch size $16$, OEA reduces MoE-layer decode latency by $39\\%$ on Qwen3-30B while preserving standard-error-adjusted downstream accuracy, and by $15\\%$ on Qwen3-235B with only small overall degradation on the long-generation benchmark suite.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
批感知的令牌到专家动态重路由。

### 2. 核心内容
混合专家大模型在自回归生成时，专家平均负载增长慢于稠密层，导致中等批次下进入内存受限状态，解码延迟由激活专家数决定。本文提出一种动态重路由框架，将令牌到专家的映射重新分配，在保持生成质量的同时降低激活专家数量。其中批感知路由利用同批令牌的共享信息进一步优化路由。该工作聚焦效率而非泛化，但其动态路由机制对样本级专家调度有一定借鉴价值。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=bSLIDztFwx](https://openreview.net/forum?id=bSLIDztFwx)
