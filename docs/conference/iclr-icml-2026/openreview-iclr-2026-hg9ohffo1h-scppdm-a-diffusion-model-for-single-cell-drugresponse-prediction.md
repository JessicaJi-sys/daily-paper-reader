---
title: "scPPDM: A Diffusion Model for Single-Cell Drug–Response Prediction"
title_zh: scPPDM：面向单细胞药物反应预测的扩散模型
authors: "Zhaokang Liang, Shuyang Zhuang, Xiaoran Jiao, Weian Mao, Hao Chen, Chunhua Shen"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=HG9OHffO1h"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 面向未见药物与未见协变量设定的药物反应扩散模型
tldr: 针对单细胞药物反应预测中药物与协变量组合未见的分布外泛化难题，本文提出首个基于扩散的框架scPPDM。该方法通过非拼接的GD-Attn将扰动前状态与药物剂量两个条件通道耦合于统一潜在空间，并利用因子化无分类器引导提供可解释控制。在Tahoe-100M基准的未见药物与未见协变量两种严苛设定下，模型在多个指标上取得最优结果。研究证明扩散模型可有效应对药物冷启动与分布外预测，为药物泛化研究提供参考。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 单细胞药物反应预测面临药物未见与协变量组合未见的分布外泛化挑战，现有方法难以应对。
method: 提出扩散框架scPPDM，用GD-Attn将扰动前状态与药物剂量两个条件通道耦合于统一潜在空间。
result: 在Tahoe-100M基准的未见药物与未见协变量两种设定下，于多个指标上取得最优结果。
conclusion: 证明扩散模型可有效处理药物冷启动与分布外预测，为药物级泛化研究提供可借鉴方案。
---

## Abstract
This paper introduces the Single-Cell Perturbation Prediction Diffusion Model (scPPDM), the first diffusion-based framework for single-cell drug-response prediction from scRNA-seq data. scPPDM couples two condition channels, pre-perturbation state and drug with dose, in a unified latent space via non-concatenative GD-Attn. During inference, factorized classifier-free guidance exposes two interpretable controls for state preservation and drug-response strength and maps dose to guidance magnitude for tunable intensity. Evaluated on the Tahoe-100M benchmark under two stringent regimes, unseen covariate combinations (UC) and unseen drugs (UD), scPPDM sets new state-of-the-art results across log fold-change recovery, $\Delta$ correlations, explained variance, and DE-overlap. Representative gains include +36.11%/+34.21% on DEG logFC–Spearman/Pearson in UD over the second-best model. This control interface enables transparent what-if analyses and dose tuning, reducing experimental burden while preserving biological specificity.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向未见药物与未见协变量设定的药物反应扩散模型。

### 2. 核心内容
针对单细胞药物反应预测中药物与协变量组合未见的分布外泛化难题，本文提出首个基于扩散的框架scPPDM。该方法通过非拼接的GD-Attn将扰动前状态与药物剂量两个条件通道耦合于统一潜在空间，并利用因子化无分类器引导提供可解释控制。在Tahoe-100M基准的未见药物与未见协变量两种严苛设定下，模型在多个指标上取得最优结果。研究证明扩散模型可有效应对药物冷启动与分布外预测，为药物泛化研究提供参考。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=HG9OHffO1h](https://openreview.net/forum?id=HG9OHffO1h)
