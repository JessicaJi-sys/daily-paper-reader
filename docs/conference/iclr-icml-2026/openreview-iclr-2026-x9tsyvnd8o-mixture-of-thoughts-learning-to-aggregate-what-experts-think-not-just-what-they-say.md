---
title: "Mixture of Thoughts: Learning to Aggregate What Experts Think, Not Just What They Say"
title_zh: 思维混合：学习聚合专家的思考而非仅其输出
authors: "Jacob Fein-Ashley, Dhruv Parikh, Rajgopal Kannan, Viktor Prasanna"
date: 2025-09-15
pdf: "https://openreview.net/pdf?id=x9tSyvnD8o"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 全局路由选择专家并在隐层聚合异质知识
tldr: 针对现有多种LLM协作方法要么独立生成、要么多轮交换成本高、要么需架构同质的问题，本文提出思维混合（MoT）。该方法在全局路由下由轻量路由器选择top-K专家，并通过交互层在隐层聚合异质专家的思考。研究实现了异构专家间的隐层级协作，为多源知识整合与动态专家路由提供了可迁移方案。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有多专家协作方法独立生成或成本高或需架构同质。
method: 提出MoT，用全局路由选择top-K专家并做隐层交互聚合。
result: 实现异构专家间的隐层级协作与知识整合。
conclusion: 为多源异质知识动态路由整合提供通用思路。
---

## Abstract
Open-source Large Language Models (LLMs) increasingly specialize by domain (e.g., math, code, general reasoning), motivating systems that leverage complementary strengths across models. Prior multi-LLM approaches either (i) route a query to one or a few experts and generate independently, (ii) aggregate outputs from each model via costly multi-turn exchanges, or (iii) fuse weights into a single model—typically requiring architectural homogeneity. We introduce Mixture of Thoughts (MoT), a simple method for latent-level collaboration among heterogeneous experts under a global routing scheme. For each query, a lightweight router selects top-$K$ experts and designates a primary expert; uniformly placed interaction layers project hidden states into a shared latent space where the primary expert performs cross-attention over its active (selected) peers. Pre-trained experts remain frozen; only the router and the lightweight interaction layers are trained with a novel joint training objective that improves both the expert selection and inter-expert collaboration. Across five in-distribution (ID) and three out-of-distribution (OOD) benchmarks, MoT surpasses the current routing and aggregation-based state-of-the-art, Avengers, by $+0.38\%$ and $+2.92\%$, respectively. Further, MoT significantly outperforms the best-performing single model. It achieves this with single-pass inference, runtime comparable to routing baselines, and none of the overheads of iterative aggregation. MoT offers a simple latent-space mechanism for combining heterogeneous LLMs, a practical step toward broader multi-LLM collaboration. Our code is publicly available at \url{https://anonymous.4open.science/r/mot-5B4B/}.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
全局路由选择专家并在隐层聚合异质知识。

### 2. 核心内容
针对现有多种LLM协作方法要么独立生成、要么多轮交换成本高、要么需架构同质的问题，本文提出思维混合（MoT）。该方法在全局路由下由轻量路由器选择top-K专家，并通过交互层在隐层聚合异质专家的思考。研究实现了异构专家间的隐层级协作，为多源知识整合与动态专家路由提供了可迁移方案。

### 3. 对应检索需求
How can models dynamically adapt knowledge integration strategies to different drug pairs when heterogeneous knowledge sources contribute unequally across instances?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=x9tSyvnD8o](https://openreview.net/forum?id=x9tSyvnD8o)
