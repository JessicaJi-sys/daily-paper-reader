---
title: Towards Robust Out-of-Distribution Generalization for Deep Neural Networks with Tailored Data Regularization
title_zh: 面向深度神经网络鲁棒 OOD 泛化的定制数据正则化
authors: "Umberto Barros, Cristofer Silva, William Teles de Andrade Junior, Marcos Oliveira, CARMELO JOSE ALBANEZ BASTOS FILHO, Diego Pinheiro"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=9eBYO45Fcx"
tags: ["query:ood-inv"]
score: 7.0
evidence: 通过随机数据正则化提升 OOD 泛化
tldr: 针对深度神经网络在分布偏移下易过拟合、OOD 泛化能力不足的问题，本文系统探索随机变换与噪声注入等随机数据正则化技术，并通过课程学习式的调度策略框架对其进行组织。研究将正则化从孤立策略扩展为渐进式训练机制，以更好地管理偏差—方差权衡。实验展示了该类数据正则在缓解分布压力、提升 OOD 泛化方面的作用，为鲁棒表征学习提供了简单有效的正则化视角。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 深度神经网络在分布偏移下容易过拟合，OOD 泛化能力不足。
method: 采用随机变换与噪声注入等数据正则化，并用课程学习式调度策略加以组织。
result: 渐进式调度正则有助管理偏差—方差权衡，缓解分布压力。
conclusion: 为提升 DNN 的 OOD 泛化提供了简单有效的正则化训练框架。
---

## Abstract
Out-of-Distribution (OOD) generalization remains both a fundamental challenge and an often-overlooked aspect of modern machine learning—especially in the context of Deep Neural Networks (DNNs), which are highly expressive yet prone to overfitting under distributional stress. Classical learning theory highlights the role of regularization in managing the bias-variance trade-off—particularly important for complex models with higher VC dimension. In this work, we explore stochastic data regularization techniques—such as random transformations and noise injection—applied not only as isolated strategies but also organized through a Scheduling Policy framework using a Curriculum Learning-based approach. By progressively increasing input difficulty during training, the scheduling aligns model capacity with task complexity, promoting more robust generalization. We also propose a novel statistical procedure to assess the consistency of performance estimates across cross-validation folds, mitigating miscoverage effects in confidence interval estimation. Altogether, our findings highlight the importance of a tailored data regularization, where the selection, combination, and scheduling of perturbations become key to achieving OOD robustness in DNNs.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过随机数据正则化提升 OOD 泛化。

### 2. 核心内容
针对深度神经网络在分布偏移下易过拟合、OOD 泛化能力不足的问题，本文系统探索随机变换与噪声注入等随机数据正则化技术，并通过课程学习式的调度策略框架对其进行组织。研究将正则化从孤立策略扩展为渐进式训练机制，以更好地管理偏差—方差权衡。实验展示了该类数据正则在缓解分布压力、提升 OOD 泛化方面的作用，为鲁棒表征学习提供了简单有效的正则化视角。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=9eBYO45Fcx](https://openreview.net/forum?id=9eBYO45Fcx)
