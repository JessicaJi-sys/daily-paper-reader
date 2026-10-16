---
title: Graph Attention with Knowledge-Aware Domain Adaptation for Drug-Target Interaction Prediction
title_zh: 面向药物靶点相互作用预测的图注意力与知识感知域适应
authors: "Ellen Yi-Ge, Taric Chen, Heng Huang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=boxKMr17zV"
tags: ["query:ood-inv"]
score: 5.0
evidence: 域偏移下的药物靶点相互作用域适应
tldr: 针对数据驱动药物发现中域偏移下药物靶点相互作用预测困难的问题，本文提出DTI-DA框架，结合图注意力网络编码化合物、知识感知网络注入化学与生物先验，并利用最大均值差异与对抗域判别进行域适应。系统端到端、模块化且可复现，并区分仅源域与转导式无监督域适应两种评测设定。实验验证了该框架在域偏移下提升DTI预测的能力，为药物相关分布外泛化提供了方法参考。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 数据驱动药物发现中，域偏移条件下药物靶点相互作用预测仍具挑战，现有方法泛化不足。
method: 提出DTI-DA，融合图注意力编码、知识感知先验注入与基于MMD的对抗域适应。
result: 实验在源域与转导式无监督域适应两种设定下验证了该框架提升域偏移DTI预测的效果。
conclusion: 为药物发现中分布偏移下的关系预测提供了模块化、可复现的域适应方案。
---

## Abstract
Predicting drug-target interactions (DTIs) under domain shift is a central challenge in data-driven drug discovery. In this context, we suggest DTI-DA, a practical framework which combines (i) a Graph Attention Network (GAT) for compound encoding, (ii) a Knowledge-Aware Network (KAN) for injecting prior chemical and biological relations into representation learning and (iii) domain adaptation (DA) with the help of maximum mean discrepancy with adversarial domain discrimination. The subsequent system is end-to-end, modular and a repeatable process. In particular, we differentiate two tracks of reporting, that is, source only (no access to unlabeled target data for any method) and transductive UDA (unlabeled target examples aiding the distribution alignment while target labels are always strictly hidden). Beginning comparators are reported in parallel to contextualise performance improvements. We do not make claims of statistical significance and all numbers are treated as single-run point estimates at a fixed protocol. Minor differences between runs (with an AUC of 0.744 in the primary comparison vs. 0.7452 in ablation) are the result of different runs with the same parameter settings (and are irrelevant for the conclusion) and are left in for the sake of fidelity to the runs. Under the mentioned settings, DTI-DA also rivals the performance of strictly classical machine-learning baselines like SVM and RF, as well as widely-known deep baselines like GraphDTA and MolTrans, on BioSNAP and BindingDB. For example, on BioSNAP we have an AUC of 0.744 and an AUPR of 0.757, which calculates to a relative improvement of 0.895%.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
域偏移下的药物靶点相互作用域适应。

### 2. 核心内容
针对数据驱动药物发现中域偏移下药物靶点相互作用预测困难的问题，本文提出DTI-DA框架，结合图注意力网络编码化合物、知识感知网络注入化学与生物先验，并利用最大均值差异与对抗域判别进行域适应。系统端到端、模块化且可复现，并区分仅源域与转导式无监督域适应两种评测设定。实验验证了该框架在域偏移下提升DTI预测的能力，为药物相关分布外泛化提供了方法参考。

### 3. 对应检索需求
research on out of distribution generalization and invariant representation learning for cold start drug drug interaction prediction。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=boxKMr17zV](https://openreview.net/forum?id=boxKMr17zV)
