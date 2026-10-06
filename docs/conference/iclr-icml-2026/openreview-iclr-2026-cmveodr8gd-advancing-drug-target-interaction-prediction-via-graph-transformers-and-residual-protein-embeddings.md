---
title: Advancing Drug-Target Interaction Prediction via Graph Transformers and Residual Protein Embeddings
title_zh: 基于图Transformer与残差蛋白嵌入推进药物-靶标相互作用预测
authors: "Ellen Yi-Ge, Taric Chen, Heng Huang"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=CmvEOdr8gD"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 域漂移感知的药物-靶标相互作用预测与风险迁移控制
tldr: 药物-靶标相互作用预测方法常假设可获得标注靶标数据，并依赖不透明的对齐损失，导致鲁棒性难以审计。作者提出MoleProLink，一种域漂移感知的DTI预测器，融合最优传输、再生核嵌入与信息几何，并给出风险迁移控制的理论界限。该工作提升了分布漂移下的预测鲁棒性，为药物级分布外泛化提供了可审计的理论与方法支撑。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 既有DTI预测依赖标注靶标数据与不透明对齐损失，鲁棒性难以审计。
method: 提出MoleProLink，结合最优传输、核嵌入与信息几何实现域漂移感知预测。
result: 给出风险迁移控制理论界限，提升分布漂移下的鲁棒性。
conclusion: 为药物-靶标预测的分布外泛化提供可审计的理论与方法。
---

## Abstract
Predicting drug-target interactions (DTIs) is important for the acceleration of drug discovery. Prevailing approaches often assume access to labeled target data or entangle training with opaque unsupervised alignment losses, which makes robustness hard to audit and failure modes difficult to diagnose. To address these gaps, we propose MoleProLink, a domain-shift-aware predictor of DTI for mining bioactive molecules which is based on the integration of methods inspired by measure-theoretic optimal transport, reproducing-kernel embeddings, and information-geometric perspectives. On the theory side, we present two compact risk-transfer control under the following two explicit assumptions: (i) Wasserstein-1 control under Lipschitz regularity assumption of the composed loss, and (ii) RKHS control with Maximum Mean Discrepancy (MMD). These statements are standard IPM-style bounds that are included here in a DTI-specific notation, we use them to motivate diagnostics and feature designing principles not to make any new forward inequalities. On the methodology side, we use a graph Transformer model for molecular graph with a sequence encoder for proteins. Protein embedding is performed with a residue based embedding (named as Residue2vec) and a bi-directional state space model, whereas molecular embedding is achieved through centrality and spatial encodings in a state space model Graph Transformer. Experimental results on three popular benchmarks (Human, C.elegans and Davis) show our method achieving strong AUC/AUPR, using a single protocol. Compared to the baselines, gains are achieved under the same data processing and negative-sampling; these margins are regarded not as inferential statements, but rather, as descriptive. We give implementation details that are sufficient for direct replication, and reproduce the ablative experiments that isolate the contributions of the protein sequence encoder and interaction decoder.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
域漂移感知的药物-靶标相互作用预测与风险迁移控制。

### 2. 核心内容
药物-靶标相互作用预测方法常假设可获得标注靶标数据，并依赖不透明的对齐损失，导致鲁棒性难以审计。作者提出MoleProLink，一种域漂移感知的DTI预测器，融合最优传输、再生核嵌入与信息几何，并给出风险迁移控制的理论界限。该工作提升了分布漂移下的预测鲁棒性，为药物级分布外泛化提供了可审计的理论与方法支撑。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=CmvEOdr8gD](https://openreview.net/forum?id=CmvEOdr8gD)
