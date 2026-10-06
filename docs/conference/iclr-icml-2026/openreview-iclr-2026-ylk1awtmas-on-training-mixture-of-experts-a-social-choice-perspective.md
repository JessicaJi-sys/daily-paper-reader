---
title: "On Training Mixture-of-Experts: A Social Choice Perspective"
title_zh: 从社会选择视角看混合专家的训练
authors: "Jingyong Ye, Yao Zhang, Jintao Chen, Zihan Zhou, Xin Liu, Mali Zhu, Yang Zhou, Ruoming Jin, Lemao Liu, Dejing Dou"
date: 2025-09-20
pdf: "https://openreview.net/pdf?id=YLk1awtmAS"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 在DomainBed分布外基准上评估专家专门化的MoE训练
tldr: 针对MoE训练中专家专门化与负载均衡难以兼顾的困境，本文从社会选择理论视角将其归因于阿罗不可能定理，并提出受调控的混合专家（RMoE）。该方法包含分阶段负载均衡课程与有状态专家加权融合。实验在GLUE和DomainBed上显著优于标准MoE与动态路由基线，并展现大规模推理任务的扩展性，为分布外泛化下的MoE训练提供新视角。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: MoE训练在专家专门化与负载均衡之间存在困境。
method: 提出RMoE，用分阶段课程和有状态融合进行专家加权。
result: 在GLUE和DomainBed上超越标准MoE与动态路由基线。
conclusion: 以社会选择视角为MoE专门化训练提供新方案。
---

## Abstract
Mixture-of-Experts (MoE) training faces a dilemma between expert specialization and balanced computation. We recast this problem through the lens of social choice theory, attributing training difficulties to Arrow's Impossibility Theorem. Inspired by this, we propose Regulated Mixture-of-Experts (RMoE), comprising a phased curriculum for load-balancing and stateful fusion for expert weighting. Experiments on GLUE and DomainBed show RMoE significantly outperforms standard MoE and dynamic routing baselines. Furthermore, RMoE demonstrates strong scalability on large-scale reasoning tasks with Qwen3 and Mixtral architectures. Our code is available at https://anonymous.4open.science/r/R-MoE-E3DC.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
在DomainBed分布外基准上评估专家专门化的MoE训练。

### 2. 核心内容
针对MoE训练中专家专门化与负载均衡难以兼顾的困境，本文从社会选择理论视角将其归因于阿罗不可能定理，并提出受调控的混合专家（RMoE）。该方法包含分阶段负载均衡课程与有状态专家加权融合。实验在GLUE和DomainBed上显著优于标准MoE与动态路由基线，并展现大规模推理任务的扩展性，为分布外泛化下的MoE训练提供新视角。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=YLk1awtmAS](https://openreview.net/forum?id=YLk1awtmAS)
