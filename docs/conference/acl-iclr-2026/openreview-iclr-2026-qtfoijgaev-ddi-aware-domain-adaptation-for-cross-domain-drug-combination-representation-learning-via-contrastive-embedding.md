---
title: DDI-Aware Domain Adaptation for Cross-Domain Drug Combination Representation Learning via Contrastive Embedding
title_zh: 基于对比嵌入的DDI感知跨域药物组合表示学习
authors: "Ellen Yi-Ge, Taric Chen, Heng Huang"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=QtFOIJGAEv"
tags: ["query:ood-inv"]
score: 8.0
evidence: 分布偏移下DDI感知的跨域药物组合表示学习
tldr: 该文关注组合疗法中药物相互作用表示学习在分布偏移下的困难，指出已有方法只对齐边缘分布而忽视应跨域保留的成对交互结构。作者提出DDI感知的域适应框架，用对比嵌入将群体级耦合目标与可处理的映射级替代目标分离。该工作把DDI结构融入域适应对齐视角，为跨域药物组合表示学习提供了更保守且完整的方案。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 组合疗法中DDI表示学习在分布偏移下困难，已有方法只对齐边缘分布忽视成对交互结构。
method: 提出DDI感知的域适应框架，用对比嵌入分离群体级耦合目标与映射级替代目标。
result: 框架在跨域设置下保留DDI交互结构并提升表示学习效果。
conclusion: 将DDI结构融入域适应对齐可更好应对分布偏移。
---

## Abstract
Drug–drug interaction (DDI)–aware representation learning for combination therapy remains challenging under distribution shift: prevailing approaches tend to align marginals while neglecting the pairwise interaction structure that should be preserved across domains. We address these gaps with a DDI-aware, domain-adaptation–style framework that cleanly separates a population-level coupling objective from a tractable map-level surrogate. We present a conservative and fully specified framework integrating drug-drug interaction (DDI) structure into a domain-adaptation-style (DA-style) alignment view for association combination representation learning. Our composition has two purposely separated layers. In the paper coupling layer we add to classical optimal transport (OT) a structure-preserving DDI penalty that induces congruency between pairwise interaction structure between domains and we prove the existence of minimizers under standard measure theoretic conditions, without making any claims on determinism of the maps, called Monge maps. Under Dutch map layer and locally Lipschitz map layer and linear growth global well-posedness of induced preconditioned descent in map layer energy monotonicity is stated only under an explicit optional assumption of monotonicity of preconditioner not covering adaptive optimizers such as Adam. We present so-called Eulerian (continuity equation) view for help in interpretation but with clear indication of the scope of rigor. Empirically, we utilize the TWOSIDES proxy dataset to investigate whether DDI-aware pretraining will lead to better interaction-aware feature learning through the use of a proxy data-set (adverse-interaction). We emphasize that adverse DDI labels are not clinical non-synergy but conclusions are limited to the proxy discrimination task. On a variety of graph backbones and embedding baselines, supervised contrastive learning (SCL) with DA-style marginal alignment approaches leads to improvements in terms of Accuracy and Precision with competitive Recall.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布偏移下DDI感知的跨域药物组合表示学习。

### 2. 核心内容
该文关注组合疗法中药物相互作用表示学习在分布偏移下的困难，指出已有方法只对齐边缘分布而忽视应跨域保留的成对交互结构。作者提出DDI感知的域适应框架，用对比嵌入将群体级耦合目标与可处理的映射级替代目标分离。该工作把DDI结构融入域适应对齐视角，为跨域药物组合表示学习提供了更保守且完整的方案。

### 3. 对应检索需求
cold-start drug-drug interaction event prediction with unseen drugs。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=QtFOIJGAEv](https://openreview.net/forum?id=QtFOIJGAEv)
