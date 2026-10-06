---
title: "GRAM-DTI: Adaptive Multimodal Representation Learning for Drug–Target Interaction Prediction"
title_zh: GRAM-DTI：面向药物-靶点相互作用预测的自适应多模态表示学习
authors: "Feng Jiang, Amina Mollaysa, Hehuan Ma, Yuzhi Guo, Tommaso Mansi, Junzhou Huang, Mangal Prakash, Rui Liao"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=dbZeLxOCIs"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 面向DTI预测的自适应多模态表示
tldr: 药物-靶点相互作用预测是药物发现基石，但现有方法多仅用SMILES-蛋白对，未充分利用多模态信息。本文提出GRAM-DTI预训练框架，将小分子与蛋白的多模态输入整合为统一表示，并把体积对比学习扩展到四种模态以捕捉高阶语义对齐。该框架处理模态缺失等问题，为异构多源知识融合的DTI预测提供可迁移思路，但与药物对级MoE路由关系有限。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有DTI方法多依赖SMILES-蛋白对，未充分利用小分子与蛋白的丰富多模态信息。
method: 提出GRAM-DTI预训练框架，整合多模态分子与蛋白输入并将对比学习扩展到四模态。
result: 该框架捕捉高阶语义对齐并提升DTI预测的表示能力。
conclusion: 为异构多源知识融合的DTI建模提供了自适应多模态方案。
---

## Abstract
Drug target interaction (DTI) prediction is a cornerstone of computational drug discovery, enabling rational design, repurposing, and mechanistic insights. While deep learning has advanced DTI modeling, existing approaches primarily rely on SMILES–protein pairs and fail to exploit the rich multimodal information available for small molecules and proteins. Inspired by recent successes in multimodal molecular property prediction, we introduce GRAM-DTI, a pre-training framework that integrates multimodal small molecule and protein inputs into a unified representation. GRAM-DTI extends volume-based contrastive learning to four modalities, capturing higher-order semantic alignment beyond conventional pairwise approaches. To handle modality informativeness, we propose adaptive modality dropout, dynamically regulating each modality’s contribution during pretraining. Additionally, IC50 activity measurements, when available, are incorporated as weak supervision to ground representations in biologically meaningful interaction strengths. Experiments on four publicly available datasets demonstrate that GRAM-DTI consistently outperforms state-of-the-art baselines. Our results highlight the benefits of higher-order multimodal alignment, adaptive modality utilization, and auxiliary supervision for robust and generalizable DTI prediction. Our code is available at https://github.com/uta-smile/GRAM-DTI.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向DTI预测的自适应多模态表示。

### 2. 核心内容
药物-靶点相互作用预测是药物发现基石，但现有方法多仅用SMILES-蛋白对，未充分利用多模态信息。本文提出GRAM-DTI预训练框架，将小分子与蛋白的多模态输入整合为统一表示，并把体积对比学习扩展到四种模态以捕捉高阶语义对齐。该框架处理模态缺失等问题，为异构多源知识融合的DTI预测提供可迁移思路，但与药物对级MoE路由关系有限。

### 3. 对应检索需求
How can models dynamically adapt knowledge integration strategies to different drug pairs when heterogeneous knowledge sources contribute unequally across instances?

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=dbZeLxOCIs](https://openreview.net/forum?id=dbZeLxOCIs)
