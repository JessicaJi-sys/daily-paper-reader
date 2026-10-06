---
title: DDI-Aware Domain Adaptation for Cross-Domain Drug Combination Representation Learning via Contrastive Embedding
title_zh: DDI感知的域适应：基于对比嵌入的跨域药物组合表征学习
authors: "Ellen Yi-Ge, Taric Chen, Heng Huang"
date: 2025-09-17
pdf: "https://openreview.net/pdf?id=QtFOIJGAEv"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 分布偏移下DDI感知的药物组合域适应表征学习
tldr: 针对药物组合表征学习在分布偏移下困难、现有方法只对齐边缘分布而忽略应跨域保留的成对交互结构的问题，本文提出DDI感知的域适应框架。该方法将总体层面的耦合目标与可处理的映射级代理分离，用对比嵌入将药物-药物交互结构融入域适应式对齐。实验表明该框架在跨域药物组合表征中保留DDI结构并缓解分布偏移，提升组合学习效果。研究强调成对交互结构在域适应中的重要性，直接服务于DDI与分布外泛化主题。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 分布偏移下药物组合表征学习困难，现有方法仅对齐边缘分布而忽略应跨域保留的成对交互结构。
method: 提出DDI感知域适应框架，分离总体耦合目标与映射级代理，用对比嵌入对齐并保留DDI结构。
result: 在跨域药物组合表征中保留药物-药物交互结构、缓解分布偏移，提升组合学习表现。
conclusion: 强调成对交互结构在域适应中的关键作用，直接服务于DDI与分布外泛化的研究目标。
---

## Abstract
Drug–drug interaction (DDI)–aware representation learning for combination therapy remains challenging under distribution shift: prevailing approaches tend to align marginals while neglecting the pairwise interaction structure that should be preserved across domains. We address these gaps with a DDI-aware, domain-adaptation–style framework that cleanly separates a population-level coupling objective from a tractable map-level surrogate. We present a conservative and fully specified framework integrating drug-drug interaction (DDI) structure into a domain-adaptation-style (DA-style) alignment view for association combination representation learning. Our composition has two purposely separated layers. In the paper coupling layer we add to classical optimal transport (OT) a structure-preserving DDI penalty that induces congruency between pairwise interaction structure between domains and we prove the existence of minimizers under standard measure theoretic conditions, without making any claims on determinism of the maps, called Monge maps. Under Dutch map layer and locally Lipschitz map layer and linear growth global well-posedness of induced preconditioned descent in map layer energy monotonicity is stated only under an explicit optional assumption of monotonicity of preconditioner not covering adaptive optimizers such as Adam. We present so-called Eulerian (continuity equation) view for help in interpretation but with clear indication of the scope of rigor. Empirically, we utilize the TWOSIDES proxy dataset to investigate whether DDI-aware pretraining will lead to better interaction-aware feature learning through the use of a proxy data-set (adverse-interaction). We emphasize that adverse DDI labels are not clinical non-synergy but conclusions are limited to the proxy discrimination task. On a variety of graph backbones and embedding baselines, supervised contrastive learning (SCL) with DA-style marginal alignment approaches leads to improvements in terms of Accuracy and Precision with competitive Recall.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布偏移下DDI感知的药物组合域适应表征学习。

### 2. 核心内容
针对药物组合表征学习在分布偏移下困难、现有方法只对齐边缘分布而忽略应跨域保留的成对交互结构的问题，本文提出DDI感知的域适应框架。该方法将总体层面的耦合目标与可处理的映射级代理分离，用对比嵌入将药物-药物交互结构融入域适应式对齐。实验表明该框架在跨域药物组合表征中保留DDI结构并缓解分布偏移，提升组合学习效果。研究强调成对交互结构在域适应中的重要性，直接服务于DDI与分布外泛化主题。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=QtFOIJGAEv](https://openreview.net/forum?id=QtFOIJGAEv)
