---
title: "Beyond Benchmarks: Understanding Mixture-of-Experts Models through Internal Mechanisms"
title_zh: 超越基准：从内部机制理解混合专家模型
authors: "Jiahao Ying, Mingbao Lin, Qianru Sun, Yixin Cao"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=6fmQJGaA8p"
tags: ["query:ddi-moe"]
score: 5.0
evidence: MoE路由与专家级专门化的内部机制分析
tldr: 该文指出当前MoE研究偏重性能而缺乏对内部机制的理解，因而采用内部指标系统分析路由机制与专家行为。通过对多种公开MoE模型的实验，作者发现神经元利用率随模型演进下降，反映更强的泛化能力，且训练呈现动态轨迹。这些发现加深了对专家专门化与路由行为的理解，为设计更优的专家整合策略提供了依据。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有MoE研究偏重性能，缺乏对内部路由与专家行为的理解。
method: 采用内部指标系统分析MoE的路由机制与专家级行为。
result: 发现神经元利用率随模型演进下降，反映更强泛化且训练呈动态轨迹。
conclusion: 深化了对专家专门化与路由行为的理解，助力更优专家整合设计。
---

## Abstract
Mixture-of-Experts (MoE) architectures have emerged as a promising direction, offering efficiency and scalability by activating only a subset of parameters during inference. However, current research remains largely performance-centric, with limited understanding of its internal mechanisms, thereby constraining broader progress. In this work, we use an internal metric to investigate the mechanisms of MoE architecture by explicitly incorporating routing mechanisms and analyzing expert-level behaviors. Through systematic analyses of a wide range of publicly available MoE models, we uncover several findings: (1) neuron utilization decreases as models evolve, reflecting stronger generalization; (2) training exhibits a dynamic trajectory, where benchmark performance alone provides limited signal while MUI reveals deeper insights; (3) task completion emerges from collaborative contributions of multiple experts, with shared experts driving concentration; and (4) activation patterns at the neuron level provide a fine-grained proxy for data diversity. Together, these results demonstrate the potential of MUI as a complementary indicator to benchmark performance, offering new insights into the capacity, dynamics, and specialization of MoE models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
MoE路由与专家级专门化的内部机制分析。

### 2. 核心内容
该文指出当前MoE研究偏重性能而缺乏对内部机制的理解，因而采用内部指标系统分析路由机制与专家行为。通过对多种公开MoE模型的实验，作者发现神经元利用率随模型演进下降，反映更强的泛化能力，且训练呈现动态轨迹。这些发现加深了对专家专门化与路由行为的理解，为设计更优的专家整合策略提供了依据。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=6fmQJGaA8p](https://openreview.net/forum?id=6fmQJGaA8p)
