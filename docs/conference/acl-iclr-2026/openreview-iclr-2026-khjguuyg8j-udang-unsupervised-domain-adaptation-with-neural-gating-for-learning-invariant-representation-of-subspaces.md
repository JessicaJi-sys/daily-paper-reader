---
title: "UDANG: Unsupervised Domain Adaptation with Neural Gating for learning invariant representation of subspaces"
title_zh: UDANG：用于学习子空间不变表示的无监督域适应神经门控
authors: "Jen Yee Kok, Vellayappan Dheivanayagam, Ching Teo, Teck-Yian Lim"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=khjGuuYg8j"
tags: ["query:ood-inv"]
score: 7.0
evidence: 无监督域适应学习不变表示且无需标签
tldr: 该文针对深度模型在源域与目标域分布不一致时性能骤降的问题，指出主流无监督域适应方法依赖域对抗训练却未显式解耦任务特征。作者提出UDANG，利用神经门控在子空间层面学习不变表示，并分离任务相关与域相关成分。方法在域适应任务上提升了目标域泛化性能，为在缺少环境标签时解耦不变特征提供了可借鉴的机制。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 域对抗等域适应方法未显式解耦任务特征与域特征，导致迁移性能受限。
method: 提出UDANG，用神经门控在子空间层面学习不变表示并分离任务成分。
result: 在域适应任务上提升了目标域泛化性能并实现特征解耦。
conclusion: 为无环境标签下解耦不变特征提供了可借鉴机制。
---

## Abstract
The key assumption of deep learning is that the data that the model will be tested on (target domain) are drawn from the same distribution as the data it was trained on (source domain). Breaking this assumption can lead to a significant drop in performance despite having similar underlying features between the source and target domains. Unsupervised Domain Adaptation (UDA) involves using unlabeled samples from the target domain, in addition to labeled samples from source domain, to train a model that can perform well on the target domain. Many existing UDA approaches rely on domain adversarial training (DAT) to reduce domain shift. Although effective, they do not explicitly disentangle the learned features into task-specific and domain-specific components. As a result, the features despite appearing to be domain invariant, may still contain domain-specific biases. To address this, we propose a novel method, UDA with Neural Gating (UDANG), that utilizes a dual adversarial objective to learn an adaptive gating which dynamically route each feature dimension to either the domain or task subspace. Using our strategy, networks have the ability to effectively disentangle task-specific features from domain-specific ones. We validated our approach in multiple datasets and network architectures for image classification, demonstrating strong adaptation performance while retaining the features for discerning the domain.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无监督域适应学习不变表示且无需标签。

### 2. 核心内容
该文针对深度模型在源域与目标域分布不一致时性能骤降的问题，指出主流无监督域适应方法依赖域对抗训练却未显式解耦任务特征。作者提出UDANG，利用神经门控在子空间层面学习不变表示，并分离任务相关与域相关成分。方法在域适应任务上提升了目标域泛化性能，为在缺少环境标签时解耦不变特征提供了可借鉴的机制。

### 3. 对应检索需求
invariant representation learning without explicit environment labels。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=khjGuuYg8j](https://openreview.net/forum?id=khjGuuYg8j)
