---
title: "Measuring Invariance in Representation Learning: A Robust Evaluation Framework"
title_zh: 度量表示学习中的不变性：一个鲁棒的评估框架
authors: "Wenlu Tang, Shuxin Liang, Zicheng Liu, Ce Zhang, Linglong Kong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=327o4QYRoO"
tags: ["query:ood-inv"]
score: 7.0
evidence: 面向OOD环境的不变表示直接评估准则
tldr: 该文针对分布偏移下不变表示学习缺乏直接、高效评估准则的问题，提出计算高效的评估指标DRIC。它通过密度比把不变预测器的条件期望与环境多样性建立形式化联系，从而可直接度量所学表示在不同OOD环境下的真实不变性。该框架为验证与比较不变表示方法提供了理论可靠的工具，有助于诊断不变学习中的退化现象。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 不变表示学习缺少直接、高效评估其真实不变性的准则。
method: 提出基于密度比的DRIC指标，将不变预测器条件期望与环境多样性关联。
result: 提供理论可靠且计算高效的不变性度量。
conclusion: 有助于诊断不变学习退化并比较不同方法。
---

## Abstract
Distribution shifts challenge reliable deployment even when in-distribution accuracy is high. Invariant representation learning aims to mitigate this challenge by learning feature spaces that remain invariant across diverse out-of-distribution (OOD) scenarios.  However, a critical gap exists in directly and efficiently evaluating the true invariance of learned representations across varied environments. To address this, we introduce DRIC, a novel and computationally efficient criterion designed for the direct assessment of invariant representation performance. DRIC establishes a formal link between the conditional expectation of invariant predictors and environmental diversity through the density ratio, providing a theoretically sound and practical evaluation framework. We validate the effectiveness and robustness of DRIC through extensive numerical experiments on both synthetic and real-world datasets, demonstrating its utility in quantifying and comparing the invariance of learned representations, ultimately contributing to the development of more robust machine learning models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向OOD环境的不变表示直接评估准则。

### 2. 核心内容
该文针对分布偏移下不变表示学习缺乏直接、高效评估准则的问题，提出计算高效的评估指标DRIC。它通过密度比把不变预测器的条件期望与环境多样性建立形式化联系，从而可直接度量所学表示在不同OOD环境下的真实不变性。该框架为验证与比较不变表示方法提供了理论可靠的工具，有助于诊断不变学习中的退化现象。

### 3. 对应检索需求
invariant representation learning without explicit environment labels。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=327o4QYRoO](https://openreview.net/forum?id=327o4QYRoO)
