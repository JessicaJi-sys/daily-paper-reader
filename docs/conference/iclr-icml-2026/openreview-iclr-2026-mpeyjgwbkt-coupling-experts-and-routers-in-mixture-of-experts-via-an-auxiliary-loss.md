---
title: Coupling Experts and Routers in Mixture-of-Experts via an Auxiliary Loss
title_zh: 通过辅助损失耦合混合专家中的专家与路由器
authors: "Ang Lv, Jin Ma, Yiyuan Ma, Siyuan Qiao"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=MpeyjgWbKt"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 辅助损失将路由器决策与专家能力耦合
tldr: 针对混合专家模型缺乏显式约束使路由器决策与专家能力对齐的问题，本文提出专家-路由器耦合损失（ERC）。该方法将每个专家的路由器嵌入视为其分配token的代理token，并施加两项激活约束以强化专家专门化。该轻量辅助损失提升了MoE性能，为专家专门化与路由对齐提供了通用机制。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: MoE缺乏显式约束使路由器决策与专家能力对齐。
method: 提出ERC损失，用代理token和激活约束耦合路由器与专家。
result: 轻量辅助损失有效提升MoE专门化与整体性能。
conclusion: 为专家专门化与路由一致性提供通用训练机制。
---

## Abstract
Mixture-of-Experts (MoE) models lack explicit constraints to ensure the router's decisions align well with the experts' capabilities, which ultimately limits model performance. To address this, we propose expert-router coupling (ERC) loss, a lightweight auxiliary loss that tightly couples the router's decisions with expert capabilities. Our approach treats each expert's router embedding as a proxy token for the tokens assigned to that expert, and feeds perturbed router embeddings through the experts to obtain intermediate activations. The ERC loss enforces two constraints on these activations: (1) Each expert must exhibit higher activation for its own proxy token than for the proxy tokens of any other expert. (2) Each proxy token must elicit stronger activation from its corresponding expert than from any other expert. These constraints jointly ensure that each router embedding faithfully represents its corresponding expert's capability, while each expert specializes in processing the tokens actually routed to it. The ERC loss is computationally efficient, operating only on $n^2$ activations, where $n$ is the number of experts. This represents a fixed cost independent of batch size, unlike prior coupling methods that scale with the number of tokens (often millions per batch). Through pre-training MoE-LLMs ranging from 3B to 15B parameters and extensive analysis on trillions of tokens, we demonstrate the effectiveness of the ERC loss. Moreover, the ERC loss offers flexible control and quantitative tracking of expert specialization levels during training, providing valuable insights into MoEs.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
辅助损失将路由器决策与专家能力耦合。

### 2. 核心内容
针对混合专家模型缺乏显式约束使路由器决策与专家能力对齐的问题，本文提出专家-路由器耦合损失（ERC）。该方法将每个专家的路由器嵌入视为其分配token的代理token，并施加两项激活约束以强化专家专门化。该轻量辅助损失提升了MoE性能，为专家专门化与路由对齐提供了通用机制。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=MpeyjgWbKt](https://openreview.net/forum?id=MpeyjgWbKt)
