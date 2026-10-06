---
title: "Learning Once, Routing Right: Information-Theoretic Gating for Online Continual Mixture-of-Experts"
title_zh: 一次学习，正确路由：面向在线持续混合专家的信息论门控
authors: "Xuncheng Liu, Weizhan Zhang, Tieliang Gong"
date: 2025-09-16
pdf: "https://openreview.net/pdf?id=UbJjdbDPdr"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 面向在线持续MoE的互信息门控设计
tldr: 该文指出MoE门控机制缺乏从持续学习视角出发的原则性设计，因而研究门控策略对在线持续学习中可达最小超额风险的影响。作者揭示最小超额风险与专家分配同标签之间互信息的新联系，并据此提出两种基于互信息的门控方法。该工作为动态专家路由提供了理论支撑与设计准则，对分布依赖下的专家选择具有重要借鉴意义。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: MoE门控机制缺乏从持续学习视角出发的原则性设计。
method: 研究门控策略对最小超额风险的影响，提出两种基于互信息的门控方法。
result: 揭示最小超额风险与专家分配和标签间互信息的新联系。
conclusion: 为动态专家路由提供理论支撑与可迁移的门控设计准则。
---

## Abstract
Continual Learning (CL) requires models to learn from sequential data streams while retaining previously acquired knowledge. While Mixture-of-Experts (MoE) models offer a promising solution through dynamic expert selection, a critical gap remains: their gating mechanisms lack principled design from a continual learning perspective. To bridge this gap, we investigate the impact of gating strategies on the achievable Minimum Excess Risk (MER) under the online CL setting, where data can be seen only once. Our key theoretical contribution reveals a novel connection between the MER and the mutual information between expert assignments and labels/outputs. Based on this foundation, we propose two innovative mutual information-based loss functions for both fully labeled and label-free settings. Furthermore, to ensure computational efficiency, we introduce a lightweight, matrix-based mutual information estimator with rigorous joint entropy formulation. Extensive experiments on MNIST, Fashion-MNIST, KMNIST, and EMNIST demonstrate our approach's superiority, achieving up to 12.3\% lower overall error and 3.9\% reduced forgetting with statistical significance.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向在线持续MoE的互信息门控设计。

### 2. 核心内容
该文指出MoE门控机制缺乏从持续学习视角出发的原则性设计，因而研究门控策略对在线持续学习中可达最小超额风险的影响。作者揭示最小超额风险与专家分配同标签之间互信息的新联系，并据此提出两种基于互信息的门控方法。该工作为动态专家路由提供了理论支撑与设计准则，对分布依赖下的专家选择具有重要借鉴意义。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=UbJjdbDPdr](https://openreview.net/forum?id=UbJjdbDPdr)
