---
title: Generalization and Scaling Laws for Mixture-of-ExpertsTransformers
title_zh: 混合专家 Transformer 的泛化与缩放律
authors: Mansour MAYAKI
date: 2026-04-30
pdf: "https://openreview.net/pdf/68e55a6eecf771ba9a666250a1c294a364d1c41e.pdf"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 混合专家架构的泛化与缩放理论
tldr: 如何从理论上理解 MoE 的泛化与缩放行为、厘清每输入激活容量与路由组合开销的关系尚不清楚。本文通过固定路由模式并跨模式做并集界，推导依赖激活参数预算与路由开销的覆盖数泛化界，并给出构造性近似定理。结果显示一旦恰当计入激活参数，MoE 的近似与估计权衡与稠密网络一致。其贡献在于为 MoE 的容量、路由与泛化关系提供理论刻画，指导架构设计。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 需要从理论上理解 MoE 的泛化与缩放行为，厘清每输入激活容量与路由组合开销之间的关系。
method: 通过固定路由模式并跨模式做并集界，推导依赖激活参数预算与路由开销的覆盖数泛化界，并给出近似定理。
result: 结果显示一旦恰当计入激活参数，MoE 的近似与估计权衡与稠密网络一致，路由带来额外开销。
conclusion: 为 MoE 的容量、路由与泛化关系提供理论刻画，可指导 MoE 架构设计。
---

## Abstract
We develop a theory of generalization and scaling for Mixture-of-Experts (MoE) Transformers that cleanly separates active per-input capacity from routing combinatorics. By conditioning on fixed routing patterns and union-bounding across them, we derive a sup-norm covering-number bound whose metric entropy scales with the active parameter budget and incurs a MoE-specific routing overhead. Combined with a standard ERM analysis for squared loss, this yields a generalization bound under a $d$-dimensional manifold data model and $C^\beta$ targets, showing that approximation and estimation trade off as in dense networks once active parameters are accounted for appropriately. We further prove a constructive approximation theorem for MoE architectures, showing that, under the approximation construction, error can decrease either by scaling active capacity or by increasing the number of experts, depending on the
dominant bottleneck. From these results we derive neural scaling laws for model size, data size, and compute-optimal tradeoffs. Overall, our results provide a transparent statistical reference point for reasoning about MoE scaling, clarifying which behaviors are certified by worst-case theory and which must arise from data-dependent routing structure or optimization dynamics.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
混合专家架构的泛化与缩放理论。

### 2. 核心内容
如何从理论上理解 MoE 的泛化与缩放行为、厘清每输入激活容量与路由组合开销的关系尚不清楚。本文通过固定路由模式并跨模式做并集界，推导依赖激活参数预算与路由开销的覆盖数泛化界，并给出构造性近似定理。结果显示一旦恰当计入激活参数，MoE 的近似与估计权衡与稠密网络一致。其贡献在于为 MoE 的容量、路由与泛化关系提供理论刻画，指导架构设计。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=WxmL5UjtNm](https://openreview.net/forum?id=WxmL5UjtNm)
