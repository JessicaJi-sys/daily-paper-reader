---
title: Attending on Multilevel Structure of Proteins enables Accurate Prediction of Cold-Start Drug-Target Interactions
title_zh: 关注蛋白质多层次结构实现冷启动药物靶点相互作用的准确预测
authors: "Ziying Zhang, Yaqing Wang, Yuxuan Sun, Min Ye, Quanming Yao"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=xtdPwCp5mi"
tags: ["query:ood-inv"]
score: 6.0
evidence: 面向新药物的冷启动药物靶点相互作用
tldr: 针对冷启动药物靶点相互作用预测中新药物与蛋白缺乏已知交互、现有方法仅用一级结构表示蛋白而忽略多层次结构影响的问题，本文提出ColdDTI框架，采用层次化注意力机制挖掘多层级蛋白结构之间的交互关系。该设计从蛋白质组学视角补充了高阶结构信息。实验表明其在冷启动DTI预测上取得更准确的性能，为冷启动场景下（含未见药物）的关系预测提供了可借鉴的多层次建模思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 冷启动药物靶点预测面对新药物与蛋白，现有方法仅用一级结构表示蛋白，忽略多层次结构影响。
method: 提出ColdDTI，用层次化注意力机制挖掘多层级蛋白质结构之间的交互模式。
result: 实验表明融合多层次蛋白结构的框架在冷启动DTI预测上更准确。
conclusion: 为冷启动（含未见药物）场景的关系预测提供了多层次结构建模的有效范式。
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
面向新药物的冷启动药物靶点相互作用。

### 2. 核心内容
针对冷启动药物靶点相互作用预测中新药物与蛋白缺乏已知交互、现有方法仅用一级结构表示蛋白而忽略多层次结构影响的问题，本文提出ColdDTI框架，采用层次化注意力机制挖掘多层级蛋白结构之间的交互关系。该设计从蛋白质组学视角补充了高阶结构信息。实验表明其在冷启动DTI预测上取得更准确的性能，为冷启动场景下（含未见药物）的关系预测提供了可借鉴的多层次建模思路。

### 3. 对应检索需求
cold-start drug-drug interaction event prediction with unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=xtdPwCp5mi](https://openreview.net/forum?id=xtdPwCp5mi)
