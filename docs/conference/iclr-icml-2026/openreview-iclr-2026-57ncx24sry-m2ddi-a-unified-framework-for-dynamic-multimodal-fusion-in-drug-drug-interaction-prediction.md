---
title: "M$^2$DDI: A Unified Framework for Dynamic Multimodal Fusion in Drug-Drug Interaction Prediction"
title_zh: M2DDI：药物相互作用预测中动态多模态融合的统一框架
authors: "Runqing Xu, Siyi Liu, Yongqi Zhang"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=57ncx24sRy"
tags: ["query:ddi-moe"]
score: 9.0
evidence: 用双路径门控为每个药物对自适应选择专家的DDI预测MoE框架
tldr: 药物相互作用预测对用药安全至关重要，但现有方法难以联合建模分子结构、药效功能与网络关系等异质机制。本文提出统一框架M2DDI，采用混合专家架构，每个专家对应一种药理模态，并用先验增强的双路径门控策略为每个药物对自适应选择相关专家。该设计实现了面向药物对级的动态多模态融合，能按实例整合不等贡献的异质知识来源，为冷启动与药物级分布外泛化下的动态专家路由提供了直接参考。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 药物相互作用预测对患者安全与疗效优化至关重要，但现有方法无法联合建模分子结构、药效功能与网络关系等异质机制，限制了预测能力。
method: 论文提出统一框架M2DDI，采用混合专家架构使每个专家负责一种药理模态，并设计先验增强的双路径门控为每个药物对自适应选择相关专家。
result: 该框架实现了药物对级动态多模态融合，能根据实例整合贡献不均的异质知识，在DDI预测任务上提升了建模异质机制的能力。
conclusion: M2DDI将MoE与药物对级动态路由用于DDI，为冷启动与药物级OOD泛化下分布依赖的多源知识效用整合提供了直接范式。
---

## Abstract
Drug-drug interaction (DDI) prediction is critical for ensuring patient safety and optimizing therapeutic outcomes. Existing computational approaches are limited by their inability to jointly model the heterogeneous mechanisms underlying DDIs, which span molecular structure, pharmacodynamic function, and network-mediated relations. To address this limitation, we introduce \texttt{M$^{2}$DDI}, a unified framework for dynamic multimodal fusion in DDI prediction. \texttt{M$^{2}$DDI} utilizes a Mixture-of-Experts architecture, with each expert dedicated to a distinct pharmacological modality. A novel prior-enhanced dual-path gating strategy adaptively selects relevant experts for each drug pair by integrating mechanism-matched feature queries and ATC-based biomedical priors, thereby aligning expert selection with underlying pharmacological mechanisms and addressing the challenge of data incompleteness. Empirical evaluation on benchmark datasets demonstrates that \texttt{M$^{2}$DDI} achieves state-of-the-art performance, particularly in new drug scenarios. Additional robustness experiments show that \texttt{M$^{2}$DDI} maintains high predictive accuracy even when modality-specific information is partially missing, outperforming existing methods under similar conditions. Analysis of expert selection patterns further confirms alignment with established pharmacological mechanisms. These results establish \texttt{M$^{2}$DDI} as an effective and mechanism-aware solution for comprehensive DDI prediction. The code are available at \url{https://anonymous.4open.science/r/M2DDI-AECB}

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用双路径门控为每个药物对自适应选择专家的DDI预测MoE框架。

### 2. 核心内容
药物相互作用预测对用药安全至关重要，但现有方法难以联合建模分子结构、药效功能与网络关系等异质机制。本文提出统一框架M2DDI，采用混合专家架构，每个专家对应一种药理模态，并用先验增强的双路径门控策略为每个药物对自适应选择相关专家。该设计实现了面向药物对级的动态多模态融合，能按实例整合不等贡献的异质知识来源，为冷启动与药物级分布外泛化下的动态专家路由提供了直接参考。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=57ncx24sRy](https://openreview.net/forum?id=57ncx24sRy)
