---
title: "Deceptive Risk Minimization: Out-of-Distribution Generalization by Deceiving Distribution Shift Detectors"
title_zh: 欺骗式风险最小化：通过欺骗分布漂移检测器实现分布外泛化
authors: Anirudha Majumdar
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=7tAfOGcqz8"
tags: ["query:ood-inv"]
score: 9.0
evidence: 无需域标签即可学习消除虚假相关的稳定不变特征
tldr: 针对现有不变表示学习依赖显式环境或域标签的问题，本文提出欺骗式风险最小化（DRM）机制：通过让训练数据在基于保形鞅的分布漂移检测器看来呈现独立同分布，从而自动识别出消除虚假相关性的稳定不变特征。该方法以可微目标同时优化特征稳定性与任务损失，无需域适应或环境标注即可实现分布外泛化。这为无环境标签条件下的不变表示学习提供了新范式，可直接迁移到融合药物对表示的OOD场景。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 现有不变表示学习方法通常需要显式环境或域标签，限制了在缺乏环境标注场景下的应用。
method: 提出DRM，让表示在保形鞅漂移检测器看来呈独立同分布，用可微目标同时学习稳定特征与最小化任务损失。
result: 方法无需域适应或环境标签即可识别稳定特征，消除虚假相关并泛化到未见域。
conclusion: 欺骗检测器视角为无监督不变特征学习提供了可行机制，适合缺少环境标签的OOD任务。
---

## Abstract
This paper proposes deception as a mechanism for out-of-distribution (OOD) generalization: by learning data representations that make training data appear independent and identically distributed (iid) to an observer, we can identify stable features that eliminate spurious correlations and generalize to unseen domains. We refer to this principle as deceptive risk minimization (DRM) and instantiate it with a practical differentiable objective that simultaneously learns features that eliminate distribution shifts from the perspective of a detector based on conformal martingales while minimizing a task-specific loss. In contrast to domain adaptation or prior invariant representation learning methods, DRM does not require access to test data or a partitioning of training data into a finite number of data-generating domains. We demonstrate the efficacy of DRM on numerical experiments with concept shift and a simulated imitation learning setting with covariate shift in environments that a robot is deployed in.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无需域标签即可学习消除虚假相关的稳定不变特征。

### 2. 核心内容
针对现有不变表示学习依赖显式环境或域标签的问题，本文提出欺骗式风险最小化（DRM）机制：通过让训练数据在基于保形鞅的分布漂移检测器看来呈现独立同分布，从而自动识别出消除虚假相关性的稳定不变特征。该方法以可微目标同时优化特征稳定性与任务损失，无需域适应或环境标注即可实现分布外泛化。这为无环境标签条件下的不变表示学习提供了新范式，可直接迁移到融合药物对表示的OOD场景。

### 3. 对应检索需求
invariant representation learning without explicit environment labels。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=7tAfOGcqz8](https://openreview.net/forum?id=7tAfOGcqz8)
