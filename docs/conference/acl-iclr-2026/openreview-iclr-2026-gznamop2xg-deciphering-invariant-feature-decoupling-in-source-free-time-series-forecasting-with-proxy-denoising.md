---
title: Deciphering Invariant Feature Decoupling in Source-free Time Series Forecasting with Proxy Denoising
title_zh: 基于代理去噪的无源时间序列预测不变特征解耦
authors: "Kangjia Yan, Chenxi Liu, Hao Miao, Xinle Wu, Yan Zhao, Chenjuan Guo, Bin Yang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=GZNAMOP2xg"
tags: ["query:ood-inv"]
score: 6.0
evidence: 面向无源域适应的不变特征解耦
tldr: 该文研究无源域适应下的时间序列预测，目标是在不访问源数据的前提下将预训练模型迁移到稀疏目标域。作者提出TimePD框架，通过代理去噪实现不变特征解耦，并借助大语言模型的泛化能力辅助迁移。方法在保护数据隐私的同时提升了目标域预测性能，为无源场景下的不变特征学习提供了新思路。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 无源域适应下时间序列预测需在无源数据时迁移模型并保护数据隐私。
method: 提出TimePD框架，用代理去噪实现不变特征解耦并借助大语言模型泛化能力。
result: 方法在稀疏目标域上提升预测性能且无需访问源数据。
conclusion: 代理去噪与不变解耦可支撑无源场景的时间序列迁移。
---

## Abstract
The proliferation of mobile devices generates a massive volume of time series across various domains, where effective time series forecasting enables a variety of real-world applications. This study focuses on a new problem of source-free domain adaptation for time series forecasting. It aims to adapt a pretrained model from sufficient source time series to the sparse target time series domain without access to the source data, embracing data protection regulations. To achieve this, we propose TimePD, the first source-free time series forecasting framework with proxy denoising, where large language models (LLMs) are employed to benefit from their generalization capabilities. Specifically, TimePD consists of three key components: (1) dual-branch invariant disentangled feature learning that enforces representation- and gradient-wise invariance by means of season-trend decomposition; (2) lightweight, parameter-free proxy denoising that dynamically calibrates systematic biases of LLMs; and (3) knowledge distillation that bidirectionally aligns the denoised prediction and the original target prediction. Extensive experiments on real-world datasets offer insight into the effectiveness of the proposed TimePD, outperforming SOTA baselines by 9.3\% on average.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向无源域适应的不变特征解耦。

### 2. 核心内容
该文研究无源域适应下的时间序列预测，目标是在不访问源数据的前提下将预训练模型迁移到稀疏目标域。作者提出TimePD框架，通过代理去噪实现不变特征解耦，并借助大语言模型的泛化能力辅助迁移。方法在保护数据隐私的同时提升了目标域预测性能，为无源场景下的不变特征学习提供了新思路。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=GZNAMOP2xg](https://openreview.net/forum?id=GZNAMOP2xg)
