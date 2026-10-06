---
title: "Mixing Expertise with Confidence: A Mixture of Experts Framework for Robust Multi-Modal Continual Learning"
title_zh: 以置信度混合专长：面向稳健多模态持续学习的混合专家框架
authors: "Md Abdullah Al Forhad, Yuansheng Zhu, Abhinab Acharya, Xumin Liu, Qi Yu, Weishi Shi"
date: 2026-04-30
pdf: "https://openreview.net/pdf/a5c995d519a970222068a69b4e6222ed293f8781.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 无需任务ID预测器的MoE动态专家知识共享
tldr: 该文针对持续学习中MoE的共享参数空间随任务增多成为瓶颈、且完全独立专家需显式任务ID预测器的问题。作者取消任务间共享空间与任务ID预测器，通过开放集学习实现专家间通信，使知识能像人类协作一样动态共享。该方法缓解了灾难性遗忘并简化了路由设计，为无需人工定义语义的专家知识整合提供了可迁移范式。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 持续学习中MoE共享空间随任务增多成瓶颈，独立专家又需任务ID预测器。
method: 取消共享空间与任务ID预测器，借开放集学习实现专家间动态知识共享。
result: 该方法缓解了灾难性遗忘并降低了路由设计的复杂度。
conclusion: 为无需人工语义的专家知识动态整合提供了可迁移范式。
---

## Abstract
The Mixture of Experts (MoE) framework is widely used in continual learning to mitigate catastrophic forgetting. MoEs typically combine a small inter-task shared parameter space with largely independent expert parameters. However, as the number of tasks increases, the shared space becomes a bottleneck, reintroducing forgetting, while fully independent experts require explicit task ID predictors (e.g., routers), adding complexity. In this work, we eliminate the inter-task shared parameter space and the need for a task ID predictor by enabling expert communication and allowing knowledge to be shared dynamically, akin to human collaboration. We bridge the inter-expert knowledge sharing by leveraging the open-set learning capabilities of a multimodal foundation model (e.g., CLIP), thereby providing “expert priors” that bolster each expert’s task-specific representations. Guided by these priors, experts learn calibrated inter-task posteriors. Additionally, multivariate Gaussians over the learned posteriors promote complementary specialization among experts. We propose new evaluation benchmarks that simulate realistic continual learning scenarios, and our prior-conditioned strategy consistently outperforms existing methods across diverse settings without relying on reference datasets or replay memory.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无需任务ID预测器的MoE动态专家知识共享。

### 2. 核心内容
该文针对持续学习中MoE的共享参数空间随任务增多成为瓶颈、且完全独立专家需显式任务ID预测器的问题。作者取消任务间共享空间与任务ID预测器，通过开放集学习实现专家间通信，使知识能像人类协作一样动态共享。该方法缓解了灾难性遗忘并简化了路由设计，为无需人工定义语义的专家知识整合提供了可迁移范式。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=ZPJbTXMYft](https://openreview.net/forum?id=ZPJbTXMYft)
