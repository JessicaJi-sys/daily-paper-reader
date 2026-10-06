---
title: "CONCUR: A Framework for Continual Constrained and Unconstrained Routing"
title_zh: CONCUR：面向持续约束与非约束路由的框架
authors: "Peter Baile Chen, Weiyue Li, Dan Roth, Mike Cafarella, Samuel Madden, Jacob Andreas"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=gCUY6QIv8r"
tags: ["query:ddi-moe"]
score: 4.0
evidence: 面向新策略泛化的持续路由框架
tldr: 不同AI任务复杂度各异，需要路由系统将其映射到合适的计算策略，但以往方法依赖单一模型与单一输入表示，新增策略需全量重训且泛化困难。本文提出CONCUR持续路由框架，通过多输入表示提升路由决策质量并支持策略的持续扩展。实验表明该框架在泛化能力与训练开销之间取得更优平衡，为动态策略选择提供了可扩展方案。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 既有路由框架需全量重训且泛化差，单一输入表示难以刻画路由问题的复杂度。
method: 提出CONCUR持续路由框架，融合多种输入表示并支持约束与非约束策略的持续学习。
result: 实验显示其在新增策略场景下具备更好的泛化能力与更低的训练开销。
conclusion: 持续多表示路由为动态策略选择提供了可扩展的通用方案。
---

## Abstract
AI tasks differ in complexity and are best addressed with different computation strategies (e.g., combinations of models and decoding methods). Hence, an effective routing system that maps tasks to the appropriate strategies is crucial.
Most prior methods build the routing framework by training a *single* model across *all* strategies, which demands full retraining whenever new strategies appear and leads to high overhead. Attempts at such continual routing, however, often face difficulties with generalization.
Prior models also typically use a *single* input representation, limiting their ability to capture the full complexity of the routing problem and leading to sub-optimal routing decisions.
To address these gaps, we propose CONCUR, a **con**tinual routing framework that supports both **c**onstrained and **u**nconstrained **r**outing (i.e., routing with or without a budget).
Our *modular* design trains a separate predictor model for each strategy, enabling seamless incorporation of new strategies with low additional training cost.
Our predictors also leverage *multiple* representations of both tasks and computation strategies to better capture overall problem complexity.
Experiments on both in-distribution and out-of-distribution, knowledge- and reasoning-intensive tasks show that our method outperforms the best single strategy and strong existing routing techniques with higher end-to-end accuracy and lower inference cost in both continual and non-continual settings, while also reducing training cost in the continual setting.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向新策略泛化的持续路由框架。

### 2. 核心内容
不同AI任务复杂度各异，需要路由系统将其映射到合适的计算策略，但以往方法依赖单一模型与单一输入表示，新增策略需全量重训且泛化困难。本文提出CONCUR持续路由框架，通过多输入表示提升路由决策质量并支持策略的持续扩展。实验表明该框架在泛化能力与训练开销之间取得更优平衡，为动态策略选择提供了可扩展方案。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=gCUY6QIv8r](https://openreview.net/forum?id=gCUY6QIv8r)
