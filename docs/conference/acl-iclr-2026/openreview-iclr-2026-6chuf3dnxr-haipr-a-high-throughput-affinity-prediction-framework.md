---
title: "HAIPR: A High-Throughput Affinity Prediction Framework"
title_zh: HAIPR：一种高通量亲和力预测框架
authors: "Jannis de Riz, Tom U. Schlegel, Jens Meiler, Torben Schiffner"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=6cHUf3Dnxr"
tags: ["query:ood-inv"]
score: 4.0
evidence: 揭示OOD任务上模型泛化被高估的评估框架
tldr: 该文关注蛋白质结合亲和力预测，指出常用随机交叉验证评估协议会高估模型真实泛化能力。作者提出HAIPR统一开源框架，整合训练、优化与推理流程，并引入更贴近真实分布的划分协议。实验表明随机交叉验证会显著高估OOD任务性能，提醒研究者重视评估协议对泛化结论的影响。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 亲和力预测常用随机交叉验证评估，可能高估模型在OOD任务上的真实泛化能力。
method: 提出HAIPR统一框架，整合训练优化推理流程并引入真实数据划分协议。
result: 实验表明随机交叉验证显著高估OOD任务性能。
conclusion: 合理评估协议对判断模型泛化至关重要。
---

## Abstract
Accurate prediction of protein binding affinity is key for drug discovery and protein engineering, but commonly used evaluation protocols like Random Cross-Validation (RandomCV) can misrepresent true model generalization. We present HAIPR, a unified, open-source framework that streamlines the full machine learning pipeline for affinity prediction from training and optimization to inference, with curated benchmark datasets and robust, biologically meaningful evaluation protocols. By extending the BindingGYM benchmark and introducing realistic data splits, HAIPR reveals that RandomCV substantially overestimates model performance on out-of-distribution tasks. We systematically compare Support Vector Regression (SVR) using protein language model (pLM) embeddings to parameter-efficient fine-tuning (PEFT) of pLMs. SVR shows competitive results and increased stability in data-scarce scenarios, while PEFT excels as datasets grow larger and tasks become more complex. Analysis of model input setups shows that incorporating structural information does not always improve, and may sometimes hinder, performance for practical affinity prediction. Finally, we determine the lower limits of data required for reliable prediction, finding that even compact models can achieve performance close to the reproducibility limit of state-of-the-art assays, a practical ceiling for computational prediction. Code and pre-computed embeddings are publicly available.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
揭示OOD任务上模型泛化被高估的评估框架。

### 2. 核心内容
该文关注蛋白质结合亲和力预测，指出常用随机交叉验证评估协议会高估模型真实泛化能力。作者提出HAIPR统一开源框架，整合训练、优化与推理流程，并引入更贴近真实分布的划分协议。实验表明随机交叉验证会显著高估OOD任务性能，提醒研究者重视评估协议对泛化结论的影响。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=6cHUf3Dnxr](https://openreview.net/forum?id=6cHUf3Dnxr)
