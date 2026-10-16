---
title: "What We Don't C: Manifold Disentanglement for Structured Discovery"
title_zh: "What We Don't C：面向结构化发现的流形解耦"
authors: "Brian Rogers, Micah Bowles, Chris J. Lintott, Steve Croft, Oliver N. F. King, James Kostas Ray"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=F2USOqa0La"
tags: ["query:ood-inv"]
score: 6.0
evidence: 流形解耦并去除条件化信息
tldr: "针对高维数据中难以访问与解析学习表示所包含信息的问题，本文提出基于潜流匹配的方法What We Don't C，通过显式去除条件引导所包含的信息来解耦潜子空间，从而获得有意义的残差表示，使尚未被条件捕获的变化因子更易获取。作者从理论上说明流路径中的引导必然压制引导变量的信息。实验表明该方法是一种简单而强大的表示分析、控制与再利用机制，可为不变与变化特征的解耦提供思路。"
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 高维数据中学习表示所携带的信息难以访问，限制了标注、发现与数据筛选。
method: 提出基于潜流匹配的解耦方法，通过去除条件引导所含信息得到有意义的残差潜表示。
result: 实验表明该机制能有效暴露未被条件捕获的变化因子，实现表示的分析与控制。
conclusion: 为潜空间解耦与表示再利用提供了简单而通用的工具，可迁移至不变特征分离。
---

## Abstract
Accessing information in learned representations is critical for annotation, discovery, and data filtering in disciplines where high-dimensional datasets are common. We introduce What We Don't C, a novel approach based on latent flow matching that disentangles latent subspaces by explicitly removing information included in conditional guidance resulting in meaningful residual representations. This allows factors of variation which have not already been captured in conditioning to become more readily available. We show how guidance in the flow path necessarily represses the information from the guiding, conditioning variables. Our results highlight this approach as a simple yet powerful mechanism for analyzing, controlling, and repurposing latent representations, providing a pathway toward using generative models to explore what we don't capture, consider, or catalog.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
流形解耦并去除条件化信息。

### 2. 核心内容
针对高维数据中难以访问与解析学习表示所包含信息的问题，本文提出基于潜流匹配的方法What We Don't C，通过显式去除条件引导所包含的信息来解耦潜子空间，从而获得有意义的残差表示，使尚未被条件捕获的变化因子更易获取。作者从理论上说明流路径中的引导必然压制引导变量的信息。实验表明该方法是一种简单而强大的表示分析、控制与再利用机制，可为不变与变化特征的解耦提供思路。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=F2USOqa0La](https://openreview.net/forum?id=F2USOqa0La)
