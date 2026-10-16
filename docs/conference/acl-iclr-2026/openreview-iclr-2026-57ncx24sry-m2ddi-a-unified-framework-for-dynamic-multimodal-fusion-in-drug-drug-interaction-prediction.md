---
title: "M$^2$DDI: A Unified Framework for Dynamic Multimodal Fusion in Drug-Drug Interaction Prediction"
title_zh: M2DDI：药物相互作用预测中动态多模态融合的统一框架
authors: "Runqing Xu, Siyi Liu, Yongqi Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=57ncx24sRy"
tags: ["query:ood-inv"]
score: 8.0
evidence: 混合专家多模态融合用于药物相互作用预测
tldr: 针对现有计算方法难以联合建模分子结构、药理功能与网络关系等异质机制的问题，本文提出M2DDI统一框架，采用混合专家架构为每种药理模态配备专门专家，并通过先验增强的双路径门控策略为每个药物对自适应选择相关专家。该设计实现了动态多模态融合，更贴合DDI的异质机制。实验表明其在药物相互作用预测上优于既有方法，为多模态与专家融合的DDI多分类预测提供了直接参考。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有DDI计算方法难以联合建模分子结构、药理功能与网络关系等异质机制。
method: 提出M2DDI，用混合专家架构配以先验增强双路径门控，为每个药物对自适应融合多模态。
result: 实验表明该框架在DDI预测上优于现有方法，实现动态多模态融合。
conclusion: 为药物相互作用的多模态融合与专家门控建模提供了统一且有效的方案。
---

## Abstract
Drug-drug interaction (DDI) prediction is critical for ensuring patient safety and optimizing therapeutic outcomes. Existing computational approaches are limited by their inability to jointly model the heterogeneous mechanisms underlying DDIs, which span molecular structure, pharmacodynamic function, and network-mediated relations. To address this limitation, we introduce \texttt{M$^{2}$DDI}, a unified framework for dynamic multimodal fusion in DDI prediction. \texttt{M$^{2}$DDI} utilizes a Mixture-of-Experts architecture, with each expert dedicated to a distinct pharmacological modality. A novel prior-enhanced dual-path gating strategy adaptively selects relevant experts for each drug pair by integrating mechanism-matched feature queries and ATC-based biomedical priors, thereby aligning expert selection with underlying pharmacological mechanisms and addressing the challenge of data incompleteness. Empirical evaluation on benchmark datasets demonstrates that \texttt{M$^{2}$DDI} achieves state-of-the-art performance, particularly in new drug scenarios. Additional robustness experiments show that \texttt{M$^{2}$DDI} maintains high predictive accuracy even when modality-specific information is partially missing, outperforming existing methods under similar conditions. Analysis of expert selection patterns further confirms alignment with established pharmacological mechanisms. These results establish \texttt{M$^{2}$DDI} as an effective and mechanism-aware solution for comprehensive DDI prediction. The code are available at \url{https://anonymous.4open.science/r/M2DDI-AECB}

---

## 论文详细总结（自动生成）

### 1. 检索相关性
混合专家多模态融合用于药物相互作用预测。

### 2. 核心内容
针对现有计算方法难以联合建模分子结构、药理功能与网络关系等异质机制的问题，本文提出M2DDI统一框架，采用混合专家架构为每种药理模态配备专门专家，并通过先验增强的双路径门控策略为每个药物对自适应选择相关专家。该设计实现了动态多模态融合，更贴合DDI的异质机制。实验表明其在药物相互作用预测上优于既有方法，为多模态与专家融合的DDI多分类预测提供了直接参考。

### 3. 对应检索需求
methods for multi class prediction of unseen drug pairs using invariant learning and mixture of experts。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=57ncx24sRy](https://openreview.net/forum?id=57ncx24sRy)
