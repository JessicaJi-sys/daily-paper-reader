---
title: Class-Conditional Domain Alignment via Kernel Cauchy-Schwarz Mutual Information
title_zh: 基于核柯西-施瓦茨互信息的类条件域对齐
authors: "Ahmad Abdel-Qader, Anas Chaaban, Ahmed Mostafa Soliman Radwan, Omar Abdelaziz, Mahmoud Soliman, Mohamed S. Shehata"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=nGbdYCPlZw"
tags: ["query:ood-inv"]
score: 7.0
evidence: 通过类条件对齐学习跨域不变特征以实现域泛化
tldr: 针对域泛化中不分青红皂白对齐边缘特征会丢失类别判别信息的问题，本文提出基于核柯西-施瓦茨互信息的DAS-MI框架，通过最大化不同域同类特征之间的统计依赖性来实现类条件对齐。该方法在类别先验跨域变化时仍能保留判别性，提升模型对未见分布偏移的鲁棒性。这为有多个源域条件下的不变表示学习提供了更精细的对齐策略，可为OOD不变学习借鉴。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 域泛化中盲目对齐边缘特征会丢失类别判别信息，尤其在类先验跨域变化时。
method: 提出DAS-MI框架，用核柯西-施瓦茨互信息最大化跨域同类特征间的统计依赖，实现类条件对齐。
result: 实验表明该方法在类别先验变化的域泛化场景下比边缘对齐更鲁棒。
conclusion: 类条件不变对齐能兼顾判别性与泛化性，为多源域不变学习提供新思路。
---

## Abstract
Domain Generalization (DG) seeks to learn models that are robust to unseen distribution shifts, a critical challenge for real-world machine learning applications. A dominant paradigm is to enforce domain invariance by aligning feature distributions from multiple source domains. However, aligning marginal feature distributions indiscriminately can discard critical class-discriminative information, especially when class priors vary across domains. We address this limitation with Domain Alignment via Kernel Cauchy-Schwarz Mutual Information (DAS-MI), a novel framework that advances principled class-conditional alignment. The core principle is to maximize the statistical dependence between same-class features across different domains. We operationalize this using the Cauchy-Schwarz Quadratic Mutual Information (CS-QMI), a powerful information-theoretic measure. Critically, and in contrast to prior work relying on complex approximations or adversarial training, our approach yields a closed-form, non-parametric alignment objective derived from kernel density estimates. This results in a stable loss that integrates seamlessly into deep learning pipelines. Extensive experiments across five benchmark datasets demonstrate performance comparable to state-of-the-art methods. DAS-MI offers a theoretically-grounded and practically efficient solution to domain generalization that robustly preserves discriminative information.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过类条件对齐学习跨域不变特征以实现域泛化。

### 2. 核心内容
针对域泛化中不分青红皂白对齐边缘特征会丢失类别判别信息的问题，本文提出基于核柯西-施瓦茨互信息的DAS-MI框架，通过最大化不同域同类特征之间的统计依赖性来实现类条件对齐。该方法在类别先验跨域变化时仍能保留判别性，提升模型对未见分布偏移的鲁棒性。这为有多个源域条件下的不变表示学习提供了更精细的对齐策略，可为OOD不变学习借鉴。

### 3. 对应检索需求
out-of-distribution generalization methods for robust representation learning。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=nGbdYCPlZw](https://openreview.net/forum?id=nGbdYCPlZw)
