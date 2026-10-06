---
title: Discriminative Mixture-of-Experts on Graphs with Reliable Expert Fusion
title_zh: 基于可靠专家融合的图判别式混合专家
authors: "Haoyue Deng, Menghui Wang, Yunlong Zhou, Ziwei Zhang, Ran Zhang, Chunming Hu, Xiao Wang"
date: 2026-04-30
pdf: "https://openreview.net/pdf/531cf9f037582858332d97b2928952c50e7bc18c.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 图混合专家的路由与专家专门化
tldr: 图混合专家通过自适应容量分配提升GNN规模，但其效果取决于路由决策与专家专门化的协调。本文通过实证研究发现两个关键现象：专家与路由两侧都存在判别性损失，GNN专家高度同质化且路由器坍缩到少数专家；同时路由不确定性普遍存在，并与模型表现强负相关。为此提出带可靠专家融合的判别式图混合专家方法，以改善路由与专家专门化的协同。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 图混合专家存在专家同质化与路由器坍缩问题，且路由不确定性普遍，削弱了多样化图语义的刻画。
method: 提出判别式图混合专家框架，通过可靠专家融合机制协调路由决策与专家专门化。
result: 实证揭示了专家与路由两侧的判别性损失及路由不确定性与性能的负相关，方法缓解了这些问题。
conclusion: 协调路由与专家专门化是提升图混合专家表达能力的关键。
---

## Abstract
Graph Mixture-of-Experts (Graph-MoE) offers a way to scale GNNs via adaptive capacity allocation, with the goal of allowing different experts to capture diverse graph patterns. Its effectiveness heavily depends on the coordination between routing decisions and expert specialization. However, through extensive empirical study, we identify two critical phenomena. First, discrimination loss occurs on both the expert and routing sides, where GNN experts become highly homogenized and the router collapses to a small subset of experts, failing to reflect diverse graph semantics. Second, routing uncertainty is prevalent, as existing routers produce uncertain expert assignments for most nodes, and such uncertainty exhibits a strong negative correlation with model performance.
To address these issues, we propose C$^2$GMoE, a novel Graph-MoE framework featuring Contrastive routing and Confidence-aware fusion. We introduce a group-wise contrastive routing strategy that provides explicit guidance for routing optimization by aligning node-level routing decisions with semantic clusters while satisfying load-balancing constraints. Moreover, through a theoretical analysis of generalization error, we develop a confidence-aware fusion mechanism that adaptively reweights expert predictions according to their confidence. Extensive experiments across multiple benchmarks demonstrate the effectiveness of our proposed C$^2$GMoE.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
图混合专家的路由与专家专门化。

### 2. 核心内容
图混合专家通过自适应容量分配提升GNN规模，但其效果取决于路由决策与专家专门化的协调。本文通过实证研究发现两个关键现象：专家与路由两侧都存在判别性损失，GNN专家高度同质化且路由器坍缩到少数专家；同时路由不确定性普遍存在，并与模型表现强负相关。为此提出带可靠专家融合的判别式图混合专家方法，以改善路由与专家专门化的协同。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=iB1x9F6n3p](https://openreview.net/forum?id=iB1x9F6n3p)
