---
title: "Skill-Based Mixture-of-Experts: Adaptive Routing for Heterogeneous Reasoning via Inferred Skills"
title_zh: 技能式混合专家：基于推断技能的异构推理自适应路由
authors: "Justin Chen, Sukwon Yun, Elias Stengel-Eskin, Tianlong Chen, Mohit Bansal"
date: 2026-04-30
pdf: "https://openreview.net/pdf/920dfc96a4f8616ab72d1c0cec8cba896384c0a9.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 实例级专家选择，按查询技能动态调整知识整合
tldr: 将多个预训练模型组合用于推理时，任务级专家选择过于粗糙，因为不同实例需要不同专长。作者提出Skill-MoE，一种无梯度的技能式框架，先从查询中推断技能再据此选择专家，并由聚合器整合多专家输出。实验显示实例级选择显著提升异构推理表现，为按实例动态调整知识整合策略提供了范例。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 任务级专家选择过于粗糙，不同实例需要不同专长。
method: 提出Skill-MoE，推断查询技能并按技能相关性选择专家，用聚合器整合输出。
result: 实例级专家选择显著提升异构推理任务的性能。
conclusion: 表明按实例动态整合专家知识优于粗粒度选择，可迁移到药物对建模。
---

## Abstract
Combining existing pre-trained LLMs is a promising approach for diverse reasoning tasks. However, task-level expert selection is often too coarse-grained, since different instances may require different expertise. To address this, we propose Skill-MoE, a symbolic, skill-based, and gradient-free Mixture-of-Experts framework for instance-level expert selection. Skill-MoE infers skills (e.g., algebra in mathematics) from each query, selects experts based on skill relevance, and lets each expert generate its own reasoning. The resulting k outputs are then synthesized by an aggregator chosen for its ability to integrate diverse responses. While instance-level selection substantially improves performance, naively implementing it incurs heavy overhead from repeated model loading and offloading. We address this with a batch inference strategy that groups instances by assigned experts, allowing each model to be loaded only once. As a result, Skill-MoE integrates 16 expert models on a single GPU with runtime comparable to prior multi-agent baselines using 4 GPUs. Across diverse benchmarks (MMLU-Pro, GPQA, AIME, and MedMCQA), Skill-MoE achieves an average absolute improvement of 8.15% over the best baseline. It also generalizes well to unseen tasks and outperforms discussion-based methods without requiring expensive multi-round interactions.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
实例级专家选择，按查询技能动态调整知识整合。

### 2. 核心内容
将多个预训练模型组合用于推理时，任务级专家选择过于粗糙，因为不同实例需要不同专长。作者提出Skill-MoE，一种无梯度的技能式框架，先从查询中推断技能再据此选择专家，并由聚合器整合多专家输出。实验显示实例级选择显著提升异构推理表现，为按实例动态调整知识整合策略提供了范例。

### 3. 对应检索需求
How can models dynamically adapt knowledge integration strategies to different drug pairs when heterogeneous knowledge sources contribute unequally across instances?

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=M2pbI9uKjW](https://openreview.net/forum?id=M2pbI9uKjW)
