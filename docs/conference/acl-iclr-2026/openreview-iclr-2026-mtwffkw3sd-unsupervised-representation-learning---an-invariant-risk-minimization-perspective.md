---
title: Unsupervised Representation Learning - an Invariant Risk Minimization Perspective
title_zh: 无监督表示学习：不变风险最小化视角
authors: "Yotam Norman, Ron Meir"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=MTWFfKw3sd"
tags: ["query:ood-inv"]
score: 9.0
evidence: 无需标签与环境划分的无监督不变风险最小化
tldr: 针对传统不变风险最小化依赖标注数据、需要显式环境划分的问题，本文提出无监督IRM框架，将不变性重新定义为特征分布对齐，从而在无标签条件下学习对分布偏移稳健的表示。作者给出PICA线性方法与VIAE深度生成方法，分别提取不变方向并分离环境不变与环境相关潜变量。实验表明该方法在无环境标签时仍能实现稳健表示学习。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 传统IRM依赖标注数据和显式环境划分，无法用于无标签场景。
method: 将不变性重定义为特征分布对齐，提出PICA线性方法与VIAE深度生成方法。
result: 实验表明在无标签无环境划分时仍能学习对分布偏移稳健的表示。
conclusion: 为缺少环境标签的不变表示学习提供了无监督框架。
---

## Abstract
We propose a novel unsupervised framework for Invariant Risk Minimization (IRM), extending the concept of invariance to settings where labels are unavailable. Traditional IRM methods rely on labeled data to learn representations that are robust to distributional shifts across environments. In contrast, our approach redefines invariance through feature distribution alignment, enabling robust representation learning from unlabeled data. We introduce two methods within this framework: Principal Invariant Component Analysis (PICA), a linear method that extracts invariant directions under Gaussian assumptions, and Variational Invariant Autoencoder (VIAE), a deep generative model that separates environment-invariant and environment-dependent latent factors. Our approach is based on a novel ``unsupervised'' structural causal model and supports environment-conditioned sample-generation and intervention. Empirical evaluations on synthetic dataset, modified versions of MNIST, and CelebA demonstrate the effectiveness of our methods in capturing invariant structure, preserving relevant information, and generalizing across environments without access to labels.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
无需标签与环境划分的无监督不变风险最小化。

### 2. 核心内容
针对传统不变风险最小化依赖标注数据、需要显式环境划分的问题，本文提出无监督IRM框架，将不变性重新定义为特征分布对齐，从而在无标签条件下学习对分布偏移稳健的表示。作者给出PICA线性方法与VIAE深度生成方法，分别提取不变方向并分离环境不变与环境相关潜变量。实验表明该方法在无环境标签时仍能实现稳健表示学习。

### 3. 对应检索需求
invariant representation learning without explicit environment labels。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=MTWFfKw3sd](https://openreview.net/forum?id=MTWFfKw3sd)
