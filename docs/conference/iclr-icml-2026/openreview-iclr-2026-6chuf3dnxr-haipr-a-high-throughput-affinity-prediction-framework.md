---
title: "HAIPR: A High-Throughput Affinity Prediction Framework"
title_zh: HAIPR：高通量亲和力预测框架
authors: "Jannis de Riz, Tom U. Schlegel, Jens Meiler, Torben Schiffner"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=6cHUf3Dnxr"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 分布偏移下亲和力预测的现实分布外评估
tldr: 该文指出随机交叉验证等常用评估协议会高估模型的真实泛化能力，尤其在药物发现的亲和力预测中。作者提出HAIPR统一开源框架，覆盖训练、优化到推理全流程，并引入更贴近现实的数据划分与生物学评估协议。实验揭示随机交叉验证显著高估分布外性能，为药物级分布外泛化的严格评估提供了重要工具与警示。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 随机交叉验证等协议会高估模型在分布外任务上的真实泛化能力。
method: 提出HAIPR统一框架，整合全流程管线并引入现实数据划分与评估协议。
result: 实验表明随机交叉验证显著高估分布外亲和力预测性能。
conclusion: 为药物级分布外泛化的严格评估提供了工具与方法论警示。
---

## Abstract
Accurate prediction of protein binding affinity is key for drug discovery and protein engineering, but commonly used evaluation protocols like Random Cross-Validation (RandomCV) can misrepresent true model generalization. We present HAIPR, a unified, open-source framework that streamlines the full machine learning pipeline for affinity prediction from training and optimization to inference, with curated benchmark datasets and robust, biologically meaningful evaluation protocols. By extending the BindingGYM benchmark and introducing realistic data splits, HAIPR reveals that RandomCV substantially overestimates model performance on out-of-distribution tasks. We systematically compare Support Vector Regression (SVR) using protein language model (pLM) embeddings to parameter-efficient fine-tuning (PEFT) of pLMs. SVR shows competitive results and increased stability in data-scarce scenarios, while PEFT excels as datasets grow larger and tasks become more complex. Analysis of model input setups shows that incorporating structural information does not always improve, and may sometimes hinder, performance for practical affinity prediction. Finally, we determine the lower limits of data required for reliable prediction, finding that even compact models can achieve performance close to the reproducibility limit of state-of-the-art assays, a practical ceiling for computational prediction. Code and pre-computed embeddings are publicly available.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布偏移下亲和力预测的现实分布外评估。

### 2. 核心内容
该文指出随机交叉验证等常用评估协议会高估模型的真实泛化能力，尤其在药物发现的亲和力预测中。作者提出HAIPR统一开源框架，覆盖训练、优化到推理全流程，并引入更贴近现实的数据划分与生物学评估协议。实验揭示随机交叉验证显著高估分布外性能，为药物级分布外泛化的严格评估提供了重要工具与警示。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=6cHUf3Dnxr](https://openreview.net/forum?id=6cHUf3Dnxr)
