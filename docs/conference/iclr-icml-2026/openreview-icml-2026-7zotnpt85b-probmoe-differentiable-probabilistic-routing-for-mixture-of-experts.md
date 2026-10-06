---
title: "ProbMoE: Differentiable Probabilistic Routing for Mixture-of-Experts"
title_zh: ProbMoE：面向混合专家的可微概率路由
authors: "Heng Zhao, Zilei Shao, Guy Van den Broeck, Zhe Zeng"
date: 2026-04-30
pdf: "https://openreview.net/pdf/87026d43d1de68060b4ea1b873141dd0268a8830.pdf"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 将专家选择建模为子集分布的可微概率路由
tldr: 混合专家模型依赖top-k路由选择专家，但该过程离散且不可微，需要梯度估计器，其设计仍是难题。本文提出概率路由框架ProbMoE，把专家选择建模为基数受限专家子集上的分布，并将路由转化为该离散子集空间的概率推断。方法在前向采样k专家子集，反向则利用各专家精确边缘概率的梯度作为可处理代理。该工作为更稳定可微的专家路由提供了新范式，对动态专家路由有方法价值。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 混合专家模型靠top-k路由激活少量专家，但该路由离散不可微，需依赖梯度估计器，如何设计有效的专家选择梯度仍是核心难题。
method: 论文提出概率路由框架ProbMoE，将专家选择建模为基数受限专家子集上的分布，并把路由形式化为离散子集空间的概率推断，用专家边缘概率梯度作代理。
result: ProbMoE在前向采样k专家子集、反向利用精确边缘概率梯度，实现了可微且更稳定的专家路由，缓解了离散选择的训练困难。
conclusion: 该工作为混合专家模型提供了可微概率路由的新思路，对药物对级动态专家路由的可训练性具有借鉴意义。
---

## Abstract
Mixture-of-Experts (MoE) models scale by activating only a small subset of experts per token.
However, training such models remains challenging because top-$k$ routing is discrete and non-differentiable, requiring gradient estimators for expert selection whose design remains a central open problem. We introduce ProbMoE, a probabilistic routing framework that models expert selection as a distribution over cardinality-constrained expert subsets and formulates routing as probabilistic inference in this discrete subset space. We first propose ProbMoE Exact-$k$ routing, which samples $k$-expert subsets in the forward pass, and the backward pass uses gradients through each expert's exact marginal probability as a tractable surrogate for the true gradient. ProbMoE naturally generalizes to a dynamic-$k$ routing setting, where both training and inference constrain the routing cardinality to the same predefined range, allowing adaptive expert allocation per token. Across benchmarks and model backbones, ProbMoE Exact-$k$ achieves strong performance compared to competitive baselines, with improved expert utilization and routing diversity; ProbMoE Dynamic-$k$ achieves comparable performance with fewer activated experts. Code is available at: https://github.com/HengHugoZhao/ProbMoE.git

---

## 论文详细总结（自动生成）

### 1. 检索相关性
将专家选择建模为子集分布的可微概率路由。

### 2. 核心内容
混合专家模型依赖top-k路由选择专家，但该过程离散且不可微，需要梯度估计器，其设计仍是难题。本文提出概率路由框架ProbMoE，把专家选择建模为基数受限专家子集上的分布，并将路由转化为该离散子集空间的概率推断。方法在前向采样k专家子集，反向则利用各专家精确边缘概率的梯度作为可处理代理。该工作为更稳定可微的专家路由提供了新范式，对动态专家路由有方法价值。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=7zOtnPt85B](https://openreview.net/forum?id=7zOtnPt85B)
