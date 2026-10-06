---
title: "Union-of-Experts: Experts in Mixture-of-Experts are Secretly Routers"
title_zh: 专家联盟：混合专家模型中的专家其实是路由器
authors: "Songhao Wu, Ang Lv, Ruobing Xie, Xingwu Sun, Di Wang, Rui Yan, Yankai Lin"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=Ksgiup7ZNZ"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 专家内部能力感知的隐式路由
tldr: 混合专家模型的路由器外置于专家，无法感知专家内部能力，造成路由决策与专家能力脱节。本文发现每个专家参数中存在少量路由神经元，其激活可忠实反映专家能力与输入token的匹配度。这些分布式路由神经元构成隐式且能力感知的路由器，其激活范数暗示专家权重。该发现为无需手工定义专家语义的自动专门化路由提供了新视角。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: MoE的路由器外置于专家，无法感知专家内部能力，限制了模型性能。
method: 揭示专家内部路由神经元的激活构成隐式且能力感知的路由器。
result: 路由神经元激活范数可反映专家与输入的匹配度及专家权重。
conclusion: 为无需手工定义语义的专家专门化与动态路由提供了新机制。
---

## Abstract
Mixture-of-Experts (MoE) is a foundational architecture in modern large language
models (LLMs). However, a structural limitation has been overlooked: the router
is external to the experts, rendering it unaware of their internal capabilities. This
gap between routing decisions and expert capabilities limits model performance.
In this paper, we demonstrate that the activations of a small subset of “routing neurons” within each routed expert’s own parameters can faithfully capture the match
between the expert’s capabilities and input tokens. Collectively, these distributed
routing neurons within each routed experts compose an implicit, capabilities-aware
“router”, where the norm of the routing neurons’ activations suggests its corresponding expert’s weight. A straightforward implementation of this design requires
activating all experts to compute these routing signals, where the unselected experts’ routing neurons are abandoned. To avoid the computational waste from
activating unselected experts, we introduce another novel design: we unify the
routing neurons of all routed experts to form a virtual shared expert, replacing the
standard shared expert in MoE. In this virtual shared expert, activations are not
wasted, as they serve not only for routing but also contribute to the final outputs of
both the shared expert and partial of routed experts. We name this new MoE variant
Union-of-Experts (UoE), drawing an analogy where the routing neuron acts as each
expert’s representative, and the virtual shared expert is their union, enabling the
experts’ autonomous selection and joint statement. We pre-train language models
ranging from 1B to 3B parameters, showing that UoE consistently outperforms
strong MoE baselines with comparable efficiency.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
专家内部能力感知的隐式路由。

### 2. 核心内容
混合专家模型的路由器外置于专家，无法感知专家内部能力，造成路由决策与专家能力脱节。本文发现每个专家参数中存在少量路由神经元，其激活可忠实反映专家能力与输入token的匹配度。这些分布式路由神经元构成隐式且能力感知的路由器，其激活范数暗示专家权重。该发现为无需手工定义专家语义的自动专门化路由提供了新视角。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=Ksgiup7ZNZ](https://openreview.net/forum?id=Ksgiup7ZNZ)
