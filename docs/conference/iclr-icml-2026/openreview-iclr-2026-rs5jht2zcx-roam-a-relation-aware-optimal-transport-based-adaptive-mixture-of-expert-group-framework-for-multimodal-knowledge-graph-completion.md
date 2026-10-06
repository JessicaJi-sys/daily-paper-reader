---
title: "ROAM: A Relation-aware Optimal Transport-based Adaptive Mixture-of-Expert-Group Framework for Multimodal Knowledge Graph Completion"
title_zh: ROAM：基于关系感知最优传输的自适应专家混合组多模态知识图谱补全框架
authors: "Xinrong Hu, Bin Li, Wanqing Li, Jie Yang, Wenbin Zhang, Yi Guo"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=rs5JhT2zCx"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 关系感知最优传输的自适应专家混合，避免预定义路由
tldr: 针对多模态知识图谱补全需融合结构、文本、视觉等异构信息，而现有专家混合方法依赖预定义路由或任务无关距离、适应性不足的问题，本文提出ROAM框架。该方法利用关系感知的最优传输实现自适应专家分组与路由，在保留各模态语义的同时缓解跨模态干扰。实验表明ROAM提升了多模态知识图谱补全的融合效果与整体性能。工作展示了自适应MoE在异构知识整合中的潜力，可迁移至多源药物知识融合场景。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 多模态知识图谱补全需融合异构模态信息，现有MoE依赖预定义路由与任务无关距离，适应性受限。
method: 提出ROAM，采用关系感知最优传输实现自适应专家分组与路由，在保留模态语义的同时抑制跨模态干扰。
result: 在多模态知识图谱补全任务中缓解跨模态干扰，提升异构信息融合与补全性能。
conclusion: 展示自适应MoE在异构知识整合中的潜力，可迁移至多源药物知识融合与动态整合场景。
---

## Abstract
Multimodal Knowledge Graph Completion (MMKGC) aims to predict missing facts by reasoning over heterogeneous information sources, including structural, textual, and visual modalities. A central challenge in this task lies in effectively integrating modality-specific information while preserving their distinct semantics and mitigating cross-modal interference. Recent efforts have explored employing Mixture of-Experts (MoE) architectures to address this issue. However, many of these approaches rely on predefined expert routing or task-agnostic distance measures, thereby limiting their adaptability and performance. This paper proposes ROAM, a Relation-aware Optimal Transport-based Adaptive Mixture-of-Expert-Group framework, which dynamically routes modality-specific embeddings across expert groups conditioned on relation semantics. Specifically, ROAM first establishes modality-specialized expert groups to disentangle representation learning across modalities. Then, an Optimal Transport-based gating mechanism is introduced with a learnable, relation-conditioned cost function. Expert groups are further represented dynamically via their constituent parameters, enabling context-sensitive routing and capturing relation-aware specialization. Extensive experiments on multiple MMKGC benchmarks demonstrate that ROAM achieves state-of-the-art performance, achieving up to 9.76% relative gains.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
关系感知最优传输的自适应专家混合，避免预定义路由。

### 2. 核心内容
针对多模态知识图谱补全需融合结构、文本、视觉等异构信息，而现有专家混合方法依赖预定义路由或任务无关距离、适应性不足的问题，本文提出ROAM框架。该方法利用关系感知的最优传输实现自适应专家分组与路由，在保留各模态语义的同时缓解跨模态干扰。实验表明ROAM提升了多模态知识图谱补全的融合效果与整体性能。工作展示了自适应MoE在异构知识整合中的潜力，可迁移至多源药物知识融合场景。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=rs5JhT2zCx](https://openreview.net/forum?id=rs5JhT2zCx)
