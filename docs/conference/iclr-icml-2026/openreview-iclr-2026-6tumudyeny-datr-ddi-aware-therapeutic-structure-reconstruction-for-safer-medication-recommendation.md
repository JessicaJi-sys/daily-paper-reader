---
title: "DATR: DDI-Aware Therapeutic Structure Reconstruction for Safer Medication Recommendation"
title_zh: DATR：面向更安全用药推荐的DDI感知治疗结构重建
authors: "Jinke Feng, Wenjie Du, Yang Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=6tumuDYeny"
tags: ["query:ddi-moe"]
score: 5.0
evidence: DDI感知的药物结构与安全建模
tldr: 用药推荐系统需兼顾预测准确性与用药安全，尤其是避免药物相互作用。现有方法虽引入分子结构提升准确率，却忽视化学结构与治疗结果之间的语义鸿沟，且DDI缓解多为事后处理，难以主动预防。本文提出DDI感知治疗结构重建框架DATR，联合建模药物结构、治疗意图与安全画像。该框架以更前瞻的方式整合安全信息，为更安全的用药推荐提供支持。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 现有用药推荐忽视化学结构与治疗结果的语义鸿沟，且DDI缓解多为事后处理难以主动预防。
method: 提出DATR框架，联合建模药物分子结构、治疗意图与安全画像以实现DDI感知的结构重建。
result: 该方法将安全信息前置整合，提升了推荐中对药物相互作用的主动规避能力。
conclusion: 联合建模结构与安全画像有助于实现更安全、更准确的用药推荐。
---

## Abstract
Medication recommendation systems play a critical role in clinical decision support, where ensuring both predicting accuracy and safety, particularly drug-drug interaction (DDI) avoidance, is essential. While recent studies have explored drug molecular structures to enhance accuracy, they often overlook the semantic gap between chemical structures and therapeutic outcomes, leading to suboptimal recommendation. Moreover, existing DDI mitigation strategies typically operate in a post-hoc manner, limiting their ability to proactively prevent adverse interactions. In this work, we propose DDI-Aware therapeutic Structure Reconstruction (DATR), a novel framework that jointly models drug structures, therapeutic intent, and safety profiles. DATR conditionally encodes drug structures based on ATC-derived therapeutic labels, enabling intent-aware representation learning, and introduces a selectivity potential DDI constraint to proactively reduce interaction risk. Experiments on two real-world datasets and evaluations by clinical experts demonstrate that DATR achieves superior performance in recommendation accuracy and DDI reduction. Code is available at https://anonymous.4open.science/r/DATR-7EA8.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
DDI感知的药物结构与安全建模。

### 2. 核心内容
用药推荐系统需兼顾预测准确性与用药安全，尤其是避免药物相互作用。现有方法虽引入分子结构提升准确率，却忽视化学结构与治疗结果之间的语义鸿沟，且DDI缓解多为事后处理，难以主动预防。本文提出DDI感知治疗结构重建框架DATR，联合建模药物结构、治疗意图与安全画像。该框架以更前瞻的方式整合安全信息，为更安全的用药推荐提供支持。

### 3. 对应检索需求
cold-start drug-drug interaction prediction for unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=6tumuDYeny](https://openreview.net/forum?id=6tumuDYeny)
