---
title: "Parameters as Experts: Adapting Vision Models with Dynamic Parameter Routing"
title_zh: 参数即专家：基于动态参数路由的视觉模型适配
authors: "Meng Lou, Stanley Yu, Yizhou Yu"
date: 2025-09-04
pdf: "https://openreview.net/pdf?id=o4Blnaaef7"
tags: ["query:ddi-moe"]
score: 5.0
evidence: 基于MoE的动态参数路由，按输入生成权重
tldr: 参数高效微调在复杂稠密预测任务中常因输入无关建模与跨层冗余表示而受限。作者提出AdaRoute，一种适配器式方法，采用简单混合专家架构，以可训练参数矩阵为专家中心，在前向传播中按当前模块动态生成权重。该设计缓解了输入无关与冗余问题，为MoE式动态参数路由在高效适配中的应用提供了参考。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 参数高效微调存在输入无关建模与跨层冗余表示问题。
method: 提出AdaRoute适配器，用参数矩阵作专家并动态生成当前模块权重。
result: 在稠密预测任务中缓解输入无关与冗余，提升适配效果。
conclusion: 展示了动态参数路由MoE在高效适配中的价值。
---

## Abstract
Adapting vision models using parameter-efficient fine-tuning (PEFT) remains challenging, as it aims to achieve performance comparable to full fine-tuning using a minimal number of trainable parameters. When applied to complex dense prediction tasks, existing methods exhibit limitations, including input-agnostic modeling and redundant cross-layer representations. To address these limitations, we propose AdaRoute, a new adapter-style method featuring a simple mixture-of-experts (MoE) architecture. Specifically, we introduce shared expert centers, where each expert is a trainable parameter matrix. During a feedforward pass, each AdaRoute module in the network dynamically generates weight matrices tailored for the current module via a simple dynamic parameter routing mechanism, which selectively aggregates parameter matrices in the corresponding expert center. Dynamic weight matrices in AdaRoute modules facilitate low-rank adaptation in an input-dependent manner, thus generating more customized and powerful feature representations.
Moreover, since AdaRoute modules across multiple network layers share the same expert center, they improve feature diversity by promoting implicit cross-layer feature interaction. Extensive experiments on diverse vision tasks demonstrate the superiority of AdaRoute. For instance, in the object detection and instance segmentation task on COCO2017 with ConvNeXt-L, AdaRoute significantly exceeds full fine-tuning by 1.4\%/1.6\% in AP$^b$/AP$^m$ using less than 5\% of the trainable parameters. In the more challenging panoptic segmentation task, when Swin-B and ConvNeXt-B are used as the backbone, AdaRoute remarkably improves over AdaptFormer by 1.7\% and 2.0\% in PQ, respectively, while using a comparable number of trainable parameters.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于MoE的动态参数路由，按输入生成权重。

### 2. 核心内容
参数高效微调在复杂稠密预测任务中常因输入无关建模与跨层冗余表示而受限。作者提出AdaRoute，一种适配器式方法，采用简单混合专家架构，以可训练参数矩阵为专家中心，在前向传播中按当前模块动态生成权重。该设计缓解了输入无关与冗余问题，为MoE式动态参数路由在高效适配中的应用提供了参考。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=o4Blnaaef7](https://openreview.net/forum?id=o4Blnaaef7)
