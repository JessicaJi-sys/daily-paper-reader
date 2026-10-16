---
title: Variational Learning of Disentangled Representations
title_zh: 解耦表征的变分学习
authors: "Yuli Slavutsky, Ozgur Beker, David Blei, Bianca Dumitrascu"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=6P3JxS3Pfl"
tags: ["query:ood-inv"]
score: 8.0
evidence: 无需先验地解耦不变与条件特异因子
tldr: 针对现有VAE类方法在分离不变因子与条件特异因子时存在潜变量泄漏、限制泛化的问题，本文提出DisCoVR变分框架，采用双潜变量结构、并行重构与最大最小目标，无需手工先验即可显式分离不变与条件特异因素。实验表明该框架能在生物医学等场景中有效隔离稳定信号，提升对新治疗、患者或物种的泛化能力。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有VAE方法分离不变与条件特异因子时存在潜变量泄漏，限制泛化。
method: 提出DisCoVR，用双潜变量结构、并行重构与最大最小目标显式分离两类因子。
result: 实验表明其能在生物医学场景中隔离稳定信号并提升跨条件泛化。
conclusion: 为无先验条件下的不变表征解耦提供了有效变分方案。
---

## Abstract
Disentangled representations allow models to separate factors shared across conditions from those that are condition-specific. This separation is crucial in domains such as biomedicine, where generalization to new treatments, patients, or species requires isolating stable biological signals from context-dependent effects. While several VAE-based extensions aim to achieve this, they often exhibit leakage between latent variables, limiting generalization.
We introduce DisCoVR, a variational framework that explicitly separates invariant and condition-specific factors through: (i) a dual-latent architecture, (ii) parallel reconstructions to keep both representations informative, and (iii) a max–min objective that enforces separation without handcrafted priors.
We show this objective maximizes data likelihood, promotes disentanglement, and admits a unique equilibrium.
Empirically, DisCoVR achieves stronger disentanglement on synthetic data, natural images, and single-cell RNA-seq datasets, establishing it as a principled approach for multi-condition representation learning.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无需先验地解耦不变与条件特异因子。

### 2. 核心内容
针对现有VAE类方法在分离不变因子与条件特异因子时存在潜变量泄漏、限制泛化的问题，本文提出DisCoVR变分框架，采用双潜变量结构、并行重构与最大最小目标，无需手工先验即可显式分离不变与条件特异因素。实验表明该框架能在生物医学等场景中有效隔离稳定信号，提升对新治疗、患者或物种的泛化能力。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=6P3JxS3Pfl](https://openreview.net/forum?id=6P3JxS3Pfl)
