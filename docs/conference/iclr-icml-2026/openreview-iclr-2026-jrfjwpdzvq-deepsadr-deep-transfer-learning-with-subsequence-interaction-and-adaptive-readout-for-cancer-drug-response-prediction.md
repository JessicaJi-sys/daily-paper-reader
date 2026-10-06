---
title: "DeepSADR: Deep Transfer Learning with Subsequence Interaction and Adaptive Readout for Cancer Drug Response Prediction"
title_zh: DeepSADR：面向癌症药物反应预测的子序列交互与自适应读出深度迁移学习
authors: "Yuanpeng Zhang, Zhijian Huang, Ziyu Fan, Siyuan Shen, Yahan Li, Shangqian Wu, Min Wu, Lei Deng"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=jrFJWpDZvq"
tags: ["query:ddi-moe"]
score: 4.0
evidence: 基因组分布偏移下的药物反应迁移学习预测
tldr: 针对癌症药物反应预测中细胞系与患者间存在基因组分布偏移、临床数据稀缺的问题，本文提出DeepSADR深度迁移学习框架。该方法联合建模药物子序列交互与基因组通路，并引入自适应读出以缓解体外与体内机制差异。实验表明考虑子结构与域差异能提升患者药物反应预测表现。研究强调了分布偏移下细粒度交互建模的重要性，为药物级泛化预测提供借鉴。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 细胞系与患者间存在基因组分布偏移，且临床反应数据稀缺，现有迁移方法仅对齐全局特征而忽略药物子结构。
method: 提出DeepSADR，结合药物子序列交互建模与自适应读出机制，实现从细胞系到患者的深度迁移学习。
result: 通过考虑药物子结构与通路交互并处理体外体内差异，缓解分布偏移，提升患者药物反应预测表现。
conclusion: 强调子结构交互与域差异对迁移预测的重要性，为分布偏移下的药物反应预测提供新思路。
---

## Abstract
Cancer treatment efficacy exhibits high inter-patient heterogeneity due to genomic variations. While large-scale in vitro drug response data from cancer cell lines exist, predicting patient drug responses remains challenging due to genomic distribution shifts and the scarcity of clinical response data. Existing transfer learning methods primarily align global genomic features between cell lines and patients. However, they often ignore two critical aspects. First, drug response depends on specific drug substructures and genomic pathways. Second, drug response mechanisms differ in vitro and in vivo settings due to factors such as the immune system and tumor microenvironment. To address these limitations, we propose DeepSADR, a novel deep transfer learning framework for enhanced drug response prediction based on subsequence interaction and adaptive readout. In particular, DeepSADR models drug responses as interpretable bipartite interaction graphs between drug substructures and enriched genomic pathways. Subsequently, a supervised graph autoencoder was designed to capture latent interactions between drugs and gene subsequences within these interaction graphs. In addition, DeepSADR treats the drug response process as a transferable domain. A Set Transformer-based adaptive readout (AR) function learns domain-invariant response representations, enabling effective knowledge transfer from abundant cell line data to scarce patient data. Extensive experiments on clinical patient cohorts demonstrate that DeepSADR significantly outperforms state-of-the-art methods, and ablation experiments have validated the effectiveness of each module.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基因组分布偏移下的药物反应迁移学习预测。

### 2. 核心内容
针对癌症药物反应预测中细胞系与患者间存在基因组分布偏移、临床数据稀缺的问题，本文提出DeepSADR深度迁移学习框架。该方法联合建模药物子序列交互与基因组通路，并引入自适应读出以缓解体外与体内机制差异。实验表明考虑子结构与域差异能提升患者药物反应预测表现。研究强调了分布偏移下细粒度交互建模的重要性，为药物级泛化预测提供借鉴。

### 3. 对应检索需求
drug-level out-of-distribution generalization under distribution shift。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=jrFJWpDZvq](https://openreview.net/forum?id=jrFJWpDZvq)
