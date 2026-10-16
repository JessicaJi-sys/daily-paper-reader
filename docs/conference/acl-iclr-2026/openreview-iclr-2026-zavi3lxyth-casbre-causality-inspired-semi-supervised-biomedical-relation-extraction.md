---
title: "CaSBRE: Causality-inspired Semi-supervised Biomedical Relation Extraction"
title_zh: CaSBRE：因果启发的半监督生物医学关系抽取
authors: "Sihang Zeng, Jun Wen, Jiangchuan Du, Jingyun Qian, Tianxi Cai, Hao Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=ZAvI3lxYTh"
tags: ["query:ood-inv"]
score: 7.0
evidence: 因果启发解耦虚假相关，泛化到未见生物医学实体
tldr: 论文针对生物医学关系抽取中标注稀缺、模型易过拟合虚假特征-标签相关而难以泛化到未见实体的问题。作者提出因果启发的半监督框架CaSBRE，通过因果机制解耦并缓解虚假相关，在化学-蛋白相互作用等任务上提升对未见生物医学实体的泛化。该工作为在缺乏显式环境标签下识别不变特征、抑制虚假相关提供了可迁移思路，与冷启动DDI的OOD不变学习高度相关。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 生物医学实体多样且标注稀缺，传统监督方法易过拟合虚假相关，难以泛化到未见实体。
method: 提出因果启发的半监督框架CaSBRE，解耦并缓解虚假特征-标签相关以提升对未见实体的关系抽取。
result: 在化学-蛋白相互作用等生物医学关系上缓解虚假相关，改善对未见实体的泛化能力。
conclusion: 为缺少环境标签下解耦不变特征与虚假相关提供可行范式。
---

## Abstract
Biomedical interaction relations, such as chemical-protein interactions (CPIs) and gene-disease associations (GDAs), are crucial for advancing drug discovery and clinical treatments. However, the vast diversity of biomedical entities and the limited availability of labeled data pose significant challenges to accurately modeling these interactions using traditional supervised learning approaches. These methods often overfit to spurious feature-label correlations in the scarce labeled relations, leading to poor generalization to unseen biomedical entities. To overcome these challenges, we introduce CaSBRE, a causality-inspired semi-supervised learning framework designed to disentangle and mitigate the impact of such spurious correlations. CaSBRE includes two core components: (i) Feature Disentanglement, which separates causal from spurious features by identifying and exploiting discrepancies between their correlations in labeled and unlabeled data; and (ii) Do-calculus Interaction Inference, which marginalizes the influence of spurious features on relation predictions. Through extensive experiments on CPI and GDA tasks, we demonstrate that CaSBRE substantially outperforms state-of-the-art methods, particularly in generalizing to previously unseen biomedical entities, thereby providing a robust and scalable solution for biomedical relation extraction.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
因果启发解耦虚假相关，泛化到未见生物医学实体。

### 2. 核心内容
论文针对生物医学关系抽取中标注稀缺、模型易过拟合虚假特征-标签相关而难以泛化到未见实体的问题。作者提出因果启发的半监督框架CaSBRE，通过因果机制解耦并缓解虚假相关，在化学-蛋白相互作用等任务上提升对未见生物医学实体的泛化。该工作为在缺乏显式环境标签下识别不变特征、抑制虚假相关提供了可迁移思路，与冷启动DDI的OOD不变学习高度相关。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=ZAvI3lxYTh](https://openreview.net/forum?id=ZAvI3lxYTh)
