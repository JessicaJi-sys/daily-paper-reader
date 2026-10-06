---
title: Test-Time Adaptation without Source Data for Out-of-Domain Bioactivity Prediction
title_zh: 无源数据的测试时自适应用于分布外生物活性预测
authors: "Yiming Yang, Zhiyuan Zhou, Yueming Yin, Hoi-Yeung Li, Adams Wai-Kin Kong"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=0R6HLWvWYk"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 药物活性预测的分布外泛化
tldr: 该文针对蛋白质-配体生物活性预测中的分布外泛化难题，指出现有深度模型依赖源数据，在隐私或知识产权受限场景下难以适用。作者提出一种不确定性加权的测试时一致性策略，在无源数据条件下让模型适应分布外分布。实验表明该方法能有效提升跨分布生物活性预测的稳健性，为药物发现中的域偏移问题提供了更现实的解决方案。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有生物活性预测模型依赖源数据，在数据受限场景下难以应对分布外泛化。
method: 提出不确定性加权的测试时一致性策略，在无源数据条件下自适应调整模型。
result: 实验显示该方法在分布外生物活性预测任务上提升了泛化性能。
conclusion: 为药物发现中无源数据的域偏移适应提供了现实可行的新范式。
---

## Abstract
Accurate prediction of protein-ligand bioactivity is a cornerstone of modern drug discovery, yet current deep learning methods often struggle with out-of-domain (OOD) generalization. The existing methods rely on access to source data, making them impractical in scenarios where data cannot be accessed due to confidentiality, privacy concerns or intellectual property restrictions. In this paper, we provide the first exploration of a more realistic setting for bioactivity prediction, where models are expected to adapt to out-of-domain distributions without access to source data. Motivated by the critical role of binding-relevant interactions in determining ligand-protein bioactivity, we introduce an uncertainty-weighted consistency strategy, in which original samples with high confidence guide their augmented counterparts by minimizing feature distance. This encourages the model to focus on informative interaction regions while suppressing reliance on spurious or non-causal substructures. To further enhance representation discriminability and prevent feature collapse, we integrate a contrastive optimization objective that pulls together augmented views of the same complex and pushes away views from different complexes. Together, these two components enable the learning of invariant, bioactivity-aware representations, allowing robust adaptation under distribution shifts. Extensive experiments across DTIGN, SIU 0.6, and DrugOOD demonstrate that our framework consistently outperforms state-of-the-art baselines under scaffold, protein, and assay based OOD settings. Especially on the eight subsets of DTIGN, it improves Pearson’s $R$ by 8.2\% and Kendall’s Tau $\tau$ by 5.8\% on average over the best baseline, underscoring its effectiveness as a source data-absent solution for OOD bioactivity prediction.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
药物活性预测的分布外泛化。

### 2. 核心内容
该文针对蛋白质-配体生物活性预测中的分布外泛化难题，指出现有深度模型依赖源数据，在隐私或知识产权受限场景下难以适用。作者提出一种不确定性加权的测试时一致性策略，在无源数据条件下让模型适应分布外分布。实验表明该方法能有效提升跨分布生物活性预测的稳健性，为药物发现中的域偏移问题提供了更现实的解决方案。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=0R6HLWvWYk](https://openreview.net/forum?id=0R6HLWvWYk)
