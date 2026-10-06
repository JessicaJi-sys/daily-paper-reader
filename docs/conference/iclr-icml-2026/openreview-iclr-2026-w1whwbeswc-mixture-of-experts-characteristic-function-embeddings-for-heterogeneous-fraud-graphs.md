---
title: Mixture of Experts Characteristic Function Embeddings for Heterogeneous Fraud Graphs
title_zh: 面向异质欺诈图的混合专家特征函数嵌入
authors: "Junliang Luo, Di Wu, Xue Liu"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=W1whWBesWC"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 输入自适应MoE投影为异质图实例专门化
tldr: 针对异质图欺诈检测中多重关系与属性异质偏差纠缠于单一流程的问题，本文提出先解耦再融合的表示学习框架。结构侧用特征函数签名刻画分布邻域，属性侧用输入自适应混合专家投影为每个实例按角色专门化。该方法实现了对异质关系的自适应融合，提升了跨域欺诈检测的泛化能力。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 异质图欺诈检测中多重偏差被纠缠于单一流程。
method: 先解耦结构属性再用输入自适应MoE投影做自适应融合。
result: 实现对异质关系的自适应专门化，提升跨域检测表现。
conclusion: 为异质图上的实例级专家专门化提供思路。
---

## Abstract
Fraud detection over heterogeneous graphs requires reasoning over multiplex relations, attribute polymorphism, and structural heterophily, yet prevailing detectors entangle these orthogonal biases into monolithic pipelines assumed to generalize across domains. We address this limitation by instantiating a decouple–then–fuse representation learning that isolates structural and attribute channels before reintroducing interaction through an adaptive fusion interface. On the structural side, we encode distributional neighborhood context via characteristic-function signatures compressed through randomized spectral factorization; on the attribute side, we deploy input-adaptive Mixture-of-Experts projections that specialize each instance to role-conditioned patterns. The two views are subsequently reconciled through a Bayesian mean–difference fusion layer that models per-node consensus and discrepancy, enabling calibrated integration under heterophily and cross-modal conflict. Empirical evaluation across benchmark fraud graphs from telecom records, e-commerce reviews, and cryptocurrency transactions domains shows improved fraud node detection performance, attributable to the model’s ability to disentangle structural and attribute features and reconcile their discrepancies.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
输入自适应MoE投影为异质图实例专门化。

### 2. 核心内容
针对异质图欺诈检测中多重关系与属性异质偏差纠缠于单一流程的问题，本文提出先解耦再融合的表示学习框架。结构侧用特征函数签名刻画分布邻域，属性侧用输入自适应混合专家投影为每个实例按角色专门化。该方法实现了对异质关系的自适应融合，提升了跨域欺诈检测的泛化能力。

### 3. 对应检索需求
How can models dynamically adapt knowledge integration strategies to different drug pairs when heterogeneous knowledge sources contribute unequally across instances?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=W1whWBesWC](https://openreview.net/forum?id=W1whWBesWC)
