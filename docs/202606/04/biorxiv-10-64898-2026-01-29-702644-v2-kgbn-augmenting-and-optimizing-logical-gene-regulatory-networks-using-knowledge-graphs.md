---
title: "KGBN: Augmenting and optimizing logical gene regulatory networks using knowledge graphs"
title_zh: KGBN：利用知识图谱增强和优化逻辑基因调控网络
authors: "Li, L. X., Zhang, Y., Aguilar, B., Shah, T., Gennari, J., Qin, G."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.29.702644v2.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 知识图谱增强逻辑基因网络用于药物反应预测
tldr: 逻辑基因调控网络模型通常不完整且难以扩展。本文提出KGBN工作流，利用知识图谱中的调控关系作为替代逻辑规则，并通过实验数据优化规则概率。在急性髓系白血病中，扩展的模型能依据突变信息预测药物敏感性。该方法实现了可解释、上下文感知的GRN建模，助力精准医学。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有逻辑GRN模型不完整，难以扩展至全面网络，限制了药物反应预测等应用。
method: KGBN从知识图谱提取调控关系作为替代逻辑规则，并优化规则概率以匹配实验数据。
result: 在AML中，KGBN扩展的模型能基于突变预测药物敏感性，复现已知治疗敏感性。
conclusion: KGBN实现了可解释、上下文感知的GRN建模，有助于精准医学应用。
---

## 摘要
逻辑基因调控网络模型提供了细胞调控的可解释、机制性表示，广泛应用于系统生物学。然而，现有模型大多不完整、具有上下文特异性，且难以扩展为全面的基因调控网络，限制了其在药物反应预测和精准医学等任务中的广泛应用。在此，我们补充关于虚拟孪生的想法：针对急性髓系白血病患者，我们可以利用全面的基因调控网络预测药物反应。我们提出KGBN（知识图谱增强的布尔网络建模），一种系统增强逻辑基因调控网络的计算工作流。KGBN整合来自精心整理的知识图谱的调控相互作用作为替代逻辑规则，同时保留现有模型经过验证的结构。规则概率根据实验数据进行优化，以表示调控不确定性并实现数据驱动的校准。将KGBN应用于急性髓系白血病，我们表明，通过药物-靶点通路扩展现有基因调控网络并针对离体药物反应数据进行训练，可生成重现已知治疗敏感性和信号依赖性的突变特异性模型，证明了KGBN在可解释、上下文感知的基因调控网络建模中的实用性。

## Abstract
Logical gene regulatory network (GRN) models provide interpretable, mechanistic representations of cellular regulation and are widely used in systems biology. However, most existing models remain incomplete, context-specific, and difficult to extend to comprehensive GRNs, limiting their broader applicability to tasks such as drug-response prediction and precision medicine. Here, add some ideas about virtual twins: With AML patients, we can use comprehensive GRNs to predict drug response. We present KGBN (Knowledge Graph-augmented Boolean Network modeling), a computational workflow for systematically augmenting logical GRN models. KGBN incorporates regulatory interactions derived from curated knowledge graphs as alternative logical rules while preserving the validated structure of existing models. Rule probabilities are optimized against experimental data to represent regulatory uncertainty and achieve data-driven calibration. Applying KGBN to acute myeloid leukemia, we show that extending an existing GRN with drug-target pathways and training against ex vivo drug-response data yields mutation-specific models that recapitulate known therapeutic sensitivities and signaling dependencies, demonstrating the utility of KGBN for interpretable, context-aware GRN modeling. (Should be predict)