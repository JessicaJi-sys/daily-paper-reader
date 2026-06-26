---
title: "OmniPath Metabo: chemical structures, interactions and mechanisms to study the metabolome"
title_zh: OmniPath Metabo：用于研究代谢组的化学结构、相互作用和机制
authors: "Schaul, J., Bai, Y., Franken, J., Lawrence, T., Palacio-Escat, N., Bottazzi, D., Carreno, E., Daley, M., Gul, L., Sahin, A., Mananes, D., Bohar, B., Dugourd, A., Korcsmaros, T., Turei, D., Schmidt, C., Saez-Rodriguez, J."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733117v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 提供涵盖代谢物和药物的综合知识库，支持药物相互作用知识图的构建
tldr: 代谢组学数据分析因先验知识分散而困难。OmniPath Metabo整合40+数据库，统一化学结构、标识符和相互作用，提供交互式网页和API。该数据库支持构建细胞通讯和多组学调节子网络，结合OmniPath可实现信号、基因调控和代谢的集成分析。通过肺癌细胞系代谢组学数据展示其应用，为代谢组学机制和功能分析提供统一框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 代谢组学数据解读因知识资源碎片化而受限，需要统一先验知识框架。
method: 整合40+原始资源，使用受控词汇和化学信息学统一标识符与结构。
result: 构建OmniPath Metabo数据库，提供交互式网络和API，支持多组学整合分析。
conclusion: 为代谢组学提供统一先验知识框架，促进机制和功能分析。
---

## 摘要
组学数据的机制和功能分析在很大程度上依赖于整合先验知识；然而，将代谢组学数据与知识联系起来是一个主要的方法学挑战。这主要是由于不同的先验知识分散在许多数据库中，需要合并不同数据库记录中的化学结构、标识符以及不同水平的结构特异性。因此，这限制了代谢组的机制解释和功能表征。

在这里，我们提出OmniPath Metabo，一个全面的、协调一致的、以代谢组为中心的数据库，涵盖代谢物、脂质、食物源性化合物和小分子药物，以及它们相关的受体、转运蛋白、酶、反应、变构调节因子和疾病关联。OmniPath Metabo使用受控词汇和本体、结构以及内置的化学信息学来协调属性，映射标识符并跟踪歧义。OmniPath Metabo直接从40多个原始资源构建，并通过交互式网络应用和API在metabo.omnipathdb.org上免费访问。OmniPath Metabo能够动态地、特定上下文地构建子网络，以满足专门目的，如细胞间通讯或整合多组学代谢物驱动的调控，连接反应、变构调节、代谢物-受体和代谢物-转运蛋白相互作用。将其与OmniPath中的170多个其他资源结合，可用于信号传导、基因调控和代谢的整合网络。我们通过分析肺癌细胞系的公开代谢组学数据和代谢足迹对突变模式的影响，展示了OmniPath Metabo的应用。

总之，OmniPath Metabo将分散的资源转化为一个协调的先验知识框架，用于代谢组的机制和功能分析。

## Abstract
Mechanistic and functional analysis of omics data largely relies on the incorporation of prior knowledge; however, connecting metabolomics data and knowledge is a major methodological challenge. This is largely driven by the diverse prior knowledge being fragmented across many databases requiring the merging of different database records across chemical structures, identifiers, and varying levels of structural specificity. Hence, this limits mechanistic interpretation and functional characterisation of the metabolome.

Here, we present OmniPath Metabo, a comprehensive, harmonized, metabolome-centric database covering metabolites, lipids, food-derived compounds, and small molecule drugs, along with their associated receptors, transporters, enzymes, reactions, allosteric regulators, and disease associations. OmniPath Metabo harmonizes attributes using controlled vocabularies and ontologies, structures and built-in cheminformatics to map identifiers and track ambiguity. OmniPath Metabo is built directly from 40+ original resources and is freely accessible via an interactive web app and API at metabo.omnipathdb.org. OmniPath Metabo enables dynamic, context-specific construction of subnetworks to serve dedicated purposes, such as cell-cell communication or integrated multi-omics metabolite-driven regulation, connecting reactions, allosteric regulation, metabolite-receptor and metabolite-transporter interactions. Combining it with the over 170 other resources in OmniPath, it can be used for integrated networks of signaling, gene regulation, and metabolism. We showcase the application of OmniPath Metabo by analysing publicly available metabolomics data of lung cancer cell lines and metabolic footprints to mutational patterns.

In summary, OmniPath Metabo transforms fragmented resources into a harmonised prior knowledge framework for a mechanistic and functional analysis of the metabolome.