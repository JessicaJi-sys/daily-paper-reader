---
title: Cross-Modal Feature Disentanglement with Contrastive Task Alignment for Multi-Modal Image Fusion
title_zh: 面向多模态图像融合的跨模态特征解耦与对比任务对齐
authors: "Shenghai Wu, Yue Lin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=Jz5OcxVJbP"
tags: ["query:ood-inv"]
score: 6.0
evidence: 用可微正交分解解耦纠缠特征
tldr: 针对多模态图像融合中模态、内容与任务相关信息在统一表征空间内相互纠缠、导致融合质量与泛化受限的问题，本文提出 CMD-CTA 框架，通过数学驱动的特征分离与语义对齐加以解决。方法引入可微正交特征分解，鼓励将表征分离为内容、模态等成分，并用对比任务对齐增强语义一致性。该工作提供了可迁移的特征解耦机制，对解耦不变与虚假特征有方法上的借鉴意义，但任务场景为图像融合。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 多模态图像融合中模态、内容与任务信息在统一表征空间内相互纠缠，影响泛化。
method: 提出 CMD-CTA，用可微正交特征分解与对比任务对齐实现特征分离与语义对齐。
result: 在真实融合基准上验证了特征分离与对齐对融合质量与泛化的改善。
conclusion: 提供了可迁移的特征解耦思路，可借鉴于不变与虚假特征的分离。
---

## Abstract
Multi-modal image fusion suffers from feature entanglement, where modality-specific, content-specific, and task-specific information becomes conflated in unified representation spaces, leading to suboptimal fusion quality and limited generalization. This paper proposes Cross-Modal Feature Disentanglement with Contrastive Task Alignment (CMD-CTA), a framework that addresses this fundamental challenge through mathematically motivated feature separation and semantic alignment, supported by both theoretical analysis under idealized assumptions and empirical evidence on real-world fusion benchmarks. The approach introduces two key innovations: (1) differentiable orthogonal feature decomposition that encourages separation into content, modality, and task subspaces under information-theoretic sufficiency constraints; and (2) contrastive task alignment that establishes semantic bridges through learnable prototypes and multi-granularity contrastive learning. We further adopt hybrid Vision Mamba–Swin backbone to couple linear-complexity long-range modeling with windowed locality, thereby reducing parameters while preserving context. Extensive experiments across six fusion tasks and downstream object detection demonstrate 5.8--7.3\% improvements over state-of-the-art methods, 6.1\% higher mAP\@0.5, and 15.7$\times$ parameter efficiency. This empirically validated framework for representation learning in multi-modal fusion has broad implications for computer vision and autonomous systems.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用可微正交分解解耦纠缠特征。

### 2. 核心内容
针对多模态图像融合中模态、内容与任务相关信息在统一表征空间内相互纠缠、导致融合质量与泛化受限的问题，本文提出 CMD-CTA 框架，通过数学驱动的特征分离与语义对齐加以解决。方法引入可微正交特征分解，鼓励将表征分离为内容、模态等成分，并用对比任务对齐增强语义一致性。该工作提供了可迁移的特征解耦机制，对解耦不变与虚假特征有方法上的借鉴意义，但任务场景为图像融合。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=Jz5OcxVJbP](https://openreview.net/forum?id=Jz5OcxVJbP)
