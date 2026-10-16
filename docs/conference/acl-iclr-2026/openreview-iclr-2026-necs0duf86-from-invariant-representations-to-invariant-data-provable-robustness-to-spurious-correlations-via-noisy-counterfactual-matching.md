---
title: "From Invariant Representations to Invariant Data: Provable Robustness to Spurious Correlations via Noisy Counterfactual Matching"
title_zh: 从不变表示到不变数据：通过噪声反事实匹配实现对虚假相关的可证明鲁棒性
authors: "Ruqi Bai, Yao Ji, Zeyu Zhou, David I. Inouye"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=nEcs0Duf86"
tags: ["query:ood-inv"]
score: 9.0
evidence: 无环境标签下借助反事实匹配对抗虚假相关
tldr: 该文针对不变表示学习方法常逊于普通经验风险最小化、难以应对虚假相关的问题，转而从数据层面出发，利用天然满足不变性的反事实样本对，提出噪声反事实匹配（NCM）这一约束式方法。理论证明即使仅有少量含噪反事实对，也能获得对虚假相关的可证明鲁棒性。该工作为缺少显式环境标签时学习不变性提供了新范式，对无环境标注的不变学习具有重要启发意义。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 不变表示方法常不如普通经验风险最小化，难以应对训练数据中的虚假相关。
method: 提出数据中心的噪声反事实匹配NCM，利用应具相同预测的样本对作为约束。
result: 证明少量含噪反事实对即可带来可证明的虚假相关鲁棒性提升。
conclusion: 为无环境标签下的不变学习提供了数据层面的新范式。
---

## Abstract
Models that learn spurious correlations from training data often fail when deployed in new environments. While many methods aim to learn invariant representations to address this, they often underperform standard empirical risk minimization (ERM). We propose a data-centric alternative that shifts the focus from learning invariant representations to leveraging invariant data pairs---pairs of samples that should have the same prediction. We prove that certain counterfactuals naturally satisfy this invariance property. Based on this, we introduce Noisy Counterfactual Matching (NCM), a simple constraint-based method that improves robustness by leveraging even a small number of \emph{noisy} counterfactual pairs---improving upon prior works that do not explicitly consider noise. For linear causal models, we prove that NCM's test-domain error is bounded by its in-domain error plus a term dependent on the counterfactuals' quality and diversity. Experiments on synthetic data validate our theory, and we demonstrate NCM's effectiveness on real-world datasets.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无环境标签下借助反事实匹配对抗虚假相关。

### 2. 核心内容
该文针对不变表示学习方法常逊于普通经验风险最小化、难以应对虚假相关的问题，转而从数据层面出发，利用天然满足不变性的反事实样本对，提出噪声反事实匹配（NCM）这一约束式方法。理论证明即使仅有少量含噪反事实对，也能获得对虚假相关的可证明鲁棒性。该工作为缺少显式环境标签时学习不变性提供了新范式，对无环境标注的不变学习具有重要启发意义。

### 3. 对应检索需求
How to identify and disentangle invariant features from variant or spurious features without explicit environment labels or invariant feature supervision?

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=nEcs0Duf86](https://openreview.net/forum?id=nEcs0Duf86)
