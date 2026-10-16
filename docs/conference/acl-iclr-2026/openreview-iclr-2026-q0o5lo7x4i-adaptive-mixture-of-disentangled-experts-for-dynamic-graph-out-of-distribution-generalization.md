---
title: Adaptive Mixture of Disentangled Experts for Dynamic Graph Out-of-Distribution Generalization
title_zh: 面向动态图分布外泛化的自适应解耦专家混合
authors: "Haibo Chen, Xin Wang, Guanheng Chen, Yuan Meng, Haoyang Li, Yang Yao, Zeyang Zhang, Zhiqiang Zhang, JUN ZHOU, Ling Feng, Wenwu Zhu"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=q0O5LO7X4I"
tags: ["query:ood-inv"]
score: 9.0
evidence: 自适应解耦专家混合捕捉不变模式实现OOD泛化
tldr: 针对动态图分布外泛化中固定架构难以应对随时间演化的分布偏移的问题，本文首次提出自适应架构设计，引入自适应架构专家混合来捕捉不断变化分布下的不变模式，并解耦不变与变异表示。实验表明该方法在动态图OOD任务上优于固定架构基线，验证了专家混合与解耦机制的有效性。这为混合专家与不变学习结合、直接作用于表示层的方法提供了直接参照，可迁移到药物对多分类预测场景。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 动态图OOD泛化中分布偏移随时间演化，固定架构提取不变模式效果次优。
method: 提出自适应架构设计，用自适应架构专家混合捕捉演化分布下的不变模式并解耦变异特征。
result: 在动态图OOD基准上取得优于固定架构方法的性能，验证解耦专家机制有效。
conclusion: 自适应专家混合与解耦思想可直接启发无环境标签下的不变表示学习与融合表示建模。
---

## Abstract
Dynamic graph out-of-distribution (OOD) generalization has drawn an increasing amount of attention in the research community, given its wide applicability in real-world scenarios. Existing methods typically employ a fixed-architecture design to extract invariant patterns. However, there may exist evolving distribution shifts in dynamic graphs, leading to suboptimal performance of fixed-architecture designs. To address this issue, we propose a novel adaptive-architecture design to handle evolving distribution shifts over time, to the best of our knowledge, for the first time. The proposed adaptive-architecture design introduces an adaptive mixture of architecture experts to capture invariant patterns under evolving distribution shifts, which imposes three challenges: 1) How to detect and characterize evolving distribution shifts to inform architectural decisions; 2) How to dynamically route different expert architectures to handle varying distribution characteristics; 3) How to ensure that the adaptive mixture of experts effectively discovers invariant patterns. To solve these challenges, we propose a novel **Ada**ptive **Mix**ture of Disentangled Experts (**AdaMix**) model to adaptively route architecture experts to varying distribution shifts and jointly learn spatio-temporal invariant patterns. Specifically, we propose a spatio-temporal distribution detector to infer evolving distribution shifts by jointly leveraging historical and current information. Building upon this, we develop a prototype-guided mixture of disentangled experts that adaptively routes experts with disentangled factors to different distribution shifts. Finally, we design a distribution-aware intervention mechanism that discovers invariant patterns based on expert selection of nodes. Extensive experiments on both synthetic and real-world datasets demonstrate that our proposed **AdaMix** model significantly outperforms state-of-the-art baselines.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
自适应解耦专家混合捕捉不变模式实现OOD泛化。

### 2. 核心内容
针对动态图分布外泛化中固定架构难以应对随时间演化的分布偏移的问题，本文首次提出自适应架构设计，引入自适应架构专家混合来捕捉不断变化分布下的不变模式，并解耦不变与变异表示。实验表明该方法在动态图OOD任务上优于固定架构基线，验证了专家混合与解耦机制的有效性。这为混合专家与不变学习结合、直接作用于表示层的方法提供了直接参照，可迁移到药物对多分类预测场景。

### 3. 对应检索需求
methods for multi class prediction of unseen drug pairs using invariant learning and mixture of experts。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=q0O5LO7X4I](https://openreview.net/forum?id=q0O5LO7X4I)
