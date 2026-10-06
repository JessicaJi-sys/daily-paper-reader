---
title: "Drug-ProGO: A Gene Ontology-Enhanced Contrastive Learning Framework for Drug Virtual Screening with Multi-modality Whole-Protein Input"
title_zh: Drug-ProGO：面向多模态全蛋白输入药物虚拟筛选的基因本体增强对比学习框架
authors: "Ao Shen, Mingzhi Yuan, Qiao Huang, Bin Feng, Jie Du, Yingfan MA, Manning Wang"
date: 2025-09-15
pdf: "https://openreview.net/pdf?id=fz1Gnrv9Wx"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 通过GO增强对比学习泛化到未见蛋白
tldr: 虚拟筛选多依赖已知结合口袋，蛋白质层面筛选在口袋信息缺失时更具价值但泛化困难。本文提出Drug-ProGO，一种基因本体增强的对比学习框架，训练中融入GO信息以丰富蛋白表示。模型借此捕捉新蛋白与已知蛋白的功能相似性，从而更好泛化到未见蛋白。该工作为冷启动场景下对未见对象的泛化提供了可迁移思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 多数虚拟筛选依赖已知结合口袋，蛋白质层面筛选在口袋信息缺失时泛化能力不足。
method: 提出Drug-ProGO，在对比学习中融入基因本体信息以丰富蛋白表示。
result: 模型通过捕捉新蛋白与已知蛋白的功能相似性，更好泛化到未见蛋白。
conclusion: 该框架为未见对象泛化的冷启动筛选提供了有效表征学习范式。
---

## Abstract
Virtual screening plays a crucial role in accelerating early-stage drug discovery by efficiently identifying promising small molecule candidates. While most existing methods depend on known binding pockets, protein-level virtual screening has recently gained attention due to its broader applicability in scenarios where pocket information is incomplete or unavailable. In this work, we propose Drug-ProGO, a Gene Ontology (GO) enhanced contrastive learning framework that integrates GO information during training to enrich protein representations, enabling the model to generalize better to unseen proteins by capturing their functional similarity to known ones. This enables the model to better infer compatibility between novel proteins and small molecules. Our framework supports flexible protein inputs, including sequence, structure, and their combination. In the dual-modality setting, the two modalities are processed independently, and their prediction scores are fused using an uncertainty-aware fusion mechanism without additional trainable parameters. Extensive experiments across four virtual screening benchmarks and input settings demonstrate that incorporating GO knowledge consistently improves performance, highlighting the importance of functional knowledge integration for protein-level virtual screening.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过GO增强对比学习泛化到未见蛋白。

### 2. 核心内容
虚拟筛选多依赖已知结合口袋，蛋白质层面筛选在口袋信息缺失时更具价值但泛化困难。本文提出Drug-ProGO，一种基因本体增强的对比学习框架，训练中融入GO信息以丰富蛋白表示。模型借此捕捉新蛋白与已知蛋白的功能相似性，从而更好泛化到未见蛋白。该工作为冷启动场景下对未见对象的泛化提供了可迁移思路。

### 3. 对应检索需求
cold-start drug-drug interaction prediction for unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=fz1Gnrv9Wx](https://openreview.net/forum?id=fz1Gnrv9Wx)
