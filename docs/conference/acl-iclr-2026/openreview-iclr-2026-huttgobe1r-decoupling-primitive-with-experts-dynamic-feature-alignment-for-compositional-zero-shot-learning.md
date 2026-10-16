---
title: "Decoupling Primitive with Experts: Dynamic Feature Alignment for Compositional Zero-Shot Learning"
title_zh: 以专家解耦基元：组合零样本学习的动态特征对齐
authors: "Xiao Zhang, Haodong Jing, Yongqiang Ma, Nanning Zheng"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=hUtTGobe1r"
tags: ["query:ood-inv"]
score: 6.0
evidence: 面向未见组合对的混合专家方法
tldr: 针对组合零样本学习中原型映射次优、跨模态匹配忽略组合差异的问题，本文提出 EVA，一种基于混合专家（MoE）的语义变体对齐框架，通过领域专家自适应与多专家动态特征对齐识别未知状态-对象组合。实验表明该方法在组合泛化上取得提升，其MoE解耦思路对未见药物对的多分类预测具借鉴价值。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有组合零样本学习用简单原型映射且忽略相同状态或物体内部的组合差异。
method: 提出EVA混合专家框架，引入领域专家自适应与多专家动态特征对齐。
result: 实验表明该方法提升了识别未知状态-对象组合的泛化能力。
conclusion: 其专家解耦思路对未见药物对的多分类预测具有迁移价值。
---

## Abstract
Compositional Zero-Shot Learning (CZSL) investigates compositional generalization capacity to recognize unknown state-object pairs based on learned primitive concepts. Existing CZSL methods typically derive primitives features through a simple composition-prototype mapping, which is suboptimal for a set of individuals that can be divided into distinct semantic subsets. 
Moreover, the one-to-all cross-modal primitives matching neglects compositional divergence within identical states or objects, limiting fine-grained image-composition alignment. In this study, we propose EVA, a Mixture-of-Experts Framework for Semantic Variant Alignment. Specifically, we introduce domain-expert adaption, leveraging multiple experts to achieve token-aware learning and model high-quality primitive representations. To enable accurate compositional generalization, we further present semantic variant alignment to select semantically relevant representation for image-primitives matching. 
Our method significantly outperforms other state-of-the-art CZSL methods on three popular benchmarks in both closed- and open-world settings, demonstrating the efficacy of the proposed insight.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向未见组合对的混合专家方法。

### 2. 核心内容
针对组合零样本学习中原型映射次优、跨模态匹配忽略组合差异的问题，本文提出 EVA，一种基于混合专家（MoE）的语义变体对齐框架，通过领域专家自适应与多专家动态特征对齐识别未知状态-对象组合。实验表明该方法在组合泛化上取得提升，其MoE解耦思路对未见药物对的多分类预测具借鉴价值。

### 3. 对应检索需求
methods for multi class prediction of unseen drug pairs using invariant learning and mixture of experts。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=hUtTGobe1r](https://openreview.net/forum?id=hUtTGobe1r)
