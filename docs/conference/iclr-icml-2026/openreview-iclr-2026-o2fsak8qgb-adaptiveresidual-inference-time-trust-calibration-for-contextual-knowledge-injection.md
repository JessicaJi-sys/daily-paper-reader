---
title: "AdaptiveResidual: Inference-Time Trust Calibration for Contextual Knowledge Injection"
title_zh: 自适应残差：面向上下文知识注入的推理期信任校准
authors: "Songlin Zhai, Jiaye Li, Tianyu Zhang, Yuan Meng, Guilin Qi"
date: 2025-09-02
pdf: "https://openreview.net/pdf?id=O2FsAk8QGB"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 动态调和外部上下文与内部知识冲突以实现忠实知识整合
tldr: 大模型在上下文信息与内部参数知识冲突时往往低估外部证据，导致输出不可靠甚至自相矛盾。该文受机制可解释性发现启发，识别注意力模块为外部上下文聚合器、前馈网络为内部知识载体，提出推理期信任校准方法自适应地调和知识冲突。方法在冲突场景下提升了对上下文信息的忠实整合能力。其贡献在于为异构知识来源效用不均时的动态融合策略提供了可迁移的校准框架。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 大模型在上下文信息与内部参数知识冲突时倾向低估外部证据，导致输出不可靠甚至自相矛盾。
method: 基于注意力聚合外部上下文、前馈网络承载内部知识的可解释性发现，提出推理期信任校准以动态调和知识冲突。
result: 在知识冲突场景下提升了模型对上下文信息的忠实整合能力，减少矛盾输出。
conclusion: 为异构知识来源贡献不均时的动态融合提供了可迁移的信任校准框架。
---

## Abstract
In modern large language models (LLMs), injecting external knowledge via the context to guide models' outputs toward desired outcomes (e.g., through RAG) is a standard practice. 
However, recent research reveals that once conflicts arise between the contextual information and the internal parametric knowledge, LLMs tend to underutilize the external evidence, leading to unreliable or even contradictory outputs. 
This raises a fundamental question: *how can we dynamically reconcile these knowledge conflicts to ensure faithful integration of contextual information* ? 
Inspired by mechanism interpretability findings that identify the `Attention` module as the primary aggregator of external context and the `FFN` module as the locus of internal knowledge lookup, we pinpoint the vanilla residual pathway as the crucial junction where these two information streams are integrated. 
Based on this insight, we introduce AdaRes (*Ada*ptive *Res*idual), a lightweight, parameter-free trust calibration mechanism that operates at test-time. 
Specifically, AdaRes recalibrates the standard residual connection to dynamically balance the influence of external knowledge (from `Attention`) and internal knowledge (from `FFN`). 
This balancing is guided by two instance-specific "trust scores", which are calculated on-the-fly by probing how much the input query relies on contextual versus parametric knowledge sources. 
By adaptively reweighting these contributions without altering any model parameters, AdaRes effectively mitigates knowledge conflicts. 
Experiments on different benchmarks verify the effectiveness of AdaRes in regulating contextual and parametric knowledge.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
动态调和外部上下文与内部知识冲突以实现忠实知识整合。

### 2. 核心内容
大模型在上下文信息与内部参数知识冲突时往往低估外部证据，导致输出不可靠甚至自相矛盾。该文受机制可解释性发现启发，识别注意力模块为外部上下文聚合器、前馈网络为内部知识载体，提出推理期信任校准方法自适应地调和知识冲突。方法在冲突场景下提升了对上下文信息的忠实整合能力。其贡献在于为异构知识来源效用不均时的动态融合策略提供了可迁移的校准框架。

### 3. 对应检索需求
How can models dynamically adapt knowledge integration strategies to different drug pairs when heterogeneous knowledge sources contribute unequally across instances?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=O2FsAk8QGB](https://openreview.net/forum?id=O2FsAk8QGB)
