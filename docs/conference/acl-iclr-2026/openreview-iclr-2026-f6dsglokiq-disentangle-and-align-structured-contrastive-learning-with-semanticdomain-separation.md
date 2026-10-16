---
title: "Disentangle and Align: Structured Contrastive Learning with Semantic–Domain Separation"
title_zh: 解耦与对齐：语义-域分离的结构化对比学习
authors: "Ke Wan, Tianyi Zhao, Tianhao Huang, Guanghui Min, Aiying Zhang, Chen Chen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=f6DsglOKIq"
tags: ["query:ood-inv"]
score: 7.0
evidence: 通过结构化对比学习解耦语义与域特征以提升新域泛化
tldr: 该文指出实例级对比学习在异构域数据中会把跨域但语义相似的样本误判为负例，并将域线索与语义特征纠缠，导致表示按域聚集、新域泛化差。作者提出结构化对比学习SCL，通过语义对比与域对比分别学习语义表示和域表示，并最小化二者依赖实现解耦。该方法获得更可迁移的表示，为域泛化下的特征解耦提供有效手段。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 实例级对比学习在异构域下会把语义相似样本误判为负例并纠缠域线索与语义。
method: 提出结构化对比学习SCL，分别用语义对比与域对比学习两类表示并最小化其依赖。
result: 方法获得更可迁移、非域聚集的表示并改善新域泛化。
conclusion: 显式语义-域解耦有助于鲁棒表示学习。
---

## Abstract
Learning compact representations that preserve semantics while discarding nuisance variation is central to self-supervised learning (SSL).
However, when training data come from heterogeneous domains, instance-level contrastive learning often treats cross-domain yet semantically similar samples as false negatives and entangles domain cues with semantic features, yielding domain-clustered representations that generalize poorly to novel domains. To address this issue, we propose Structured Contrastive Learning (SCL).
This unified framework jointly learns (i) a semantic representation $\mathbf{z}_s$ via semantic contrast, (ii) a domain representation $\mathbf{z}_d$ via domain contrast, and (iii) their disentanglement by minimizing the dependence (mutual information) between $\mathbf{z}_s$ and $\mathbf{z}_d$. This structure preserves domain-invariant semantics in $\mathbf{z}_s$ while isolating domain factors in $\mathbf{z}_d$, enabling robust self-supervised training on data from a mixture of domains and out-of-domain(OOD) generalization on novel domains. Theoretically, we proved that the training objective of SCL is to extract semantic and domain information separately, and minimizing the mutual information between $\mathbf{z}_s$ and $\mathbf{z}_d$ can enhance the model’s generalization ability under domain shift. Empirically, we validate the performance of SCL on multi-domain training tasks and its generalization to novel domains through experiments on multiple datasets from multiple modalities.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过结构化对比学习解耦语义与域特征以提升新域泛化。

### 2. 核心内容
该文指出实例级对比学习在异构域数据中会把跨域但语义相似的样本误判为负例，并将域线索与语义特征纠缠，导致表示按域聚集、新域泛化差。作者提出结构化对比学习SCL，通过语义对比与域对比分别学习语义表示和域表示，并最小化二者依赖实现解耦。该方法获得更可迁移的表示，为域泛化下的特征解耦提供有效手段。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=f6DsglOKIq](https://openreview.net/forum?id=f6DsglOKIq)
