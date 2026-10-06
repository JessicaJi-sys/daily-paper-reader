---
title: "KG-MoE: Multimodal Knowledge Graph Grounded Mixture of Experts for Fair Visual Question Answering"
title_zh: KG-MoE：面向公平视觉问答的多模态知识图谱驱动混合专家
authors: "Prabhav Sanga, Jaskaran Singh, Tapabrata Chakraborti"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=muJ0EYIXFC"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 知识图谱驱动的专家专门化与动态门控
tldr: 该文针对混合专家模型受相关性驱动路由、缺乏显式知识支撑以及子群差异等问题，提出知识图谱驱动的公平感知MoE框架。方法将结构化知识图谱融入专家专门化，用动态门控在模态专家间路由，并通过对抗去偏降低子群风险。理论上证明知识支撑可降低分布偏移下的超额风险，为无监督语义定义的专家专门化与泛化提供依据。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有MoE路由受相关性驱动、缺乏知识支撑且存在子群差异。
method: 将知识图谱融入专家专门化，用动态门控路由并采用对抗去偏。
result: 理论证明知识支撑可降低分布偏移下的超额风险并改善最差组泛化。
conclusion: 展示了知识驱动专家专门化在分布偏移下提升泛化的潜力。
---

## Abstract
Mixture-of-Experts architectures scale model capacity efficiently but remain limited by correlation-driven routing, lack of explicit knowledge grounding, and subgroup disparities in high-stakes domains. We propose KG-MoE, a knowledge-based and fairness-aware MoE framework that integrates structured knowledge graphs into expert specialization and employs adversarial debiasing to reduce subgroup risk. A dynamic gating network routes inputs across modality-specific experts while retrieved subgraphs constrain reasoning and guide explanation generation. We derive theoretical bounds showing that knowledge grounding reduces excess risk under distribution shift and that fairness regularization improves worst-group generalization. Empirically, KG-MoE achieves state-of-the-art performance across multimodal benchmarks, including dermoscopic, clinical, and histopathology tasks in dermatology, while reducing demographic parity gaps by more than 50% relative to foundation model baselines. Ablation studies confirm the dual benefit of knowledge integration and fairness constraints for both robustness and equity, and qualitative analysis demonstrates knowledge-based explanations aligned with domain reasoning. Our results position KG-MoE as a general paradigm for trustworthy, interpretable, and fair multimodal learning systems.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
知识图谱驱动的专家专门化与动态门控。

### 2. 核心内容
该文针对混合专家模型受相关性驱动路由、缺乏显式知识支撑以及子群差异等问题，提出知识图谱驱动的公平感知MoE框架。方法将结构化知识图谱融入专家专门化，用动态门控在模态专家间路由，并通过对抗去偏降低子群风险。理论上证明知识支撑可降低分布偏移下的超额风险，为无监督语义定义的专家专门化与泛化提供依据。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=muJ0EYIXFC](https://openreview.net/forum?id=muJ0EYIXFC)
