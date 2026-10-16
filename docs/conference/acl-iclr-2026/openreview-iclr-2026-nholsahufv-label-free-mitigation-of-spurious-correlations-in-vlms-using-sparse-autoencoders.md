---
title: Label-Free Mitigation of Spurious Correlations in VLMs using Sparse Autoencoders
title_zh: 基于稀疏自编码器的视觉语言模型虚假相关无标签缓解
authors: "Bharat Chandra Yalavarthi, Nalini K. Ratha, Venu Govindaraju"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=NHOLsaHuFv"
tags: ["query:ood-inv"]
score: 7.0
evidence: 无标签地解耦并去除虚假相关
tldr: 针对视觉语言模型学到虚假相关而损害下游泛化的问题，本文提出无需额外数据与外部监督的零样本方法DIAL，通过解耦、识别与无标签去除三个步骤过滤表示中受虚假相关过度影响的成分。该方法完全可解释，避免了以往依赖重训练、标注特征或外部语言模型的局限。实验证明其在无监督条件下有效缓解虚假相关，为缺少显式监督时的不变与虚假特征解耦提供了直接可迁移的技术路线。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 视觉语言模型易学到虚假相关，现有缓解方法依赖额外数据、标注或重训练，难以扩展。
method: 提出DIAL零样本框架，用稀疏自编码器解耦、识别并无标签去除受虚假相关影响的表示成分。
result: 实验表明无需辅助数据或外部监督即可有效缓解虚假相关，提升下游任务鲁棒性。
conclusion: 为缺乏显式监督时解耦不变与虚假特征提供了可解释、可扩展的通用方法。
---

## Abstract
Vision-Language Models (VLMs) have demonstrated impressive zero-shot capabilities across a wide range of tasks and domains. However, their performance is often compromised by learned spurious correlations, which can adversely affect downstream applications. Existing mitigation strategies typically depend on additional data, model retraining, labeled features or classes, domain-specific expertise, or external language models posing scalability and generalization challenges. In contrast, we introduce a fully interpretable, zero-shot method that requires no auxiliary data or external supervision named DIAL (Disentangle, Identify, And Label-free removal). Our approach begins by filtering the representations that might be disproportionately influenced by spurious features, using distributional analysis. We then apply a sparse autoencoder to disentangle the representations and identify the feature directions associated with spurious features. To mitigate their impact, we remove the subspace spanned by these spurious directions from the affected representations. 
Additionally, for cases where prior knowledge of spurious features in a dataset is unknown, we introduce DIAL+ which can detect and mitigate the spurious features. We validate our method through extensive experiments on widely used spurious correlation benchmarks. Results show that our approach consistently outperforms or matches existing baselines in terms of overall accuracy and worst-group performance, offering a scalable and interpretable solution to a persistent challenge in VLMs.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无标签地解耦并去除虚假相关。

### 2. 核心内容
针对视觉语言模型学到虚假相关而损害下游泛化的问题，本文提出无需额外数据与外部监督的零样本方法DIAL，通过解耦、识别与无标签去除三个步骤过滤表示中受虚假相关过度影响的成分。该方法完全可解释，避免了以往依赖重训练、标注特征或外部语言模型的局限。实验证明其在无监督条件下有效缓解虚假相关，为缺少显式监督时的不变与虚假特征解耦提供了直接可迁移的技术路线。

### 3. 对应检索需求
How to identify and disentangle invariant features from variant or spurious features without explicit environment labels or invariant feature supervision?

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=NHOLsaHuFv](https://openreview.net/forum?id=NHOLsaHuFv)
