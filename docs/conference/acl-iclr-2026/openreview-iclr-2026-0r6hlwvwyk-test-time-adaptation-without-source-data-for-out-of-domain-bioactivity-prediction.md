---
title: Test-Time Adaptation without Source Data for Out-of-Domain Bioactivity Prediction
title_zh: 无源数据的测试时自适应用于域外生物活性预测
authors: "Yiming Yang, Zhiyuan Zhou, Yueming Yin, Hoi-Yeung Li, Adams Wai-Kin Kong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=0R6HLWvWYk"
tags: ["query:ood-inv"]
score: 6.0
evidence: 无源数据的生物活性域外泛化
tldr: 针对蛋白质-配体生物活性预测在域外分布下泛化困难、且现有方法依赖源数据的问题，本文首次探索无源数据的测试时自适应设定。作者提出不确定性加权一致性策略，利用结合相关相互作用信息引导模型在目标域自适应。实验表明该方法在无法访问源数据时仍能提升域外预测鲁棒性，为隐私受限场景下的OOD泛化提供了新思路。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有生物活性预测方法在域外分布下泛化差且依赖源数据，隐私受限时难以应用。
method: 提出无源数据的测试时自适应设定，并设计不确定性加权一致性策略引导目标域适配。
result: 实验表明该方法在无法访问源数据时仍能提升域外生物活性预测的鲁棒性。
conclusion: 为隐私受限下的OOD泛化提供了不依赖源数据的新范式。
---

## Abstract
Accurate prediction of protein-ligand bioactivity is a cornerstone of modern drug discovery, yet current deep learning methods often struggle with out-of-domain (OOD) generalization. The existing methods rely on access to source data, making them impractical in scenarios where data cannot be accessed due to confidentiality, privacy concerns or intellectual property restrictions. In this paper, we provide the first exploration of a more realistic setting for bioactivity prediction, where models are expected to adapt to out-of-domain distributions without access to source data. Motivated by the critical role of binding-relevant interactions in determining ligand-protein bioactivity, we introduce an uncertainty-weighted consistency strategy, in which original samples with high confidence guide their augmented counterparts by minimizing feature distance. This encourages the model to focus on informative interaction regions while suppressing reliance on spurious or non-causal substructures. To further enhance representation discriminability and prevent feature collapse, we integrate a contrastive optimization objective that pulls together augmented views of the same complex and pushes away views from different complexes. Together, these two components enable the learning of invariant, bioactivity-aware representations, allowing robust adaptation under distribution shifts. Extensive experiments across DTIGN, SIU 0.6, and DrugOOD demonstrate that our framework consistently outperforms state-of-the-art baselines under scaffold, protein, and assay based OOD settings. Especially on the eight subsets of DTIGN, it improves Pearson’s $R$ by 8.2\% and Kendall’s Tau $\tau$ by 5.8\% on average over the best baseline, underscoring its effectiveness as a source data-absent solution for OOD bioactivity prediction.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无源数据的生物活性域外泛化。

### 2. 核心内容
针对蛋白质-配体生物活性预测在域外分布下泛化困难、且现有方法依赖源数据的问题，本文首次探索无源数据的测试时自适应设定。作者提出不确定性加权一致性策略，利用结合相关相互作用信息引导模型在目标域自适应。实验表明该方法在无法访问源数据时仍能提升域外预测鲁棒性，为隐私受限场景下的OOD泛化提供了新思路。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=0R6HLWvWYk](https://openreview.net/forum?id=0R6HLWvWYk)
