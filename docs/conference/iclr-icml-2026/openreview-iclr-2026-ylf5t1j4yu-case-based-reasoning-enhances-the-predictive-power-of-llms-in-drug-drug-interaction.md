---
title: Case-Based Reasoning Enhances the Predictive Power of LLMs in Drug-Drug Interaction
title_zh: 案例推理增强大语言模型在药物-药物相互作用中的预测能力
authors: "Guangyi Liu, Yongqi Zhang, Xunyuan Liu, Quanming Yao"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Ylf5t1j4Yu"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 结合 GNN 与 LLM 的案例推理用于药物-药物相互作用预测
tldr: 药物-药物相互作用预测对用药安全至关重要，但大语言模型在 DDI 任务上效果仍受限。本文提出 CBR-DDI，借鉴临床案例推理，用 LLM 抽取药理洞见、GNN 建模药物关联以构建知识库，并采用混合检索与两级知识增强提示。实验表明从历史案例蒸馏药理模式可增强 LLM 推理，提升 DDI 预测的准确性与可靠性。其贡献在于把案例推理与多源知识整合引入 DDI 预测。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: DDI 预测对治疗安全至关重要，但大语言模型在 DDI 任务上的效果仍面临挑战。
method: 提出 CBR-DDI，用 LLM 抽取药理洞见、GNN 建模药物关联构建知识库，并采用混合检索与两级知识增强提示。
result: 通过从历史案例中蒸馏药理模式来增强 LLM 推理，提升了 DDI 预测的准确性与可靠性。
conclusion: 表明案例推理与多源知识整合可有效提升 DDI 预测，为安全用药提供支持。
---

## Abstract
Drug–drug interaction (DDI) prediction is critical for treatment safety. While large language models (LLMs) show promise in pharmaceutical tasks, their effectiveness in DDI prediction remains challenging. Inspired by the well-established clinical practice where physicians routinely reference similar historical cases to guide their decisions through case-based reasoning (CBR), we propose CBR-DDI, a novel framework that distills pharmacological patterns from historical cases to improve LLM reasoning for DDI tasks. CBR-DDI constructs a knowledge repository by leveraging LLMs to extract pharmacological insights and graph neural networks (GNNs) to model drug associations. A hybrid retrieval mechanism and two-tier knowledge-enhanced prompting allow LLMs to effectively retrieve and reuse relevant cases. We further introduce a representative sampling strategy for dynamic case refinement. Extensive experiments demonstrate that CBR-DDI achieves state-of-the-art performance, with a significant 28.7% accuracy improvement over both popular LLMs and CBR baseline, while maintaining high interpretability and flexibility.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
结合 GNN 与 LLM 的案例推理用于药物-药物相互作用预测。

### 2. 核心内容
药物-药物相互作用预测对用药安全至关重要，但大语言模型在 DDI 任务上效果仍受限。本文提出 CBR-DDI，借鉴临床案例推理，用 LLM 抽取药理洞见、GNN 建模药物关联以构建知识库，并采用混合检索与两级知识增强提示。实验表明从历史案例蒸馏药理模式可增强 LLM 推理，提升 DDI 预测的准确性与可靠性。其贡献在于把案例推理与多源知识整合引入 DDI 预测。

### 3. 对应检索需求
cold-start drug-drug interaction prediction for unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=Ylf5t1j4Yu](https://openreview.net/forum?id=Ylf5t1j4Yu)
