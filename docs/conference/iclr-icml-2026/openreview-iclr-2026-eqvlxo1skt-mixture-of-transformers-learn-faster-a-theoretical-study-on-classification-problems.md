---
title: "Mixture-of-Transformers Learn Faster: A Theoretical Study on Classification Problems"
title_zh: 混合Transformer学习更快：分类问题的理论研究
authors: "Hongbo Li, Qinhang Wu, Sen Lin, Yingbin Liang, Ness Shroff"
date: 2025-09-12
pdf: "https://openreview.net/pdf?id=eqvlxO1sKT"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 专家专门化与门控路由的理论研究
tldr: 本文针对混合专家模型缺乏统一理论解释的问题，提出混合Transformer（MoT）的可分析框架，让每个Transformer块充当由持续训练门控网络调度的专家，并设计三阶段训练算法。理论分析表明，各专家会专门化于不同任务类别，门控网络能准确将样本路由到对应专家。该结果为专家专门化与动态路由的学习动力学提供了理论依据，有助于理解无需人工定义专家语义的自动分工机制。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 混合专家模型虽提升效率，但缺乏统一理论解释，尤其当注意力层与前馈层都可专门化时，专家专门化与门控路由的学习机制尚不清晰。
method: 论文提出混合Transformer（MoT）框架，将每个Transformer块视为由持续训练门控网络调度的专家，并设计三阶段训练算法以分离研究专家专门化与注意力对齐的动态。
result: 理论分析显示，每个Transformer专家会专门化于不同任务类别，门控网络能准确把数据样本路由至相应专家，从而实现高效的任务分工。
conclusion: 该工作为混合专家架构中专家自动专门化与门控路由提供了可证明的理论支撑，对理解自动知识整合策略具有参考价值。
---

## Abstract
Mixture-of-Experts (MoE) models improve transformer efficiency but lack a unified theoretical explanation—especially when both feed-forward and attention layers are allowed to specialize. To this end, we study the Mixture-of-Transformers (MoT), a tractable theoretical framework in which each transformer block acts as an expert governed by a continuously trained gating network. This design allows us to isolate and study the core learning dynamics of expert specialization and attention alignment. In particular, we develop a three-stage training algorithm with continuous training of the gating network, and show that each transformer expert specializes in a distinct class of tasks and that the gating network accurately routes data samples to the correct expert. Our analysis shows how expert specialization reduces gradient conflicts and makes each subtask strongly convex. We prove that the training drives the expected prediction loss to near zero in $\mathcal{O}(\log(\epsilon^{-1}))$ iteration steps, significantly improving over the $\mathcal{O}(\epsilon^{-1})$ rate for a single transformer. We further validate our theoretical findings through extensive real-data experiments, demonstrating the practical effectiveness of MoT. Together, these results offer the first unified theoretical account of transformer-level specialization and learning dynamics, providing practical guidance for designing efficient large-scale models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
专家专门化与门控路由的理论研究。

### 2. 核心内容
本文针对混合专家模型缺乏统一理论解释的问题，提出混合Transformer（MoT）的可分析框架，让每个Transformer块充当由持续训练门控网络调度的专家，并设计三阶段训练算法。理论分析表明，各专家会专门化于不同任务类别，门控网络能准确将样本路由到对应专家。该结果为专家专门化与动态路由的学习动力学提供了理论依据，有助于理解无需人工定义专家语义的自动分工机制。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=eqvlxO1sKT](https://openreview.net/forum?id=eqvlxO1sKT)
