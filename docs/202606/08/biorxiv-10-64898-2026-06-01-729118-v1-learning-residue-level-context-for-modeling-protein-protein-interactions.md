---
title: Learning residue-level context for modeling protein-protein interactions
title_zh: 学习残基层面的上下文以建模蛋白质-蛋白质相互作用
authors: "Zhang, Z., Yang, Z., Liu, A., Yu, K.-H., Zhao, J., Yang, Y., Neale, B., Chen, S."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729118v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 使用基于transformer的蛋白质语言模型进行成对相互作用预测，方法上与LLM用于DDI类似
tldr: 现有蛋白质语言模型处理相互作用时聚合全蛋白信息，分辨率与可解释性有限。本文提出ReCLIP，一个基于Transformer的框架，通过结合蛋白质内残基邻域和交互伙伴的残基条件表示，学习残基级别的交互特异性表征。在突变预测（AUROC=0.973）、翻译后修饰（AUROC=0.822）和零样本肽-MHC结合（AUROC=0.972）任务中表现优异，分析显示残基邻域具有结构功能一致性。该方法为蛋白质相互作用建模提供了通用可解释框架，并揭示了残基上下文对交互特异性的影响。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有方法缺乏残基级分辨率与可解释性，无法细粒度刻画蛋白质相互作用。
method: 提出ReCLIP框架，利用Transformer编码残基邻域与交互伙伴的残基条件表示，学习残基级交互表征。
result: 在多项任务中达高精度（突变预测AUROC 0.973，翻译后修饰0.822，pMHC零样本0.972），残基邻域反映功能模式。
conclusion: ReCLIP建立了通用可解释的相互作用建模框架，并将临床变异关联至特定分子交互扰动。
---

## 摘要
蛋白质语言模型（PLMs）通过从序列中学习残基层面特征来预测蛋白质性质，但大多数基于PLM的蛋白质-蛋白质相互作用方法会聚合整个蛋白质的信息，从而限制了分辨率和可解释性。本文提出ReCLIP，这是一个基于Transformer的框架，通过结合蛋白质内残基邻域和相互作用伙伴的残基条件化表示，在单个残基层面学习相互作用特异性表示。我们展示了以残基为中心的上下文为在不同生物学背景下建模蛋白质相互作用提供了通用框架。ReCLIP能准确预测突变诱导的扰动（AUROC = 0.973），泛化至不改变序列的翻译后修饰（AUROC = 0.822），并能对未见过的等位基因实现肽-MHC结合的零样本预测（AUROC高达0.972）。对学习到的残基邻域的分析揭示了与已知结合决定因素一致的结构和功能上连贯的模式。应用于临床注释的遗传变异时，ReCLIP识别出与疾病相关的相互作用扰动，将致病性变异与特定的分子相互作用背景联系起来。我们的结果建立了一个可泛化且可解释的蛋白质相互作用建模框架，并提供了关于残基层面上下文如何塑造相互作用特异性及其扰动的见解。

## Abstract
Protein language models (PLMs) enable prediction of protein properties by learning residue-level features from sequence, yet most PLM-based approaches to protein-protein interactions aggregate information across entire proteins, limiting resolution and interpretability. Here we present ReCLIP, a transformer-based framework that learns interaction-specific representations at the level of individual residues by combining intra-protein residue neighborhoods with residue-conditioned representations of interaction partners. We show that residue-centered context provides a general framework for modeling protein interactions across diverse biological settings. ReCLIP accurately predicts mutation-induced perturbations (AUROC = 0.973), generalizes to post-translational modifications that do not alter sequence (AUROC = 0.822), and enables zero-shot prediction of peptide-MHC binding across unseen alleles (AUROC up to 0.972). Analysis of learned residue neighborhoods reveals structurally and functionally coherent patterns aligned with known determinants of binding. Applied to clinically annotated genetic variants, ReCLIP identifies disease-associated interaction perturbations that link pathogenic variants to specific molecular interaction contexts. Our results establish a generalizable and interpretable framework for modeling protein interactions and provide insights into how residue-level context shapes interaction specificity and its perturbation.