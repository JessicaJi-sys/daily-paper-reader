---
title: Scaling Continual Learning to 300+ Tasks with Bi-Level Routing Mixture-of-Experts
title_zh: 基于双层路由混合专家将持续学习扩展到300多个任务
authors: "Meng Lou, Yunxiang Fu, Yizhou Yu"
date: 2026-04-30
pdf: "https://openreview.net/pdf/8b99d08ba33bbe52dff555568b128db0d3973109.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 双层路由MoE动态激活任务路由器与专家
tldr: 针对超长任务序列下持续学习难以兼顾稳定性和可塑性的问题，本文提出CaRE，一种采用双层路由混合专家（BR-MoE）的可扩展持续学习器。其双层路由先动态激活任务专属路由器，再激活并聚合专家，实现判别性与综合性特征的协同学习。实验表明该方法在300多个任务上保持稳定与可塑性，为长序列持续学习提供了高效路由范式。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 超长任务序列下持续学习难以同时保持稳定性和可塑性。
method: 提出CaRE，用双层路由混合专家先选任务路由器再激活聚合专家。
result: 在300多个任务上实现稳定与可塑性兼顾的可扩展学习。
conclusion: 双层路由MoE为长序列持续学习提供高效可扩展方案。
---

## Abstract
Continual learning, especially class-incremental learning (CIL), on the basis of a pre-trained model (PTM) has garnered substantial research interest in recent years. However, how to effectively learn both discriminative and comprehensive feature representations while maintaining stability and plasticity over very long task sequences remains an open problem. We propose $\mathbf{CaRE}$, a scalable $\mathbf{C}$ontinual Le$\mathbf{a}$rner with efficient Bi-Level $\mathbf{R}$outing Mixture-of-$\mathbf{E}$xperts (BR-MoE). The core idea of BR-MoE is a bi-level routing mechanism: a router selection stage that dynamically activates relevant task-specific routers, followed by an expert routing phase that dynamically activates and aggregates experts, aiming to inject discriminative and comprehensive representations into every intermediate network layer. 
On the other hand, we introduce a challenging dataset, OmniBenchmark-1K, for CIL performance evaluation on very long task sequences with hundreds of tasks.
Extensive experiments show that CaRE demonstrates leading performance across a variety of datasets and task settings, including commonly used CIL datasets with classical CIL settings (e.g., 5-20 tasks).
To the best of our knowledge, CaRE is the first continual learner that scales to very long task sequences (ranging from 100 to over 300 non-overlapping tasks), while outperforming all baselines by a large margin on such task sequences.
We hope that this work will inspire further research into continual learning over extremely long task sequences.
Code and dataset are publicly released at https://github.com/LMMMEng/CaRE.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
双层路由MoE动态激活任务路由器与专家。

### 2. 核心内容
针对超长任务序列下持续学习难以兼顾稳定性和可塑性的问题，本文提出CaRE，一种采用双层路由混合专家（BR-MoE）的可扩展持续学习器。其双层路由先动态激活任务专属路由器，再激活并聚合专家，实现判别性与综合性特征的协同学习。实验表明该方法在300多个任务上保持稳定与可塑性，为长序列持续学习提供了高效路由范式。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=Tvcii7gyRX](https://openreview.net/forum?id=Tvcii7gyRX)
