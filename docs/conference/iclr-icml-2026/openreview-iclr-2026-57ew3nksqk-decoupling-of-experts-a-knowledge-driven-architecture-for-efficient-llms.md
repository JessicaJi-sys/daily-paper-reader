---
title: "Decoupling of Experts: A Knowledge-Driven Architecture for Efficient LLMs"
title_zh: 专家解耦：面向高效大模型的知识驱动架构
authors: "Qiuwu Chen, Zimo Liu, Yaofo Chen, Zhijie Qiu, Ryan Dong, Ying Sun, Yuchen Li, Simeng Ma, Yifan Zhang, Mingkui Tan"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=57Ew3NKsQK"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 抛弃静态MoE专家，动态合成知识块，无需人工定义专家语义
tldr: 现有大模型尤其是专家混合变体难以实现高效、结构化且可解释的扩展。该文提出解耦专家架构，先用LDA从语料构建语义主题基础，再将其整合进主模型并动态精炼，抛弃传统静态专家，改用按需动态合成的知识块。该方法使计算扎根于层级化、可动态更新的知识空间，提升了扩展的结构性与可解释性。其贡献在于为无需人工定义专家语义的自适应专家专门化提供了新范式。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有大模型尤其是专家混合变体难以实现高效、结构化且可解释的参数扩展。
method: 提出解耦专家架构，用LDA构建语义主题基础，并以动态合成的知识块替代传统静态MoE专家。
result: 使计算扎根于层级化、可动态更新的知识空间，提升了扩展的结构性与可解释性。
conclusion: 为无需人工定义专家语义的自适应专家专门化提供了新范式。
---

## Abstract
Current large language models (LLMs), particularly Mixture-of-Experts (MoE) variants, face challenges in achieving efficient, structured, and interpretable scaling. We introduce the Decoupling of Experts (DoE) architecture, a novel framework that addresses these limitations by grounding computation in a hierarchically organized and dynamically updated knowledge space. Our methodology features a two-stage lifecycle: we first use Latent Dirichlet Allocation (LDA) to build a semantic topic foundation from the training corpus. This knowledge is then integrated into the main LLM, where it is dynamically refined. Critically, we discard traditional, static MoE experts. Instead, the expert entity is a dynamic \textbf{Knowledge Block} synthesized on-the-fly by reusing the Key and Value matrices from the attention computation. We replace the standard load balancer and softmax gating with an \textbf{Attention Gating Control (AGC)} that employs a VAE-based router with a ReLU activation for expert composition. This entire process is optimized with a composite loss function, balancing next-token prediction with a KL-divergence-based expert loss. Our analysis reveals that this architecture induces a remarkable \textbf{heterogeneous specialization} across layers, with some layers differentiating into "science" and "humanities" domains, while others converge on general functions. This demonstrates a learned, hierarchical division of labor, paving the way for a new, more efficient scaling dimension based on the number of structured experts.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
抛弃静态MoE专家，动态合成知识块，无需人工定义专家语义。

### 2. 核心内容
现有大模型尤其是专家混合变体难以实现高效、结构化且可解释的扩展。该文提出解耦专家架构，先用LDA从语料构建语义主题基础，再将其整合进主模型并动态精炼，抛弃传统静态专家，改用按需动态合成的知识块。该方法使计算扎根于层级化、可动态更新的知识空间，提升了扩展的结构性与可解释性。其贡献在于为无需人工定义专家语义的自适应专家专门化提供了新范式。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=57Ew3NKsQK](https://openreview.net/forum?id=57Ew3NKsQK)
