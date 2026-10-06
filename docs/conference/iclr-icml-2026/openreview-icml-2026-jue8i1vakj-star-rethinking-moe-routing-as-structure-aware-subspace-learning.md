---
title: "STAR: Rethinking MoE Routing as Structure-Aware Subspace Learning"
title_zh: STAR：将 MoE 路由重新思考为结构感知的子空间学习
authors: "Sumin Park, Noseong Park"
date: 2026-04-30
pdf: "https://openreview.net/pdf/15e4a8276bd4f3fd1565936df59b7758a922873b.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 将 MoE 路由重构为结构感知子空间学习以实现稳定专家路由
tldr: MoE 的核心动机是输入-专家专门化，但浅层线性路由器对输入结构感知有限，常导致路由不稳定。本文提出 STAR，把路由重新表述为子空间学习问题，用广义 Hebbian 算法维护演化主成分子空间以跟踪输入结构。通过让路由决策直接对齐输入结构，STAR 获得更稳定的专家分配。其贡献在于为 MoE 动态专家路由提供结构感知的改进机制，对专家专门化研究具有借鉴意义。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: MoE 的专家专门化依赖路由器是否感知输入结构，而实践中浅层线性投影路由结构感知不足，导致路由不稳定。
method: 提出 STAR，把 MoE 路由视为子空间学习问题，用广义 Hebbian 算法维护随训练演化的主成分子空间来跟踪输入结构。
result: 通过让路由决策直接对齐输入结构，STAR 实现了更稳定、更具结构感知的专家路由。
conclusion: 表明结构感知的子空间路由能增强 MoE 的输入-专家专门化，为动态专家路由提供新思路。
---

## Abstract
Mixture-of-Experts (MoE) scales model capacity efficiently by selectively routing inputs to a specialized subset of experts. However, input-expert specialization, the core motivation of MoE, critically depends on whether the router is actually aware of input structure. In practice, MoE routing is typically implemented as a shallow linear projection with limited awareness of input representation, which often leads to unstable routing. We propose STAR, a Structure Aware Routing that rethinks MoE routing as a subspace learning problem by augmenting standard learnable routing with an evolving principal subspace that tracks dominant input structure via Generalized Hebbian Algorithm (GHA). By aligning routing decisions directly with input structure, STAR enables stable expert specialization. We evaluate STAR on controlled synthetic setup and large-scale language and vision tasks, where it consistently improves routing quality and downstream performance over strong MoE baselines. Moreover, optional test-time subspace updates further enhance routing robustness and generalization under input distribution shifts. Code is available at \url{https://github.com/psmiz/STAR}.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
将 MoE 路由重构为结构感知子空间学习以实现稳定专家路由。

### 2. 核心内容
MoE 的核心动机是输入-专家专门化，但浅层线性路由器对输入结构感知有限，常导致路由不稳定。本文提出 STAR，把路由重新表述为子空间学习问题，用广义 Hebbian 算法维护演化主成分子空间以跟踪输入结构。通过让路由决策直接对齐输入结构，STAR 获得更稳定的专家分配。其贡献在于为 MoE 动态专家路由提供结构感知的改进机制，对专家专门化研究具有借鉴意义。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=jUE8i1vAKJ](https://openreview.net/forum?id=jUE8i1vAKJ)
