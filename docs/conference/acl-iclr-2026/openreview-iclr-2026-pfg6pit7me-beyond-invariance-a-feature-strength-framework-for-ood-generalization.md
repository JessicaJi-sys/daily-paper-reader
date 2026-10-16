---
title: "Beyond Invariance: A Feature-Strength Framework for OOD Generalization"
title_zh: 超越不变性：面向OOD泛化的特征强度框架
authors: "Rana Shahroz, Zhen Tan, Mufan Qiu, Charles Fleming, Tianlong Chen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=PfG6piT7ME"
tags: ["query:ood-inv"]
score: 9.0
evidence: 分析虚假特征与不变特征的OOD泛化框架
tldr: 本文针对现有OOD方法一味寻找不变特征、却忽视模型为何学习虚假捷径特征的问题，提出从特征强度角度解释泛化失败的框架。作者认为模型倾向于学习训练集中最具预测力的虚假相关特征，并据此给出新的分析视角。该框架为理解和缓解分布外泛化中的捷径学习提供了可迁移思路，对不变表示学习具有直接启发。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 现有OOD研究多聚焦寻找不变特征，却忽视了训练数据为何诱导模型学习虚假捷径特征这一根本问题。
method: 论文提出特征强度框架，从训练特征强度分布的角度分析模型偏好虚假相关的原因并给出缓解思路。
result: 实验表明该方法能刻画并削弱虚假特征的主导作用，从而改善分布外泛化性能。
conclusion: 该工作为理解并抑制OOD中的捷径学习提供了新的特征强度视角，可迁移到不变表示学习。
---

## Abstract
Out-of-Distribution (OOD) generalization is a central challenge in machine learning. Models often fail on unseen data, not because of an inability to learn robust signals, but because they $\textit{preferentially learn spurious, dataset-specific correlations that are highly predictive for in-distribution examples}$. Existing solutions typically focus on searching for invariant features, yet often overlook a more fundamental question: $\textbf{what properties of the training data cause models to learn these non-invariant ``shortcut" features in the first place?}$ In this work, we present a different perspective on OOD generalization. We argue that failures to generalize are a direct consequence of models learning the strongest features in the training data, which are often spurious. Guided by this, we reframe OOD generalization not as a search for invariance, but as the $\textit{problem of identifying and mitigating the influence of these overly dominant features}$. Under this new perspective, we develop a novel primitive for quantifying feature strength across a training set. This primitive gives rise to a targeted regularization algorithm that weakens a model's reliance on the identified strongest features, thereby compelling it to learn more robust and causally stable signals. Our method demonstrates substantial improvements in generalization across a wide range of OOD benchmarks, improving OOD accuracy by up to $2\times$ over standard training and significantly outperforming existing baselines without compromising in-distribution performance.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分析虚假特征与不变特征的OOD泛化框架。

### 2. 核心内容
本文针对现有OOD方法一味寻找不变特征、却忽视模型为何学习虚假捷径特征的问题，提出从特征强度角度解释泛化失败的框架。作者认为模型倾向于学习训练集中最具预测力的虚假相关特征，并据此给出新的分析视角。该框架为理解和缓解分布外泛化中的捷径学习提供了可迁移思路，对不变表示学习具有直接启发。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=PfG6piT7ME](https://openreview.net/forum?id=PfG6piT7ME)
