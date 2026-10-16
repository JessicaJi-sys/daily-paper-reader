---
title: "DeepSADR: Deep Transfer Learning with Subsequence Interaction and Adaptive Readout for Cancer Drug Response Prediction"
title_zh: DeepSADR：结合子序列交互与自适应读出的癌症药物反应深度迁移学习
authors: "Yuanpeng Zhang, Zhijian Huang, Ziyu Fan, Siyuan Shen, Yahan Li, Shangqian Wu, Min Wu, Lei Deng"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openreview.net/pdf?id=jrFJWpDZvq"
tags: ["query:ood-inv"]
score: 4.0
evidence: 基因组分布偏移下的药物反应迁移学习
tldr: 针对癌症患者药物反应预测中基因组分布偏移与临床数据稀缺、现有迁移学习方法仅对齐全局基因组特征而忽略药物子结构与通路依赖的问题，本文提出DeepSADR框架，结合子序列交互建模与自适应读出进行深度迁移学习，以更好地对齐药物子结构与基因组通路。该设计同时考虑了体外与体内响应机制的差异。实验表明其在药物反应预测上有所改进，属于药物领域分布偏移建模的相关工作，但与不变表示学习关联较弱。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 患者药物反应预测受基因组分布偏移与临床数据稀缺困扰，现有迁移方法仅对齐全局特征。
method: 提出DeepSADR，用子序列交互建模与自适应读出进行深度迁移学习以对齐药物子结构与通路。
result: 实验表明该方法在癌症药物反应预测上优于仅做全局特征对齐的迁移学习基线。
conclusion: 为药物领域的分布偏移建模提供了迁移学习方案，但与不变特征解耦主题关联有限。
---

## Abstract
Cancer treatment efficacy exhibits high inter-patient heterogeneity due to genomic variations. While large-scale in vitro drug response data from cancer cell lines exist, predicting patient drug responses remains challenging due to genomic distribution shifts and the scarcity of clinical response data. Existing transfer learning methods primarily align global genomic features between cell lines and patients. However, they often ignore two critical aspects. First, drug response depends on specific drug substructures and genomic pathways. Second, drug response mechanisms differ in vitro and in vivo settings due to factors such as the immune system and tumor microenvironment. To address these limitations, we propose DeepSADR, a novel deep transfer learning framework for enhanced drug response prediction based on subsequence interaction and adaptive readout. In particular, DeepSADR models drug responses as interpretable bipartite interaction graphs between drug substructures and enriched genomic pathways. Subsequently, a supervised graph autoencoder was designed to capture latent interactions between drugs and gene subsequences within these interaction graphs. In addition, DeepSADR treats the drug response process as a transferable domain. A Set Transformer-based adaptive readout (AR) function learns domain-invariant response representations, enabling effective knowledge transfer from abundant cell line data to scarce patient data. Extensive experiments on clinical patient cohorts demonstrate that DeepSADR significantly outperforms state-of-the-art methods, and ablation experiments have validated the effectiveness of each module.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基因组分布偏移下的药物反应迁移学习。

### 2. 核心内容
针对癌症患者药物反应预测中基因组分布偏移与临床数据稀缺、现有迁移学习方法仅对齐全局基因组特征而忽略药物子结构与通路依赖的问题，本文提出DeepSADR框架，结合子序列交互建模与自适应读出进行深度迁移学习，以更好地对齐药物子结构与基因组通路。该设计同时考虑了体外与体内响应机制的差异。实验表明其在药物反应预测上有所改进，属于药物领域分布偏移建模的相关工作，但与不变表示学习关联较弱。

### 3. 对应检索需求
research on out of distribution generalization and invariant representation learning for cold start drug drug interaction prediction。

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=jrFJWpDZvq](https://openreview.net/forum?id=jrFJWpDZvq)
