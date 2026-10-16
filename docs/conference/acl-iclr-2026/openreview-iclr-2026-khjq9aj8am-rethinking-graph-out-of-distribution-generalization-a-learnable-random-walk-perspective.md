---
title: "Rethinking Graph Out-Of-Distribution Generalization: A Learnable Random Walk Perspective"
title_zh: 重新思考图 OOD 泛化：可学习随机游走视角
authors: "Henan Sun, Xunkai Li, Junyi Han, Zekai Chen, Jia Li, Rong-Hua Li, Guoren Wang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=KHJq9aJ8Am"
tags: ["query:ood-inv"]
score: 8.0
evidence: 以可学习随机游走刻画图 OOD 不变知识
tldr: 针对图神经网络在分布偏移下性能下降、而现有图 OOD 方法以不变拓扑或图谱作为不变知识、但现实中二者未必成立的问题，本文提出可学习随机游走（LRW）视角，把随机游走模式作为不变知识的实例化。基于此提出 LRW-OOD 方法实现图 OOD 泛化，并重新审视不变风险最小化与结构因果模型在图上的假设。该工作为图结构数据的分布外泛化与不变表征学习提供了新的不变性刻画思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有图 OOD 方法把不变知识理解为不变拓扑或图谱，但现实中二者未必成立。
method: 提出可学习随机游走 LRW 视角与 LRW-OOD 方法，将随机游走模式作为不变知识。
result: LRW-OOD 在图上实现了 OOD 泛化，并对现有不变性假设提出反思。
conclusion: 为图结构数据的分布外泛化提供了新的不变性刻画范式。
---

## Abstract
Out-Of-Distribution (OOD) generalization has gained increasing attentions for machine learning on graphs, as graph neural networks (GNNs) often exhibit performance degradation under distribution shifts. Existing graph OOD methods tend to follow the basic ideas of invariant risk minimization and structural causal models, interpreting the invariant knowledge across datasets under various distribution shifts as graph topology or graph spectrum. However, these interpretations may be inconsistent with real-world scenarios, as neither invariant topology nor spectrum is assured. In this paper, we advocate the learnable random walk (LRW) perspective as the instantiation of invariant knowledge, and propose LRW-OOD to realize graph OOD generalization learning. Instead of employing fixed probability transition matrix (i.e., degree-normalized adjacency matrix), we parameterize the transition matrix with an LRW-sampler and a path encoder. Furthermore, we propose the kernel density estimation (KDE)-based mutual information (MI) loss to generate random walk sequences that adhere to OOD principles.  Extensive experiment demonstrates that our model can effectively enhance graph OOD generalization under various types of distribution shifts and yield a significant accuracy improvement of 3.87\% over state-of-the-art graph OOD generalization baselines.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
以可学习随机游走刻画图 OOD 不变知识。

### 2. 核心内容
针对图神经网络在分布偏移下性能下降、而现有图 OOD 方法以不变拓扑或图谱作为不变知识、但现实中二者未必成立的问题，本文提出可学习随机游走（LRW）视角，把随机游走模式作为不变知识的实例化。基于此提出 LRW-OOD 方法实现图 OOD 泛化，并重新审视不变风险最小化与结构因果模型在图上的假设。该工作为图结构数据的分布外泛化与不变表征学习提供了新的不变性刻画思路。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=KHJq9aJ8Am](https://openreview.net/forum?id=KHJq9aJ8Am)
