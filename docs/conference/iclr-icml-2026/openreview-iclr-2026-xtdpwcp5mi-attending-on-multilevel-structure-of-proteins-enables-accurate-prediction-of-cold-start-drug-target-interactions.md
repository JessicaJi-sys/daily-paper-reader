---
title: Attending on Multilevel Structure of Proteins enables Accurate Prediction of Cold-Start Drug-Target Interactions
title_zh: 关注蛋白质多级结构实现准确的冷启动药物-靶标相互作用预测
authors: "Ziying Zhang, Yaqing Wang, Yuxuan Sun, Min Ye, Quanming Yao"
date: 2025-09-20
pdf: "https://openreview.net/pdf?id=xtdPwCp5mi"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 面向新药的冷启动药物-靶标相互作用预测
tldr: 冷启动药物-靶标相互作用预测旨在刻画新药与蛋白的相互作用，但既有方法仅用一级结构表示蛋白，难以捕捉高层结构信息。作者提出ColdDTI，通过层次化注意力机制挖掘多级蛋白结构与药物的交互。实验表明该框架提升了新药场景下的相互作用预测精度，为冷启动药物建模提供了多级结构视角。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 冷启动DTI预测中既有方法仅用蛋白一级结构，忽略多级结构对相互作用的影响。
method: 提出ColdDTI，用层次化注意力机制建模蛋白多级结构与药物的交互。
result: 在新药冷启动场景下提升了药物-靶标相互作用预测精度。
conclusion: 表明多级结构建模对冷启动药物预测有效，可迁移至冷启动DDI。
---

## Abstract
Cold-start drug-target interaction (DTI) prediction focuses on interaction between novel drugs and proteins.
Previous methods typically learn transferable interaction patterns between structures of drug and proteins to tackle it.
However, insight from proteomics suggest that protein have multi-level structures and they all influence the DTI.
Existing works usually represent protein with only primary structures, limiting their ability to capture interactions involving higher-level structures. 
Inspired by this insight, we propose ColdDTI, a framework attending on protein multi-level structure for cold-start DTI prediction.
We employ hierarchical attention mechanism to mine interaction between multi-level protein structures (from primary to quaternary) and drug structures at both local and global granularities.
Then, we leverage mined interactions to fuse structure representations of different levels for final prediction.
Our design captures biologically transferable priors, avoiding the risk of overfitting caused by excessive reliance on representation learning.
Experiments on benchmark datasets demonstrate that ColdDTI consistently outperforms previous methods in cold-start settings.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向新药的冷启动药物-靶标相互作用预测。

### 2. 核心内容
冷启动药物-靶标相互作用预测旨在刻画新药与蛋白的相互作用，但既有方法仅用一级结构表示蛋白，难以捕捉高层结构信息。作者提出ColdDTI，通过层次化注意力机制挖掘多级蛋白结构与药物的交互。实验表明该框架提升了新药场景下的相互作用预测精度，为冷启动药物建模提供了多级结构视角。

### 3. 对应检索需求
cold-start drug-drug interaction prediction for unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=xtdPwCp5mi](https://openreview.net/forum?id=xtdPwCp5mi)
