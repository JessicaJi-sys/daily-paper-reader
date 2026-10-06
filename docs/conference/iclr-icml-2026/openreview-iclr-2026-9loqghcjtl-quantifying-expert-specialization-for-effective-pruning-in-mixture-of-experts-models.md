---
title: Quantifying Expert Specialization for Effective Pruning in Mixture-of-Experts Models
title_zh: 量化混合专家模型中的专家专门化以实现有效剪枝
authors: "jie hu, Jiahui Hou, Xiangyang Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=9lOqGhCjtL"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 量化混合专家中的专家专门化程度
tldr: 混合专家模型虽能稀疏激活高效扩展，但所有专家常驻内存造成部署瓶颈，专家剪枝成为关键。现有指标仅基于单层路由或输出，无法刻画专家的跨层全局影响。本文提出跨层信息流分析框架与专家专门化指数ESI，以熵度量专家对下游路由分布的影响。该指标揭示了专家专门化结构，为理解与压缩MoE提供了新工具。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 混合专家模型部署受限于内存瓶颈，现有剪枝指标无法捕捉专家的跨层全局影响。
method: 提出跨层信息流分析框架与专家专门化指数ESI，用熵量化专家对下游路由分布的影响。
result: 该指标能有效刻画专家专门化结构并支撑专家剪枝。
conclusion: 为理解MoE内部专家专门化与压缩提供了可迁移的度量方法。
---

## Abstract
Mixture-of-Experts (MoE) architectures enable efficient scaling of language models through sparse activation. However, their deployment is hindered by a significant memory bottleneck, as all expert parameters must remain resident in memory. Expert pruning is an effective technique to mitigate this issue. Existing methods rely on layer-wise metrics based on either routing behavior or expert outputs. These approaches fail to capture the global influence of an expert on cross-layer information flow. In this paper, we introduce a framework for cross-layer information flow analysis. We propose a novel metric called the Expert Specialization Index (ESI). ESI quantifies the entropy of an expert's influence on downstream routing distributions. This allows it to distinguish between functionally specialized experts and redundant, general-purpose ones. Our analysis on Mixtral-8x7B and Qwen1.5-MoE reveals significant differences in their expert specialization profiles. This leads to a key finding we term architecture-strategy fit. Models with highly specialized experts benefit from preserving the original routing distribution via redirection. In contrast, models with less specialized experts are better served by removing experts and re-normalizing routing probabilities. Supported by experimental results, our ESI analysis allows us to explore how to design compression strategies for different MoE architectures. Our findings provide insights into the relationship between model architecture and effective compression strategies.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
量化混合专家中的专家专门化程度。

### 2. 核心内容
混合专家模型虽能稀疏激活高效扩展，但所有专家常驻内存造成部署瓶颈，专家剪枝成为关键。现有指标仅基于单层路由或输出，无法刻画专家的跨层全局影响。本文提出跨层信息流分析框架与专家专门化指数ESI，以熵度量专家对下游路由分布的影响。该指标揭示了专家专门化结构，为理解与压缩MoE提供了新工具。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=9lOqGhCjtL](https://openreview.net/forum?id=9lOqGhCjtL)
