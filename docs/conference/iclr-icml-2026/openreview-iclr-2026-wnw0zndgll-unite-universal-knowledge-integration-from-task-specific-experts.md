---
title: "UNITE: Universal kNowledge Integration from Task-specific Experts"
title_zh: UNITE：从任务特定专家中提取通用知识集成
authors: "Shuxia Lin, Qiufeng Wang, Xu Yang, Xin Geng"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=WnW0zndglL"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 跨MoE专家的知识整合与固化
tldr: MoE架构的大模型在稀疏激活下表现强劲，但专家知识碎片化且跨层冗余，既有研究多停留在诊断冗余或参数重要性，缺乏将其转化为可复用知识的机制。本文提出UNITE框架，通过Fisher加权融合等方式对任务特定专家进行知识整合与固化。该工作探索MoE是否编码可系统提取与复用的通用知识，为专家知识的跨任务迁移提供了新思路。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: MoE专家知识碎片化且跨层冗余，现有研究缺乏将其转化为可复用知识的机制。
method: 提出UNITE框架，通过Fisher加权融合对任务特定专家进行整合与固化以提取通用知识。
result: 实验探索了MoE中通用知识的可提取性，并验证了整合后专家的知识复用效果。
conclusion: 专家知识整合为MoE的跨任务知识复用与迁移提供了可行路径。
---

## Abstract
Large language models (LLMs) with Mixture-of-Experts (MoE) architectures achieve strong performance under sparse activation. However, their expertise is often fragmented across experts and redundant across layers. Prior studies primarily diagnosed redundancy or parameter importance, revealing overlaps but lacking mechanisms to transform them into reusable knowledge. In contrast, human learning succeeds not by memorizing isolated facts but by reusing shared strategies across domains, which motivates the question: do MoE models similarly encode universal knowledge that can be systematically extracted and reused? We propose Universal kNowledge Integration from Task-specific Experts (UNITE), a framework that consolidates experts through Fisher-weighted fusion and then applies Tucker decomposition to disentangle shared low-rank input/output subspaces as universal knowledge from layer-specific variations. This universal component provides a compact basis for reconstructing target models with flexible depth, enabling lightweight yet competitive adaptation across tasks. To assess effectiveness, we evaluate data efficiency, convergence speed, and generalization across multiple MoE-based LLMs and diverse datasets. The results show that UNITE not only extracts universal knowledge, but also flexibly enabling once-for-all extraction and flexible target model construction that generalize across domains.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
跨MoE专家的知识整合与固化。

### 2. 核心内容
MoE架构的大模型在稀疏激活下表现强劲，但专家知识碎片化且跨层冗余，既有研究多停留在诊断冗余或参数重要性，缺乏将其转化为可复用知识的机制。本文提出UNITE框架，通过Fisher加权融合等方式对任务特定专家进行知识整合与固化。该工作探索MoE是否编码可系统提取与复用的通用知识，为专家知识的跨任务迁移提供了新思路。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=WnW0zndglL](https://openreview.net/forum?id=WnW0zndglL)
