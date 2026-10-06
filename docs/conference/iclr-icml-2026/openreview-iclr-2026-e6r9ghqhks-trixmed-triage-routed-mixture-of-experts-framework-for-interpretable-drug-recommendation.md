---
title: "TRIXMED: Triage-Routed Mixture of Experts Framework for Interpretable Drug Recommendation"
title_zh: TRIXMED：面向可解释药物推荐的分诊路由混合专家框架
authors: "Rongyu Lin, Weiwei Chen, Shichao Pei, Shengzhi LI, Mengyuan Shi"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=E6r9GHQhkS"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 面向药物推荐的混合专家路由框架
tldr: 该文针对药物推荐中患者异质性处理不足与模型黑箱问题，提出TRIXMED框架，将混合专家架构与模拟临床分诊的路由机制相结合。模型通过分诊式路由为不同患者分配专家，实现个性化药物推荐并提升可解释性。该工作表明面向药物任务的专家路由有助于应对个体差异，为药物对建模中的动态专家分配提供了可借鉴思路。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 药物推荐中患者异质性未被充分处理，且模型黑箱削弱临床信任。
method: 提出分诊路由的混合专家框架，用模拟临床分诊的路由实现个性化推荐。
result: 该框架在个性化药物推荐上兼顾了异质性建模与可解释性。
conclusion: 为药物相关任务中的动态专家路由与可解释性提供了可行方案。
---

## Abstract
Drug recommendation is a critical task in intelligent healthcare systems that significantly impacts patient outcomes. While large language models (LLMs) have advanced the field through sophisticated semantic understanding, current approaches face two fundamental challenges: (1) they fail to adequately address patient heterogeneity, treating diverse populations with a one-size-fits-all model; (2) their black-box nature undermines clinical trust and adoption. We introduce TRIXMED (Triage-Routed Interpretable eXpert Medicine), a novel framework that integrates Mixture of Experts (MoE) architecture with routing mechanisms that mimic clinical triage processes for personalized drug recommendation. TRIXMED addresses patient heterogeneity by introducing specialized experts that handle distinct patient subgroups, while ensuring interpretability through a clustering-based routing strategy that automatically directs patients to the most appropriate expert based on their clinical profile. Our approach employs a unique warm-up training phase followed by feature extraction and patient stratification, enabling transparent expert routing based on patient characteristics. Extensive experiments on the MIMIC-III datasets show that TRIXMED surpasses the SOTA model, achieving relative improvements of 27.4\% in Jaccard index, and 15.61\% in F1-score, respectively. TRIXMED represents a significant advancement in bridging the gap between AI-powered recommendations and clinical practice through its combination of heterogeneity handling and transparent decision-making.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向药物推荐的混合专家路由框架。

### 2. 核心内容
该文针对药物推荐中患者异质性处理不足与模型黑箱问题，提出TRIXMED框架，将混合专家架构与模拟临床分诊的路由机制相结合。模型通过分诊式路由为不同患者分配专家，实现个性化药物推荐并提升可解释性。该工作表明面向药物任务的专家路由有助于应对个体差异，为药物对建模中的动态专家分配提供了可借鉴思路。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=E6r9GHQhkS](https://openreview.net/forum?id=E6r9GHQhkS)
