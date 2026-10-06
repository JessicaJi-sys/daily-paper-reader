---
title: "DirMoE: Dirichlet-Routed Mixture of Experts"
title_zh: DirMoE：狄利克雷路由的专家混合模型
authors: "Amirhossein Vahidi, Hesam Asadollahzadeh, Navid Akhavan Attar, Marie Moullet, Kevin Ly, Xingyi Yang, Mohammad Lotfollahi"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=a15cDnzr6r"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 可微狄利克雷路由解耦专家选择与贡献分配
tldr: 针对现有专家混合路由依赖不可微的Top-k+Softmax、将专家选择与贡献分配两个决策混为一谈的问题，本文提出狄利克雷路由的MoE即DirMoE。该方法基于狄利克雷变分自编码器，用伯努利组件建模专家选择、用狄利克雷组件分配所选专家的贡献，使整个前向过程完全可微。实验表明解耦的选择与贡献建模提升了MoE的性能与可扩展性。该工作为动态、可微的专家路由提供新范式，可支撑药物对级动态专家路由的设计。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有MoE路由依赖不可微的Top-k+Softmax，混淆了专家选择与贡献分配两个决策，限制性能与扩展性。
method: 提出DirMoE，基于狄利克雷变分自编码器，用伯努利组件选专家、狄利克雷组件分配所选专家的贡献。
result: 实现端到端可微路由并解耦选择与贡献，提升MoE的性能与可扩展性。
conclusion: 为动态、可微的专家路由提供新范式，可支撑药物对级动态专家路由与贡献分配的设计。
---

## Abstract
Mixture-of-Experts (MoE) models have demonstrated exceptional performance in large-scale language models. Existing routers typically rely on non-differentiable Top-$k$+Softmax, limiting their performance and scalability. We argue that two distinct decisions, which experts to activate and how to distribute expert contributions among them, are conflated in standard Top-$k$+Softmax. We introduce Dirichlet-Routed MoE (DirMoE), a novel end-to-end differentiable routing mechanism built on a Dirichlet variational autoencoder framework. This design fundamentally disentangles the core routing problems: expert selection, modeled by a Bernoulli component, and expert contribution among chosen experts, handled by a Dirichlet component. The entire forward pass remains fully differentiable through the use of Gumbel-Sigmoid relaxation for the expert selection and implicit reparameterization for the Dirichlet distribution. Our training objective, a variational ELBO, includes a direct sparsity penalty that precisely controls the number of active experts in expectation, alongside a schedule for key hyperparameters that guides the model from an exploratory to a definitive routing state. Moreover, our DirMoE router matches or exceeds other methods while improving expert specialization.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
可微狄利克雷路由解耦专家选择与贡献分配。

### 2. 核心内容
针对现有专家混合路由依赖不可微的Top-k+Softmax、将专家选择与贡献分配两个决策混为一谈的问题，本文提出狄利克雷路由的MoE即DirMoE。该方法基于狄利克雷变分自编码器，用伯努利组件建模专家选择、用狄利克雷组件分配所选专家的贡献，使整个前向过程完全可微。实验表明解耦的选择与贡献建模提升了MoE的性能与可扩展性。该工作为动态、可微的专家路由提供新范式，可支撑药物对级动态专家路由的设计。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=a15cDnzr6r](https://openreview.net/forum?id=a15cDnzr6r)
