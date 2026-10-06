---
title: "Measuring Invariance in Representation Learning: A Robust Evaluation Framework"
title_zh: 衡量表征学习中的不变性：一个稳健的评估框架
authors: "Wenlu Tang, Shuxin Liang, Zicheng Liu, Ce Zhang, Linglong Kong"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=327o4QYRoO"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 跨 OOD 环境评估表征的真实不变性
tldr: 分布偏移使模型即便同分布精度高也难以可靠部署，而不变表征学习缺乏直接评估其真实不变性的手段。本文提出 DRIC 准则，借助密度比把不变预测器的条件期望与环境多样性形式化关联，实现高效评估。该准则理论上严谨且计算高效，可跨多种 OOD 环境直接度量不变性。其价值在于为不变表征学习与 OOD 泛化研究提供实用的诊断与评估框架。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 分布偏移下即使同分布精度很高也难以可靠部署，而直接、高效评估所学表征真实不变性仍存在关键空白。
method: 提出 DRIC，一种计算高效的不变性评估准则，通过密度比把不变预测器的条件期望与环境多样性形式化关联。
result: 该准则理论自洽且计算高效，可直接量化表征在不同环境中的不变性表现。
conclusion: 为不变表征学习提供可靠评估工具，有助于诊断并提升 OOD 场景下的泛化稳定性。
---

## Abstract
Distribution shifts challenge reliable deployment even when in-distribution accuracy is high. Invariant representation learning aims to mitigate this challenge by learning feature spaces that remain invariant across diverse out-of-distribution (OOD) scenarios.  However, a critical gap exists in directly and efficiently evaluating the true invariance of learned representations across varied environments. To address this, we introduce DRIC, a novel and computationally efficient criterion designed for the direct assessment of invariant representation performance. DRIC establishes a formal link between the conditional expectation of invariant predictors and environmental diversity through the density ratio, providing a theoretically sound and practical evaluation framework. We validate the effectiveness and robustness of DRIC through extensive numerical experiments on both synthetic and real-world datasets, demonstrating its utility in quantifying and comparing the invariance of learned representations, ultimately contributing to the development of more robust machine learning models.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
跨 OOD 环境评估表征的真实不变性。

### 2. 核心内容
分布偏移使模型即便同分布精度高也难以可靠部署，而不变表征学习缺乏直接评估其真实不变性的手段。本文提出 DRIC 准则，借助密度比把不变预测器的条件期望与环境多样性形式化关联，实现高效评估。该准则理论上严谨且计算高效，可跨多种 OOD 环境直接度量不变性。其价值在于为不变表征学习与 OOD 泛化研究提供实用的诊断与评估框架。

### 3. 对应检索需求
invariant representation learning for stable drug generalization。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=327o4QYRoO](https://openreview.net/forum?id=327o4QYRoO)
