---
title: "I2Mole: Interaction-aware Invariant Molecular Learning For Generalizable Property Prediction"
title_zh: I2Mole：面向可泛化性质预测的交互感知不变分子学习
authors: "Wenjie Du, Jiahui Zhang, Xuqiang Li, Sihan Wang, Zhengyang Zhou, hongxin xiang, Jun Xia, Ye Wei, Yang Wang"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=IqwF00TCmf"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 面向药物-药物相互作用性质预测的交互感知不变分子学习
tldr: 分子相互作用（如药物-药物相互作用）的结构复杂与多样会削弱模型精度并阻碍泛化。本文提出 I2Mole，显式建模分子对并学习交互感知的不变子结构，以识别核心 rationales。实验表明该框架弥补了以往忽视分子对建模的缺陷，提升了性质预测精度与跨分布泛化。其贡献在于把不变表征学习与分子对交互建模结合，为可解释且稳健的分子性质预测提供新范式。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 分子相互作用的复杂性与多样性会削弱预测精度并阻碍泛化，尤其是药物-药物相互作用等场景，亟需识别核心不变子结构。
method: 提出 I2Mole，显式建模分子对并学习交互感知的不变子结构（rationales），以同时增强可解释性与泛化能力。
result: 通过捕捉分子对间的交互关系，弥补以往忽视分子对建模的不足，提升了性质预测的精度与泛化表现。
conclusion: 表明交互感知的不变分子学习可为 DDI 等分子性质预测提供更稳健、可解释的解决方案。
---

## Abstract
Molecular interactions are a common phenomenon in physical chemistry field, which could produce unexpected biochemical properties harmful to humans, such as drug-drug interactions. Machine learning has the potential to deliver rapid and accurate predictions. However, the complexity of molecular structures and the diversity of molecular interactions could undermine model prediction accuracy and hinder generalizability. In this context, identifying core invariant substructures (\textit{i.e.}, rationales) has become essential for enhancing interpretability and generalization. Despite notable efforts, existing models often neglect the molecular pairs’ modeling, leading to insufficient capture of interaction relationships. To address these limitations, we propose a novel framework, \textbf{I}nteraction-aware \textbf{I}nvariant \textbf{Mole}cular learning (I2Mole), for generalizable property prediction. I2Mole meticulously models atomic interactions such as hydrogen bonds by initially establishing indiscriminate connections between intermolecular atoms, which are subsequently refined using an improved graph information bottleneck theory tailored for merged graphs. To further enhance model generalization, we construct an environment codebook by environment subgraph of the merged graph. This approach not only could provide noise source for optimizing mutual information but also preserve the integrity of chemical semantic information. By comprehensively leveraging the information inherent in the merged graph, our model accurately captures core substructures and significantly enhances generalization capabilities. Extensive experimental validation demonstrates the efficacy and generalizability of I2Mole. The implementation code is available.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向药物-药物相互作用性质预测的交互感知不变分子学习。

### 2. 核心内容
分子相互作用（如药物-药物相互作用）的结构复杂与多样会削弱模型精度并阻碍泛化。本文提出 I2Mole，显式建模分子对并学习交互感知的不变子结构，以识别核心 rationales。实验表明该框架弥补了以往忽视分子对建模的缺陷，提升了性质预测精度与跨分布泛化。其贡献在于把不变表征学习与分子对交互建模结合，为可解释且稳健的分子性质预测提供新范式。

### 3. 对应检索需求
invariant representation learning for stable drug generalization。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=IqwF00TCmf](https://openreview.net/forum?id=IqwF00TCmf)
