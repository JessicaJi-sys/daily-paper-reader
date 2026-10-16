---
title: "Fed-DIP: Federated Domain Generalization by Synergizing Implicit Disentanglement and Context-Aware Prompting"
title_zh: Fed-DIP：协同隐式解耦与上下文感知提示的联邦域泛化
authors: "Hongze Li, Zesheng Zhou, Xinhui Li, Hui Wang, Wei Chen, Xiaojin Zhang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=VbmV3rs284"
tags: ["query:ood-inv"]
score: 7.0
evidence: 解耦域不变特征与域特有特征
tldr: 针对联邦域泛化中因数据隔离导致域不变与域特有特征难以彻底解耦、泛化受限的问题，本文提出Fed-DIP框架，引入隐式解耦蒸馏机制，通过比较logit输出实现细粒度特征分离，并结合上下文感知提示提升对未见目标域的适应能力。该方法缓解了现有方法解耦不彻底、性能受限的缺陷。实验表明其在多个联邦域泛化基准上取得更优结果，为无中心数据场景下的不变特征解耦提供了可借鉴思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 联邦域泛化需分离域不变与域特有特征，但数据隔离使现有方法解耦不彻底、泛化受限。
method: 提出Fed-DIP，通过隐式解耦蒸馏比较logit实现特征分离，并用上下文感知提示增强泛化。
result: 实验表明该框架在联邦域泛化基准上实现更细粒度解耦并提升对未见域的性能。
conclusion: 为数据隔离场景下的不变特征解耦与鲁棒泛化提供了有效且可迁移的机制。
---

## Abstract
Federated Domain Generalization (FedDG) seeks to train a model on decentralized data from multiple source domains that can generalize effectively to unseen target domains. A fundamental challenge lies in achieving robust feature disentanglement—separating domain-invariant from domain-specific features—which is critical for generalization but severely hindered by the data-isolated nature of Federated Learning. Existing methods often struggle with this, leading to incomplete decoupling and limited model performance. To address this, we propose Fed-DIP, a novel framework that introduces an Implicit Decoupling Distillation mechanism. This mechanism achieves fine-grained feature separation by comparing logit outputs for local image regions, all without direct data access. This allows for the robust aggregation of domain-invariant knowledge while critically preserving rich, domain-specific information at the client side. Furthermore, to unlock the potential of this preserved local knowledge, we introduce the Context-Aware Prompt Encoder (CAPE). Unlike prior works that rely on selective prompting from a fixed set, CAPE is a fully generative solution. It dynamically synthesizes adaptive, end-to-end optimizable text prompts directly from local visual features. These generated prompts provide nuanced, contextual guidance, enabling the model to effectively leverage domain-specific insights for more robust and accurate decision-making. Extensive experiments on benchmarks including PACS, VLCS, OfficeHome, and DomainNet demonstrate that our method achieves state-of-the-art (SOTA) performance, validating the effectiveness and superiority of our framework.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
解耦域不变特征与域特有特征。

### 2. 核心内容
针对联邦域泛化中因数据隔离导致域不变与域特有特征难以彻底解耦、泛化受限的问题，本文提出Fed-DIP框架，引入隐式解耦蒸馏机制，通过比较logit输出实现细粒度特征分离，并结合上下文感知提示提升对未见目标域的适应能力。该方法缓解了现有方法解耦不彻底、性能受限的缺陷。实验表明其在多个联邦域泛化基准上取得更优结果，为无中心数据场景下的不变特征解耦提供了可借鉴思路。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=VbmV3rs284](https://openreview.net/forum?id=VbmV3rs284)
