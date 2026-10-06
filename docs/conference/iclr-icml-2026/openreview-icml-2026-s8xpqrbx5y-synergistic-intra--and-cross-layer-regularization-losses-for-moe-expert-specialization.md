---
title: Synergistic Intra- and Cross-Layer Regularization Losses for MoE Expert Specialization
title_zh: 面向MoE专家专门化的层内与跨层协同正则损失
authors: "Rizhen Hu, Yuan Cao, Boao Kong, Mou Sun, Kun Yuan"
date: 2026-04-30
pdf: "https://openreview.net/pdf/6331595e27a804fbb623ac57b61d8342608ad779.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 辅助损失促进MoE专家专门化，无需人工定义专家语义
tldr: 稀疏混合专家模型常因专家功能重叠、路由模糊而浪费容量，现有架构改造方案依赖大量结构修改。作者提出两种即插即用的层内与跨层正则损失，惩罚专家激活相似度以促进互补专门化。实验显示该方法在不改动路由器与架构的前提下提升了专家专门化与路由效率，为专家自发形成专门知识整合策略提供了训练信号。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: MoE专家功能重叠导致冗余计算与路由模糊，现有架构方案需大量结构改动。
method: 提出层内与跨层即插即用正则损失，惩罚专家激活相似度以促进专门化。
result: 在不修改路由器与架构下提升专家专门化与路由效率。
conclusion: 为专家自发专门化提供轻量训练信号，避免人工定义专家语义。
---

## Abstract
Sparse Mixture-of-Experts (MoE) models scale Transformers efficiently but suffer from expert overlap, where different experts process similar tokens and learn redundant functions, resulting in ambiguous routing and underutilized capacity. While architectural solutions like DeepSeek-style shared experts promote specialization, they require substantial structural modifications and rely solely on intra-layer signals. We propose two plug-and-play auxiliary losses that enhance MoE specialization and routing efficiency without modifying routers or model architectures. First, an intra-layer specialization loss penalizes cosine similarity between experts' SwiGLU activations on identical tokens, encouraging experts to specialize in complementary functions. Second, a cross-layer dependency loss maximizes joint Top-$k$
 routing probabilities across adjacent layers, establishing coherent expert pathways through network depth while reinforcing intra-layer specialization. Both losses are orthogonal to the standard load-balancing loss and compatible with shared-expert and vanilla Top-$k$
 MoE architectures. We implement both losses as a drop-in Megatron-LM module. Extensive experiments across pre-training, fine-tuning, and zero-shot benchmarks demonstrate consistent task gains, higher expert specialization, and lower-entropy routing; together, these improvements translate into faster inference via more stable expert pathways.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
辅助损失促进MoE专家专门化，无需人工定义专家语义。

### 2. 核心内容
稀疏混合专家模型常因专家功能重叠、路由模糊而浪费容量，现有架构改造方案依赖大量结构修改。作者提出两种即插即用的层内与跨层正则损失，惩罚专家激活相似度以促进互补专门化。实验显示该方法在不改动路由器与架构的前提下提升了专家专门化与路由效率，为专家自发形成专门知识整合策略提供了训练信号。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=S8XPQrBX5y](https://openreview.net/forum?id=S8XPQrBX5y)
