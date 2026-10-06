---
title: Structured Expert Routing with Multi-View Task Priors for Offline Meta-Reinforcement Learning
title_zh: 面向离线元强化学习的多视图任务先验结构化专家路由
authors: "Yisen Zhao, Peixi Peng, Xinyu Hu, Cong Li, Zhan Su, Zhuojian Li"
date: 2026-04-30
pdf: "https://openreview.net/pdf/99ab8acdc12504467d8ad7179d8a917a92317095.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 结构化专家路由泛化到未见任务
tldr: 离线元强化学习需从固定数据泛化到未见任务，但现有序列式与MoE方法依赖隐式或token级路由信号，难以刻画任务级结构。本文提出任务引导路由器TGR，用融合语义描述、行为摘要与隐动态特征的多视图任务表示显式建模任务间关系，按全局任务兼容性而非局部轨迹片段分配专家。实验表明该结构引导路由可实现稳定的专家专门化与有效的跨任务知识迁移。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 现有MoE路由依赖隐式或token级信号，难以刻画任务级结构，限制了对未见任务的泛化。
method: 提出任务引导路由器，用多视图任务表示建模任务间关系，按全局任务兼容性进行结构化专家分配。
result: 在连续控制离线元强化学习实验中实现稳定的专家专门化与有效的跨任务知识迁移。
conclusion: 结构引导的专家路由能提升MoE对未见任务的泛化与知识复用能力。
---

## Abstract
Offline meta-reinforcement learning requires agents to generalize to unseen tasks from fixed datasets, yet existing sequence-based and MoE-based methods rely on implicit or token-level routing signals that fail to capture task-level structure.
We propose the **Task-Guided Router (TGR)**, a structured expert-routing framework that explicitly models inter-task relationships via multi-view task representations that combine semantic descriptors, behavioral summaries, and latent dynamics features.
Using structure-guided routing, TGR assigns experts based on global task compatibility rather than local trajectory fragments, enabling stable specialization and effective knowledge transfer across tasks.Extensive experiments on continuous-control benchmarks demonstrate that TGR consistently outperforms state-of-the-art offline meta-RL methods in few-shot generalization, particularly under sparse data and heterogeneous dynamics.
Our results highlight the importance of task-level priors for robust offline meta-reinforcement learning.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
结构化专家路由泛化到未见任务。

### 2. 核心内容
离线元强化学习需从固定数据泛化到未见任务，但现有序列式与MoE方法依赖隐式或token级路由信号，难以刻画任务级结构。本文提出任务引导路由器TGR，用融合语义描述、行为摘要与隐动态特征的多视图任务表示显式建模任务间关系，按全局任务兼容性而非局部轨迹片段分配专家。实验表明该结构引导路由可实现稳定的专家专门化与有效的跨任务知识迁移。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=5AUITfUstd](https://openreview.net/forum?id=5AUITfUstd)
