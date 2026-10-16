---
title: Case-Based Reasoning Enhances the Predictive Power of LLMs in Drug-Drug Interaction
title_zh: 案例推理增强大语言模型在药物相互作用中的预测能力
authors: "Guangyi Liu, Yongqi Zhang, Xunyuan Liu, Quanming Yao"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=Ylf5t1j4Yu"
tags: ["query:ood-inv"]
score: 4.0
evidence: 基于案例推理的药物相互作用预测
tldr: 针对大语言模型在药物相互作用预测中效果有限的问题，本文受临床医生参考相似历史病例的案例推理实践启发，提出CBR-DDI框架，利用LLM抽取药理知识并用图神经网络建模药物关联，构建知识库，再通过混合检索与两阶段知识增强提示提升推理能力。该设计将历史案例经验注入LLM推理流程。实验表明其在DDI任务上提升预测能力，但方法依赖LLM与案例检索，与不变表示学习关联较弱。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 大语言模型在药物相互作用预测上表现有限，需借助类似临床案例推理的经验来增强。
method: 提出CBR-DDI，用LLM抽取药理知识、GNN建模药物关联，并结合混合检索与知识增强提示。
result: 实验表明融合历史案例的推理能提升LLM在DDI预测任务上的表现。
conclusion: 展示了案例推理与知识增强提示对DDI预测的价值，但与不变学习方向关联有限。
---

## Abstract
Drug–drug interaction (DDI) prediction is critical for treatment safety. While large language models (LLMs) show promise in pharmaceutical tasks, their effectiveness in DDI prediction remains challenging. Inspired by the well-established clinical practice where physicians routinely reference similar historical cases to guide their decisions through case-based reasoning (CBR), we propose CBR-DDI, a novel framework that distills pharmacological patterns from historical cases to improve LLM reasoning for DDI tasks. CBR-DDI constructs a knowledge repository by leveraging LLMs to extract pharmacological insights and graph neural networks (GNNs) to model drug associations. A hybrid retrieval mechanism and two-tier knowledge-enhanced prompting allow LLMs to effectively retrieve and reuse relevant cases. We further introduce a representative sampling strategy for dynamic case refinement. Extensive experiments demonstrate that CBR-DDI achieves state-of-the-art performance, with a significant 28.7% accuracy improvement over both popular LLMs and CBR baseline, while maintaining high interpretability and flexibility.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于案例推理的药物相互作用预测。

### 2. 核心内容
针对大语言模型在药物相互作用预测中效果有限的问题，本文受临床医生参考相似历史病例的案例推理实践启发，提出CBR-DDI框架，利用LLM抽取药理知识并用图神经网络建模药物关联，构建知识库，再通过混合检索与两阶段知识增强提示提升推理能力。该设计将历史案例经验注入LLM推理流程。实验表明其在DDI任务上提升预测能力，但方法依赖LLM与案例检索，与不变表示学习关联较弱。

### 3. 对应检索需求
cold-start drug-drug interaction event prediction with unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=Ylf5t1j4Yu](https://openreview.net/forum?id=Ylf5t1j4Yu)
