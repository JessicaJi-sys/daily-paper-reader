---
title: "Disentangling Content from Style to Overcome Shortcut Learning: A Hybrid Generative-Discriminative Learning Framework"
title_zh: 解耦内容与风格以克服捷径学习：一种混合生成-判别学习框架
authors: "Siming Fu, Sijun Dong, Xiaoliang Meng"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=ReKTabN9US"
tags: ["query:ood-inv"]
score: 7.0
evidence: 解耦内容与风格以消除捷径/虚假特征并提升未见域泛化
tldr: 该文指出自监督学习在未见域上泛化差，根源在于模型依赖纹理等浅层特征形成捷径学习。作者提出HyGDL混合生成-判别框架，从学习机制层面将内容与风格解耦，而非仅在表层对齐或分离域特征。实验验证了该缺陷并显示解耦机制能有效缓解捷径依赖、提升未见域泛化，为鲁棒表示学习提供新思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 自监督学习泛化受捷径学习阻碍，模型依赖纹理等浅层特征而非内在结构。
method: 提出HyGDL混合生成-判别框架，从学习机制层面解耦内容与风格，而非仅表层对齐域特征。
result: 实验验证生成式与判别式方法均存在捷径缺陷，所提机制可缓解捷径依赖。
conclusion: 从根源改变学习机制可有效提升未见域泛化能力。
---

## Abstract
Despite the remarkable success of Self-Supervised Learning (SSL), its generalization is fundamentally hindered by Shortcut Learning, where models exploit superficial features like texture instead of intrinsic structure. We experimentally verify this flaw within the generative paradigm (e.g., MAE) and argue it is a systemic issue also affecting discriminative methods, identifying it as the root cause of their failure on unseen domains. While existing methods often tackle this at a surface level by aligning or separating domain-specific features, they fail to alter the underlying learning mechanism that fosters shortcut dependency.
To address this at its core, we propose HyGDL (Hybrid Generative-Discriminative Learning Framework), a hybrid framework that achieves explicit content-style disentanglement. Our approach is guided by the Invariance Pre-training Principle: forcing a model to learn an invariant essence by systematically varying a bias (e.g., style) at the input while keeping the supervision signal constant. HyGDL operates on a single encoder and analytically defines style as the component of a representation that is orthogonal to its style-invariant content, derived via vector projection. 
This is operationalized through a synergistic design: (1) a self-distillation objective learns a stable, style-invariant content direction; (2) an analytical projection then decomposes the representation into orthogonal content and style vectors; and (3) a style-conditioned reconstruction objective uses these vectors to restore the image, providing end-to-end supervision.
Unlike prior methods that rely on implicit heuristics, this principled disentanglement allows HyGDL to learn truly robust representations, demonstrating superior performance on benchmarks designed to diagnose shortcut learning.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
解耦内容与风格以消除捷径/虚假特征并提升未见域泛化。

### 2. 核心内容
该文指出自监督学习在未见域上泛化差，根源在于模型依赖纹理等浅层特征形成捷径学习。作者提出HyGDL混合生成-判别框架，从学习机制层面将内容与风格解耦，而非仅在表层对齐或分离域特征。实验验证了该缺陷并显示解耦机制能有效缓解捷径依赖、提升未见域泛化，为鲁棒表示学习提供新思路。

### 3. 对应检索需求
disentangling invariant features from variant or spurious features。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=ReKTabN9US](https://openreview.net/forum?id=ReKTabN9US)
