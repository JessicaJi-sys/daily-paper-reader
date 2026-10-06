---
title: "Breaking the Echo Chamber: A Dynamic Ensemble Pruning Perspective on MoE"
title_zh: 打破回声室：从动态集成剪枝视角看混合专家
authors: "Xinlai Kang, Dunyao Xue, Zhengbo Wang, Chengshuo Du, Xinghao Chen, Hang Zhou, Hanting Chen, Cheng Meng"
date: 2026-04-30
pdf: "https://openreview.net/pdf/d312606aae054158c524d0c30619a47e34d72e6d.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 混合专家中的多样性感知动态路由
tldr: 现有MoE路由常因贪心top-k导致表示坍塌，或依赖复杂辅助正则而损害性能。本文提出Mahalanobis-Pruned MoE，将路由视为多样性感知的子集选择问题，基于专家共现矩阵建模协方差结构，并优化马氏距离目标以增强专家多样性。实验表明该框架缓解了表示坍塌问题，为动态且专门化的专家路由提供了可迁移的机制。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 现有MoE路由因贪心top-k易表示坍塌，或依赖复杂正则而影响性能。
method: 提出MP-MoE，将路由建模为多样性感知子集选择并优化马氏距离目标。
result: 该框架增强了专家多样性并缓解表示坍塌。
conclusion: 为动态专家路由与专门化提供了新的集成剪枝视角。
---

## Abstract
We introduce Mahalanobis-Pruned Mixture-of-Experts (MP-MoE), a novel routing framework that approaches expert selection from the perspective of ensemble pruning. Existing Mixture-of-Experts (MoE) routing strategies often suffer from representation collapse due to greedy top-k selection mechanisms or rely on complex auxiliary regularization terms that may compromise model performance. To address these issues, we formulate routing as a diversity-aware subset selection problem and optimize a Mahalanobis-distance-based objective that explicitly enhances expert diversity. Specifically, we demonstrate that the expert co-occurrence matrix effectively captures inter-expert correlations, allowing us to efficiently model the covariance structure required for distance computation without accessing expert parameters. Furthermore, we devise a greedy strategy for the routing mechanism, backed by theoretical approximation guarantees, rendering it a plug-and-play module with negligible overhead.
MP-MoE increases wall-clock training time by approximately 3\%, while incurring no additional latency at inference time.
Extensive experiments demonstrate that during the pre-training of the large language model, our method consistently outperforms the baseline by 1-3 percentage points across a broad range of benchmarks.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
混合专家中的多样性感知动态路由。

### 2. 核心内容
现有MoE路由常因贪心top-k导致表示坍塌，或依赖复杂辅助正则而损害性能。本文提出Mahalanobis-Pruned MoE，将路由视为多样性感知的子集选择问题，基于专家共现矩阵建模协方差结构，并优化马氏距离目标以增强专家多样性。实验表明该框架缓解了表示坍塌问题，为动态且专门化的专家路由提供了可迁移的机制。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=7FsbfQgti4](https://openreview.net/forum?id=7FsbfQgti4)
