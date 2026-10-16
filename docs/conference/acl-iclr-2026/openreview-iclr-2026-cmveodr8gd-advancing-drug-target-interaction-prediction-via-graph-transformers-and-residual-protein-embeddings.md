---
title: Advancing Drug-Target Interaction Prediction via Graph Transformers and Residual Protein Embeddings
title_zh: 通过图Transformer与残差蛋白质嵌入推进药物-靶点相互作用预测
authors: "Ellen Yi-Ge, Taric Chen, Heng Huang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=CmvEOdr8gD"
tags: ["query:ood-inv"]
score: 5.0
evidence: 面向域偏移的鲁棒预测与风险迁移控制
tldr: 该文针对药物-靶点相互作用预测依赖标注数据、训练与不透明对齐损失耦合导致鲁棒性难审计的问题，提出域偏移感知预测器MoleProLink，融合最优传输、再生核嵌入与信息几何思想，并在Wasserstein-1等假设下给出紧凑的风险迁移控制。方法提升了对分布偏移的稳健性与可诊断性，为冷启动DDI场景中的域偏移建模提供了可迁移的鲁棒学习思路。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 现有药物-靶点相互作用预测多依赖标注数据或与不透明对齐损失耦合，导致鲁棒性难审计。
method: 提出域偏移感知的MoleProLink，融合最优传输、再生核嵌入与信息几何并给出风险迁移控制。
result: 在Wasserstein-1等假设下建立紧凑的风险迁移界，提升分布偏移下的稳健性与可诊断性。
conclusion: 为域偏移下的鲁棒预测提供了可迁移的学习思路。
---

## Abstract
Predicting drug-target interactions (DTIs) is important for the acceleration of drug discovery. Prevailing approaches often assume access to labeled target data or entangle training with opaque unsupervised alignment losses, which makes robustness hard to audit and failure modes difficult to diagnose. To address these gaps, we propose MoleProLink, a domain-shift-aware predictor of DTI for mining bioactive molecules which is based on the integration of methods inspired by measure-theoretic optimal transport, reproducing-kernel embeddings, and information-geometric perspectives. On the theory side, we present two compact risk-transfer control under the following two explicit assumptions: (i) Wasserstein-1 control under Lipschitz regularity assumption of the composed loss, and (ii) RKHS control with Maximum Mean Discrepancy (MMD). These statements are standard IPM-style bounds that are included here in a DTI-specific notation, we use them to motivate diagnostics and feature designing principles not to make any new forward inequalities. On the methodology side, we use a graph Transformer model for molecular graph with a sequence encoder for proteins. Protein embedding is performed with a residue based embedding (named as Residue2vec) and a bi-directional state space model, whereas molecular embedding is achieved through centrality and spatial encodings in a state space model Graph Transformer. Experimental results on three popular benchmarks (Human, C.elegans and Davis) show our method achieving strong AUC/AUPR, using a single protocol. Compared to the baselines, gains are achieved under the same data processing and negative-sampling; these margins are regarded not as inferential statements, but rather, as descriptive. We give implementation details that are sufficient for direct replication, and reproduce the ablative experiments that isolate the contributions of the protein sequence encoder and interaction decoder.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向域偏移的鲁棒预测与风险迁移控制。

### 2. 核心内容
该文针对药物-靶点相互作用预测依赖标注数据、训练与不透明对齐损失耦合导致鲁棒性难审计的问题，提出域偏移感知预测器MoleProLink，融合最优传输、再生核嵌入与信息几何思想，并在Wasserstein-1等假设下给出紧凑的风险迁移控制。方法提升了对分布偏移的稳健性与可诊断性，为冷启动DDI场景中的域偏移建模提供了可迁移的鲁棒学习思路。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=CmvEOdr8gD](https://openreview.net/forum?id=CmvEOdr8gD)
