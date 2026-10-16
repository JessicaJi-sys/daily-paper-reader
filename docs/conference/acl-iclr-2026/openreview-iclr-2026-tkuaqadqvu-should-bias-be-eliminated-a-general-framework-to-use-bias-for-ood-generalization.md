---
title: Should Bias be Eliminated? A General Framework to Use Bias for OOD Generalization
title_zh: 偏置应当被消除吗？一个利用偏置实现OOD泛化的通用框架
authors: "Yan Li, Yunlong Deng, Zijian Li, Anpeng Wu, Zeyu Tang, Kun Zhang, Guangyi Chen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=TKuAQAdQvU"
tags: ["query:ood-inv"]
score: 8.0
evidence: 利用纠缠偏置提升OOD泛化的通用框架
tldr: 该文质疑OOD泛化中普遍丢弃上下文偏置的做法，提出偏置未必应被消除。作者首先从理论上刻画偏置特征产生正作用的条件，指出其有害与有益成分往往相互纠缠，进而给出一个通用框架以有效利用偏置。研究表明合理利用偏置可提升OOD泛化能力，为不变特征与虚假特征的解耦与利用提供了新的分析视角。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 主流OOD方法一味丢弃上下文偏置，可能损失有益信息。
method: 理论刻画偏置有益条件，并提出利用纠缠偏置的通用框架。
result: 分析表明在纠缠情形下合理利用偏置可提升OOD泛化。
conclusion: 为不变与虚假特征的处理提供了新的分析视角。
---

## Abstract
Most approaches to out-of-distribution (OOD) generalization learn domain-invariant representations by discarding contextual bias. In this paper, we raise a critical question: Should bias be eliminated? If not, is there a general way to leverage it for better OOD generalization? To answer these questions, we first provide a theoretical analysis that characterizes the circumstances in which biased features contribute positively. Although theoretical results show that bias may sometimes play a positive role, leveraging it effectively is non-trivial, since its harmful and beneficial components are often entangled. Recent advances have sought to refine the prediction of bias by presuming reliable prediction from invariant features. However, such assumptions may be too strong in the real world, especially when the target also shifts from training to testing domains. Motivated by this challenge, we introduce a framework to leverage bias in a more general scenario. Specifically, we employ a generative model to capture the data generation process and identify the underlying bias factors, which are then used to construct a bias-aware predictor. Since the bias-aware predictor may shift across environments, we first estimate the environment state to train predictors under different environments, combining them as a mixture of domain experts for the final prediction. Then, we built a general invariant predictor, which can be invariant under label shift, to guide the adaptation of the bias-aware predictor. Evaluations on synthetic data and standard domain generalization benchmarks demonstrate that our method consistently outperforms both invariance-only baselines and recent bias-utilization approaches, yielding improved robustness and adaptability.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
利用纠缠偏置提升OOD泛化的通用框架。

### 2. 核心内容
该文质疑OOD泛化中普遍丢弃上下文偏置的做法，提出偏置未必应被消除。作者首先从理论上刻画偏置特征产生正作用的条件，指出其有害与有益成分往往相互纠缠，进而给出一个通用框架以有效利用偏置。研究表明合理利用偏置可提升OOD泛化能力，为不变特征与虚假特征的解耦与利用提供了新的分析视角。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=TKuAQAdQvU](https://openreview.net/forum?id=TKuAQAdQvU)
