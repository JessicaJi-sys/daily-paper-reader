---
title: "I2Mole: Interaction-aware Invariant Molecular Learning For Generalizable Property Prediction"
title_zh: I2Mole：面向可泛化性质预测的交互感知不变分子学习
authors: "Wenjie Du, Jiahui Zhang, Xuqiang Li, Sihan Wang, Zhengyang Zhou, hongxin xiang, Jun Xia, Ye Wei, Yang Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=IqwF00TCmf"
tags: ["query:ood-inv"]
score: 9.0
evidence: 面向可泛化药物相互作用预测的交互感知不变分子学习
tldr: 本文针对药物相互作用预测中分子结构复杂、相互作用多样导致泛化差的问题，指出现有模型忽视分子对建模。作者提出I2Mole交互感知不变分子学习框架，识别核心不变子结构作为推理依据。方法同时提升预测准确性与可解释性，对冷启动DDI与不变表示学习高度契合，可直接启发unseen药物对场景。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 药物相互作用预测受分子结构复杂与相互作用多样影响，泛化性差，且现有模型忽视分子对建模。
method: 提出I2Mole交互感知不变分子学习框架，建模分子对并识别核心不变子结构作为推理依据。
result: 方法在性质与相互作用预测上提升准确性，并增强可解释性与泛化能力。
conclusion: 该工作将不变学习引入分子对建模，为冷启动DDI等可泛化预测提供了有效范式。
---

## Abstract
Molecular interactions are a common phenomenon in physical chemistry field, which could produce unexpected biochemical properties harmful to humans, such as drug-drug interactions. Machine learning has the potential to deliver rapid and accurate predictions. However, the complexity of molecular structures and the diversity of molecular interactions could undermine model prediction accuracy and hinder generalizability. In this context, identifying core invariant substructures (\textit{i.e.}, rationales) has become essential for enhancing interpretability and generalization. Despite notable efforts, existing models often neglect the molecular pairs’ modeling, leading to insufficient capture of interaction relationships. To address these limitations, we propose a novel framework, \textbf{I}nteraction-aware \textbf{I}nvariant \textbf{Mole}cular learning (I2Mole), for generalizable property prediction. I2Mole meticulously models atomic interactions such as hydrogen bonds by initially establishing indiscriminate connections between intermolecular atoms, which are subsequently refined using an improved graph information bottleneck theory tailored for merged graphs. To further enhance model generalization, we construct an environment codebook by environment subgraph of the merged graph. This approach not only could provide noise source for optimizing mutual information but also preserve the integrity of chemical semantic information. By comprehensively leveraging the information inherent in the merged graph, our model accurately captures core substructures and significantly enhances generalization capabilities. Extensive experimental validation demonstrates the efficacy and generalizability of I2Mole. The implementation code is available.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向可泛化药物相互作用预测的交互感知不变分子学习。

### 2. 核心内容
本文针对药物相互作用预测中分子结构复杂、相互作用多样导致泛化差的问题，指出现有模型忽视分子对建模。作者提出I2Mole交互感知不变分子学习框架，识别核心不变子结构作为推理依据。方法同时提升预测准确性与可解释性，对冷启动DDI与不变表示学习高度契合，可直接启发unseen药物对场景。

### 3. 对应检索需求
research on out of distribution generalization and invariant representation learning for cold start drug drug interaction prediction。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=IqwF00TCmf](https://openreview.net/forum?id=IqwF00TCmf)
