---
title: "FEDEMOE: IMPROVING PERSONALIZATION ON HET- EROGENEOUS FEDERATED LEARNING VIA ELASTIC MIXTURE OF EXPERTS ARCHITECTURE"
title_zh: FedEMoE：通过弹性混合专家架构提升异构联邦学习的个性化能力
authors: "Haizhou Du, Lixin Huang, Zonghan Wu, Nitin Bisht, Huan Huo, Xiufeng Liu"
date: 2025-09-09
pdf: "https://openreview.net/pdf?id=EC1NTRLwfS"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 异构下解耦个性化与泛化的弹性混合专家架构
tldr: 异构联邦学习面临数据分布与资源异质问题，现有方法常使个性化与泛化知识相互纠缠或彼此压制，导致个性化性能下降。本文提出FedEMoE弹性混合专家架构，通过多尺度个性化专家丰富个性化知识，并设计弹性共享专家以解耦泛化与个性化。该设计在异构分布下改善了模型个性化表现，为在分布异质场景中整合共享与专门知识提供了MoE式思路，对分布依赖的多源知识整合有借鉴价值。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 异构联邦学习中个性化与泛化知识常被纠缠或相互压制，造成模型个性化性能退化，难以兼顾共享知识与本地专门知识。
method: 论文提出弹性混合专家架构FedEMoE，用多尺度个性化专家丰富本地知识，并引入弹性共享专家将个性化与泛化知识解耦。
result: 在异构联邦设置下，该架构缓解了个性化与泛化的冲突，提升了模型在数据分布异质场景中的个性化表现。
conclusion: 工作表明用MoE结构分离共享与专门知识有助于应对分布异质性，对分布依赖的多源知识效用整合具有方法启示。
---

## Abstract
Heterogeneous federated learning (HtFL) has emerged as a promising approach to address heterogeneity in local computational resources and data distribution, as is common in the real world. However, existing methods cause performance degradation of model personalization because personalized and generalized knowledge are either intertwined or dominated by one of them. To address this issue, we propose a novel Elastic Mixture of Experts (EMoE) architecture on HtFL, namely FedEMoE, decoupling personalization from generalization. In detail, FedEMoE employs a multi-scale feature extraction mechanism via personalized experts to enrich personalized knowledge. Furthermore, we design an elastic shared expert to break the transferred knowledge bottleneck across heterogeneous client models. The elastic shared expert can adaptively expand or shrink according to the status of each expert by the weight spectrum analysis, respectively. Moreover, the
sparsity of mixture of experts (MoE) alleviates the loss of personalized knowledge that typically results from dense model aggregation. Extensive experiments across statistical and model heterogeneity settings demonstrate that FedEMoE significantly outperforms state-of-the-art federated learning methods on the performance of each heterogeneous model over diverse datasets.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
异构下解耦个性化与泛化的弹性混合专家架构。

### 2. 核心内容
异构联邦学习面临数据分布与资源异质问题，现有方法常使个性化与泛化知识相互纠缠或彼此压制，导致个性化性能下降。本文提出FedEMoE弹性混合专家架构，通过多尺度个性化专家丰富个性化知识，并设计弹性共享专家以解耦泛化与个性化。该设计在异构分布下改善了模型个性化表现，为在分布异质场景中整合共享与专门知识提供了MoE式思路，对分布依赖的多源知识整合有借鉴价值。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=EC1NTRLwfS](https://openreview.net/forum?id=EC1NTRLwfS)
