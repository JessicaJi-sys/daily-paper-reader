---
title: Robust Domain Generalization under Divergent Marginal and Conditional Distributions
title_zh: 边缘与条件分布偏移下的鲁棒域泛化
authors: "Je Won Yeom, Kyubyung Chae, Hyunggyu Lim, Yoonna Oh, Dongyoon Yang, Taesup Kim"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=I5Qgn23qAz"
tags: ["query:ood-inv"]
score: 6.0
evidence: 在边缘与条件分布同时偏移下学习域不变表示
tldr: 针对现有域泛化方法普遍假设标签边缘分布P(Y)稳定、仅处理条件分布偏移的局限，本文研究标签边缘与条件分布同时变化的更现实情形，提出面向未见域的新风险上界与鲁棒域泛化框架。该框架显式建模两类分布偏移，从而学习更稳健的域不变表示。这为分布偏移复杂、环境不规整场景下的不变学习提供了更一般的理论刻画。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有域泛化方法多假设标签边缘稳定，难以应对边缘与条件分布同时变化的现实场景。
method: "提出面向未见域的新风险上界，显式建模P(Y)与P(X|Y)同时偏移下的域不变表示学习框架。"
result: 在两类分布同时偏移的设定下，该框架相较仅处理条件偏移的方法更鲁棒。
conclusion: 更一般的风险刻画拓展了不变表示学习对复杂分布偏移的适用性。
---

## Abstract
Domain generalization (DG) aims to learn predictive models that can generalize to unseen domains.
Most existing DG approaches focus on learning domain-invariant representations under the assumption of conditional distribution shift (i.e., they primarily address changes in $P(X|Y)$ while assuming the label marginal $P(Y)$ remains stable). 
However, real-world data seldom satisfy this assumption.
Multiple domains often differ in more complex ways, where both the label distribution $P(Y)$ and the conditional distribution $P(X|Y)$ vary simultaneously.
In this work, we propose a new framework for robust domain generalization under divergent marginal and conditional distributions. 
We introduce a novel risk bound for unseen domains by explicitly decomposing the joint distribution into marginal and conditional components and characterizing risk gaps arising from both sources of divergence. 
To operationalize this bound, we design a meta-learning procedure that minimizes and validates the proposed risk bound across seen domains, ensuring strong generalization to unseen ones. 
Empirical evaluations demonstrate that our method achieves state-of-the-art performance not only on conventional DG benchmarks but also in challenging Multi-Domain Long-Tailed Recognition (MDLT) settings where both marginal and conditional shifts are pronounced.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
在边缘与条件分布同时偏移下学习域不变表示。

### 2. 核心内容
针对现有域泛化方法普遍假设标签边缘分布P(Y)稳定、仅处理条件分布偏移的局限，本文研究标签边缘与条件分布同时变化的更现实情形，提出面向未见域的新风险上界与鲁棒域泛化框架。该框架显式建模两类分布偏移，从而学习更稳健的域不变表示。这为分布偏移复杂、环境不规整场景下的不变学习提供了更一般的理论刻画。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=I5Qgn23qAz](https://openreview.net/forum?id=I5Qgn23qAz)
