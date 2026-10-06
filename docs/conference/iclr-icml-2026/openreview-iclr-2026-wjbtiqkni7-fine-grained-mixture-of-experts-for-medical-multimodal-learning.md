---
title: Fine-Grained Mixture of Experts for Medical Multimodal Learning
title_zh: 面向医学多模态学习的细粒度专家混合
authors: "Haoqiang Guo, Yaguang Wu, yunxin li, Kaihao Zhang, Baotian Hu, Wei Liu, Qifeng Liu, Wenhan Luo"
date: 2025-09-01
pdf: "https://openreview.net/pdf?id=wJBtiqkNI7"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 细粒度MoE研究：专家粒度与医学领域OOD泛化的关系
tldr: 针对细粒度专家混合在医学等专业领域应用不足、专家粒度对泛化与鲁棒性影响不明的问题，本文在医学多模态VQA中首次系统研究专家粒度。研究发现提高粒度可显著增强分布外泛化与鲁棒性，但会略微降低分布内拟合，并加剧专家共现与功能相似性。作者指出这些共现模式给路由机制带来额外计算压力，同时也蕴含可利用的结构。该工作揭示粒度与泛化的权衡，为医学场景下MoE设计与专家专门化提供指导。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 细粒度MoE在医学等专业领域应用不足，专家粒度对分布外泛化与鲁棒性的影响尚不清楚。
method: 在医学多模态VQA中系统研究专家粒度，分析其与OOD泛化、专家共现及功能相似性的关系。
result: 发现提高粒度显著增强OOD泛化与鲁棒性，但略微降低ID拟合并加剧专家功能相似与共现。
conclusion: 揭示粒度与泛化的权衡，为医学场景MoE设计与路由优化、专家专门化提供指导。
---

## Abstract
Fine-Grained Mixture of Experts is a powerful architecture for scaling large models, yet its application in specialized domains like medicine remains underexplored. In this work, we conduct the first systematic study of expert granularity in a medical multimodal VQA context. Our findings reveal a fundamental trade-off: while increasing granularity significantly enhances out-of-distribution (OOD) generalization and robustness, it slightly degrades in-distribution (ID) fitting and, notably, amplifies expert co-occurrence and functional similarity, indicating stronger collaborative tendencies among experts. We argue that these intensified co-occurrence patterns place additional computational pressure on the routing mechanism, yet also reveal exploitable structure in how experts are jointly activated. To address this, we introduce Adaptive Expert Grouping (AEG), a novel, end-to-end learnable mechanism that leverages these collaborative patterns by dynamically clustering frequently co-activated, functionally related experts. By shifting routing decisions from the individual expert level to the group level, AEG substantially reduces computational overhead and improves model sparsity, while preserving the generalization benefits of the fine-grained architecture. We further observe similar co-occurrence phenomena beyond the medical domain, suggesting that our findings and AEG are broadly applicable. Our work offers a new path towards building more efficient and robust MoE models for specialized domains.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
细粒度MoE研究：专家粒度与医学领域OOD泛化的关系。

### 2. 核心内容
针对细粒度专家混合在医学等专业领域应用不足、专家粒度对泛化与鲁棒性影响不明的问题，本文在医学多模态VQA中首次系统研究专家粒度。研究发现提高粒度可显著增强分布外泛化与鲁棒性，但会略微降低分布内拟合，并加剧专家共现与功能相似性。作者指出这些共现模式给路由机制带来额外计算压力，同时也蕴含可利用的结构。该工作揭示粒度与泛化的权衡，为医学场景下MoE设计与专家专门化提供指导。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=wJBtiqkNI7](https://openreview.net/forum?id=wJBtiqkNI7)
