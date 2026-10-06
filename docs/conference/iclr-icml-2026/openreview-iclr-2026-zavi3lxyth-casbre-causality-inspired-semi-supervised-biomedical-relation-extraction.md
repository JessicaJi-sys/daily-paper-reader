---
title: "CaSBRE: Causality-inspired Semi-supervised Biomedical Relation Extraction"
title_zh: CaSBRE：因果启发的半监督生物医学关系抽取
authors: "Sihang Zeng, Jun Wen, Jiangchuan Du, Jingyun Qian, Tianxi Cai, Hao Wang"
date: 2025-09-20
pdf: "https://openreview.net/pdf?id=ZAvI3lxYTh"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 因果启发的虚假相关解耦以泛化到未见实体
tldr: 针对生物医学关系抽取中实体多样、标注稀缺，传统监督方法易过拟合虚假相关而难以泛化到未见实体的问题，本文提出因果启发的半监督框架CaSBRE。该方法通过因果视角解耦并抑制虚假的特征-标签相关性，从而学习更稳定的表征。在化学-蛋白交互与基因-疾病关联等任务上，模型对未见生物医学实体的泛化能力得到提升。该工作表明因果解耦有助于分布外泛化，对不变表征学习具有借鉴意义。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 生物医学实体多样且标注稀缺，传统监督方法易过拟合虚假特征-标签相关，难以泛化到未见实体。
method: 提出因果启发的半监督框架CaSBRE，通过因果解耦与抑制虚假相关性学习更稳定的关系表征。
result: 在化学-蛋白交互和基因-疾病关联等任务上缓解过拟合，提升对未见生物医学实体的泛化能力。
conclusion: 表明因果解耦可增强关系抽取的分布外泛化，为不变表征学习提供可迁移的思路。
---

## Abstract
Biomedical interaction relations, such as chemical-protein interactions (CPIs) and gene-disease associations (GDAs), are crucial for advancing drug discovery and clinical treatments. However, the vast diversity of biomedical entities and the limited availability of labeled data pose significant challenges to accurately modeling these interactions using traditional supervised learning approaches. These methods often overfit to spurious feature-label correlations in the scarce labeled relations, leading to poor generalization to unseen biomedical entities. To overcome these challenges, we introduce CaSBRE, a causality-inspired semi-supervised learning framework designed to disentangle and mitigate the impact of such spurious correlations. CaSBRE includes two core components: (i) Feature Disentanglement, which separates causal from spurious features by identifying and exploiting discrepancies between their correlations in labeled and unlabeled data; and (ii) Do-calculus Interaction Inference, which marginalizes the influence of spurious features on relation predictions. Through extensive experiments on CPI and GDA tasks, we demonstrate that CaSBRE substantially outperforms state-of-the-art methods, particularly in generalizing to previously unseen biomedical entities, thereby providing a robust and scalable solution for biomedical relation extraction.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
因果启发的虚假相关解耦以泛化到未见实体。

### 2. 核心内容
针对生物医学关系抽取中实体多样、标注稀缺，传统监督方法易过拟合虚假相关而难以泛化到未见实体的问题，本文提出因果启发的半监督框架CaSBRE。该方法通过因果视角解耦并抑制虚假的特征-标签相关性，从而学习更稳定的表征。在化学-蛋白交互与基因-疾病关联等任务上，模型对未见生物医学实体的泛化能力得到提升。该工作表明因果解耦有助于分布外泛化，对不变表征学习具有借鉴意义。

### 3. 对应检索需求
invariant representation learning for stable drug generalization。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=ZAvI3lxYTh](https://openreview.net/forum?id=ZAvI3lxYTh)
