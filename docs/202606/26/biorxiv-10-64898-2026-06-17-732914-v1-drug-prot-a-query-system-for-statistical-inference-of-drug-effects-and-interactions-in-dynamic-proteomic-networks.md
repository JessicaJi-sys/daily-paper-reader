---
title: "Drug-Prot: A query system for statistical inference of drug effects and interactions in dynamic proteomic networks"
title_zh: Drug-Prot：动态蛋白质组学网络中药物效应与相互作用的统计推断查询系统
authors: "Ulmer, M., Sun, R., Qian, L., Aebersold, R., Guo, T., Buehlmann, P."
date: 2026-06-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.732914v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 专注于利用蛋白质组数据进行药物相互作用预测
tldr: 药物联合治疗需理解药效和相互作用，但现有方法缺乏对蛋白质组动态网络的分析。Drug-Prot基于大规模扰动蛋白质组数据，利用63种单药和59种组合在18个乳腺癌细胞系中的时间序列数据，量化药效并构建有向时间蛋白质依赖网络。该框架提供交互式网页应用，支持用户自定义蛋白质集并返回校正p值和网络，无需原始数据。通过三阴性乳腺癌案例验证，Drug-Prot能链接候选蛋白质特征与可行药物组合，助力精准治疗。
source: biorxiv
selection_source: fresh_fetch
motivation: 开发一个利用大规模蛋白质组数据统计推断药效和药物相互作用，并构建动态蛋白质网络的系统。
method: 基于63种单药和59种组合在18个乳腺癌细胞系6、24、48小时的蛋白质组数据，估计药效并重建有向时间依赖网络；提供交互式网页应用。
result: 成功量化药效和相互作用，用户可查询获得校正p值和动态网络；在三阴性乳腺癌中识别出与药物反应相关的蛋白质。
conclusion: Drug-Prot为药物组合设计提供了因果蛋白质特征的统计推断工具，可促进精准医疗。
---

## 摘要
理解药物效应和药物-药物相互作用对于开发联合疗法至关重要。我们提出了Drug-Prot，一个利用大规模扰动蛋白质组学来量化因果药物效应、药物-药物相互作用以及动态蛋白质关系的计算框架。利用来自63种单药和59种药物组合（应用于18个乳腺癌细胞系，在6、24和48小时）的数据，Drug-Prot评估药物对蛋白质表达的影响，并重建有向时间蛋白质依赖性网络。

该公开可用的软件支持对用户定义的蛋白质集进行靶向分析，显著降低了多重检验负担。通过交互式Web应用程序，用户可以获得单药和组合效应的校正p值、有向时间依赖性网络以及可下载的结果，而无需访问底层蛋白质组数据集。

作为应用案例，我们将不变性正则化随机森林应用于三阴性乳腺癌细胞系，以识别与药物反应相关的蛋白质。在Drug-Prot中查询这些蛋白质可揭示蛋白质网络层面的药物特异性和相互作用效应，说明该框架如何将候选因果蛋白质特征与可行的药物组合联系起来。

## Abstract
Understanding drug effects and drug-drug interactions is essential for developing combination therapies. We present Drug-Prot, a computational framework that leverages large-scale perturbation proteomics to quantify causal drug effects, drug-drug interactions, and dynamic protein relationships. Using data from 63 single drugs and 59 drug combinations applied to 18 breast cancer cell lines at 6, 24, and 48 hours, Drug-Prot estimates drug effects on protein expression and reconstructs directed temporal protein dependency networks.

The publicly available software enables targeted analyses of user-defined protein sets, substantially reducing the multiple-testing burden. Through an interactive web application, users obtain corrected p-values for single-drug and combination effects, directed temporal dependency networks, and downloadable results without requiring access to the underlying proteomic dataset.

As a use case, we apply invariance-regularized Random Forests to triple-negative breast cancer cell lines to identify proteins associated with drug response. Querying these proteins in Drug-Prot reveals drug-specific and interaction effects at the protein-network level, illustrating how the framework links candidate causal protein features to actionable drug combinations.