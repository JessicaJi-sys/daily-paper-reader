---
title: "NCGAMI: Domain-Adaptive Drug-Target Interaction Prediction with Graph and Sequence Models"
title_zh: NCGAMI：基于图与序列模型的域自适应药物-靶点相互作用预测
authors: "Ellen Yi-Ge, Taric Chen"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=lO1BLLh8K8"
tags: ["query:ood-inv"]
score: 6.0
evidence: 分布偏移下的域自适应药物相互作用预测
tldr: 针对药物-靶点相互作用预测在化学骨架或蛋白家族等分布偏移下鲁棒性不足的问题，本文提出NCGAMI，在图与序列编码器融合下采用无监督域适应范式，通过源域风险、跨域表示对齐与目标域条件熵正则三项目标训练。实验表明该无标签目标能提升分布偏移下的预测鲁棒性，为药物相互作用OOD泛化提供参考。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 药物-靶点相互作用预测在化学骨架或蛋白家族等分布偏移下鲁棒性不足。
method: 提出NCGAMI，融合图与序列编码器，用源域风险、跨域对齐与条件熵正则训练。
result: 实验表明该无标签目标提升了分布偏移下的预测鲁棒性。
conclusion: 为药物相互作用预测的OOD泛化提供了域适应思路。
---

## Abstract
Drug-target interaction (DTI) prediction is of central importance in computational pharmacology, but how robust these predictions are in the face of distribution shift (e.g. between chemical scaffolds, or protein families) remains challenging. We introduce a well-behaved, label-free objective and encoder fusion recipe for DTI, which is referred to as NCGAMI, under an unsupervised domain adaptation (UDA) training paradigm. NCGAMI only uses a graph encoder for the drug molecule graph and a sequence encoder for the proteins, and uses a three-term objective, consisting of (i) the supervised source-domain risk, (ii) an explicit cross-domain representation alignment, and (iii) regularization of the target domain through conditional-entropy minimization and prediction-consistency. The implementation is possible without using target labels. Throughout, we take great care to avoid using target labels during training and to clarify situations where there may be overlap between source and target entities. Using two widely used DTI datasets (Human and DrugBank), and using a protocol (random split) that we applied strictly for feasibility check, NCGAMI achieves good AUC/AUPR and is competitive against representative baselines. On Human our model achieves AUC 0.895 and AUPR 0.852 on Drugbank our model achieves AUC 0.733 and AUPR 0.675. Ablations can be seen to contribute the graph encoder, sequence encoder, and UDA regularization. We also incorporate non-operational geometric background so that theoretical assertion is motivating in your choice of design without overwhelming you with strong theoretical claims.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布偏移下的域自适应药物相互作用预测。

### 2. 核心内容
针对药物-靶点相互作用预测在化学骨架或蛋白家族等分布偏移下鲁棒性不足的问题，本文提出NCGAMI，在图与序列编码器融合下采用无监督域适应范式，通过源域风险、跨域表示对齐与目标域条件熵正则三项目标训练。实验表明该无标签目标能提升分布偏移下的预测鲁棒性，为药物相互作用OOD泛化提供参考。

### 3. 对应检索需求
research on out of distribution generalization and invariant representation learning for cold start drug drug interaction prediction。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=lO1BLLh8K8](https://openreview.net/forum?id=lO1BLLh8K8)
