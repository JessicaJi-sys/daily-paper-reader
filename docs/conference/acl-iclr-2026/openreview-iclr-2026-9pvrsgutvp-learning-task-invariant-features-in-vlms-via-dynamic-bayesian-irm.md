---
title: Learning Task-Invariant Features in VLMs via Dynamic Bayesian IRM
title_zh: 通过动态贝叶斯 IRM 学习视觉语言模型中的任务不变特征
authors: "Sergey Sharkov, Ivan Bondarenko"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=9pVrsGUTvp"
tags: ["query:ood-inv"]
score: 8.0
evidence: 用贝叶斯 IRM 学习不变特征并缓解正则衰减
tldr: 针对视觉语言模型在分布偏移和未见 OOD 任务下性能下降、ERM 易依赖虚假相关而学不到任务不变特征的问题，本文把贝叶斯不变风险最小化（BIRM）迁移到生成式多模态场景。作者通过任务类型（如 VQA、描述、OCR）形式化环境，把分布偏移视为任务间迁移，从而缓解深层网络中的正则化衰减。该工作为在缺少显式环境标签设定下学习不变特征提供了新的贝叶斯途径，与不变表征学习需求紧密相关。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: VLM 在分布偏移下依赖虚假相关，ERM 难以学到任务不变特征，且 IRM 存在正则衰减。
method: 将贝叶斯 IRM 适配到生成式 VLM，用任务类型形式化环境以刻画分布偏移。
result: 该方法缓解了深层网络正则化衰减，提升了任务不变特征的习得能力。
conclusion: 为多模态场景下的不变特征学习提供了贝叶斯 IRM 新范式。
---

## Abstract
While Visual Language Models (VLMs) excel on multimodal tasks, they suffer from performance degradation under distribution shift, particularly when facing out-of-distribution (OOD) tasks not seen during training. Traditional Empirical Risk Minimization (ERM) often fails to learn task-invariant features, relying instead on spurious correlations. Although Invariant Risk Minimization (IRM) offers a solution, its application to generative multimodal settings remains unexplored, and it suffers from regularization decay in deep networks.

We bridge this gap by adapting Bayesian IRM (BIRM) for generative VLMs. We formalize "environments" in multimodal data through task types (e.g., VQA, Captioning, OCR), treating distribution shift as a shift between tasks. To address regularization decay, we propose Dynamic BIRM — an algorithm that adaptively adjusts the invariance penalty strength throughout training, maintaining an optimal balance between empirical and invariant risk.

Our experiments on the LLaVA-OneVision dataset with SmolVLM-2B demonstrate that Dynamic BIRM significantly outperforms ERM and static BIRM baselines, achieving a +33.8\% absolute improvement in CEE score (a comprehensive LLM-based evaluation metric) on challenging OOD OCR tasks while maintaining or improving in-domain performance. Our analysis reveals that adaptive mitigation of regularization decay is key to learning truly task-invariant features, leading to substantial robustness against task-based distribution shifts. Code and models will be released.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用贝叶斯 IRM 学习不变特征并缓解正则衰减。

### 2. 核心内容
针对视觉语言模型在分布偏移和未见 OOD 任务下性能下降、ERM 易依赖虚假相关而学不到任务不变特征的问题，本文把贝叶斯不变风险最小化（BIRM）迁移到生成式多模态场景。作者通过任务类型（如 VQA、描述、OCR）形式化环境，把分布偏移视为任务间迁移，从而缓解深层网络中的正则化衰减。该工作为在缺少显式环境标签设定下学习不变特征提供了新的贝叶斯途径，与不变表征学习需求紧密相关。

### 3. 对应检索需求
invariant representation learning without explicit environment labels。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=9pVrsGUTvp](https://openreview.net/forum?id=9pVrsGUTvp)
