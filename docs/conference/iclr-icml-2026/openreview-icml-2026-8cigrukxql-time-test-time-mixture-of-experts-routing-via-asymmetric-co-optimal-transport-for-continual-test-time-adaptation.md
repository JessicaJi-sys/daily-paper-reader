---
title: "TiME: Test-Time Mixture-of-Experts Routing via Asymmetric CO-Optimal Transport for Continual Test-Time Adaptation"
title_zh: TiME：基于非对称协同最优传输的测试时混合专家路由用于持续测试时适应
authors: "Tianlun Liu, Zhiliang Tian, Zhen Huang, Tianle Liu, Xingzhi Zhou, Feng Liu, Dongsheng Li"
date: 2026-04-30
pdf: "https://openreview.net/pdf/99d27946a0a370bac62b6ec0546fd2e83312dd7c.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 分布漂移下动态MoE路由，面向未见域的正确路由
tldr: 大语言模型在测试阶段常面临连续域漂移，导致未见域性能下降，而现有持续测试时适应方法受限于稠密模型难以平衡可塑性与稳定性。作者提出TiME，利用非对称协同最优传输在测试时动态调整混合专家路由，以稀疏专家结构缓解域漂移。实验表明该方法在未见漂移域上取得更好的适应性与稳定性权衡，为分布漂移下的动态专家路由提供了新思路。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 持续测试时适应中稠密模型难以兼顾可塑性与稳定性，MoE在未见漂移域路由困难。
method: 提出TiME，用非对称协同最优传输在测试时动态调整混合专家的样本路由。
result: 实验显示该路由方法在未见漂移域上更好地平衡了适应性与稳定性。
conclusion: 表明稀疏专家路由可有效应对分布漂移，为动态路由泛化提供借鉴。
---

## Abstract
Large language models usually face continuous domain shifts during testing, which degrade performance on unseen shifting domains.
So, researchers propose continual test-time adaptation (CTTA) to adapt to evolving testing domains while preserving knowledge of previous domains, making adaptability-stability (A-S) balance.
Existing CTTA methods are constrained by dense base models that encode knowledge from all domains into a global model, hardly achieving the A-S balance.
We observe that the model sparsity of mixture-of-experts (MoE) models is better for achieving A–S balance than dense models.
In CTTA, however, MoE faces difficulty in (1) correctly routing samples from unseen shifting domains and (2) capturing domain-level shifts. 
In this paper, we propose test-time mixture-of-experts routing (TiME) via asymmetric co-optimal transport (As-COOT): we model MoE routing in CTTA as a test-time allocation problem via COOT. 
To ensure reliable routing, we propose a semantic space alignment to align sample-expert distributions via bidirectional contrastive learning.
To address COOT’s limitations in CTTA, we propose As-COOT, relaxing sample-side constraints while enforcing expert-side constraints to ensure noise robustness and balance expert load. Experiments show TiME outperforms baselines.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布漂移下动态MoE路由，面向未见域的正确路由。

### 2. 核心内容
大语言模型在测试阶段常面临连续域漂移，导致未见域性能下降，而现有持续测试时适应方法受限于稠密模型难以平衡可塑性与稳定性。作者提出TiME，利用非对称协同最优传输在测试时动态调整混合专家路由，以稀疏专家结构缓解域漂移。实验表明该方法在未见漂移域上取得更好的适应性与稳定性权衡，为分布漂移下的动态专家路由提供了新思路。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=8CIgRukXql](https://openreview.net/forum?id=8CIgRukXql)
