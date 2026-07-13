---
title: "An Integrated Knowledge Graph and Network Medicine Pipeline for Drug Repurposing: Benchmarking Across Human Diseases and Application to Amyotrophic Lateral Sclerosis"
title_zh: 集成知识图谱和网络医学的药物再利用管道：跨人类疾病基准测试及在肌萎缩侧索硬化症中的应用
authors: "Jiang, A., Hu, J., Abdulle, Y., Pain, O., Iacoangeli, A."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.03.736387v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 基于知识图谱的药物重定位管线
tldr: 药物重定位是降低研发成本的有效策略。本研究提出集成知识图谱（DGLinker预测疾病基因）、网络医学（SAveRUNNER识别候选药物）和ATC类别富集分析（ATCEA）的三阶段管线。跨12种疾病基准测试显示AUROC稳定在0.71–0.77，ATCEA显著提升精确率和F1分数。应用于肌萎缩侧索硬化症（ALS）时，新发现77种优先候选药物，包括抗抑郁药和抗精神病药，部分经电子健康记录验证。该端到端框架为加速药物重定位提供稳健、可推广的工具。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1629, \"height\": 614, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1622, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 882, \"height\": 880, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1731, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1634, \"height\": 733, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1725, \"height\": 1529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 503, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1617, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1177, \"height\": 2218, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 2546, \"height\": 1048, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1660, \"height\": 1730, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1659, \"height\": 2499, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1658, \"height\": 2532, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-03-736387-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1657, \"height\": 989, \"label\": \"Table\"}]"
motivation: 现有药物重定位方法常孤立地使用知识图谱或网络医学，缺乏系统整合与跨疾病验证，且候选药物筛选未考虑药理类别一致性，导致假阳性高。
method: 构建三阶段管线：DGLinker预测新疾病基因→SAveRUNNER基于网络计算药物-疾病关联→ATC类别富集分析（ATCEA）按药理类别优先排序候选药物，并用于ALS案例研究。
result: 跨12病基准测试AUROC 0.71–0.77，ATCEA使精确率提升0.1–0.2；ALS应用发现77种富集候选药（如抗抑郁药），其中多种获文献与471例患者EHR数据支持。
conclusion: 该管线通过整合互补计算步骤，在保持稳健性能的同时提高候选药物药理相干性，为ALS等疾病提供可操作的候选库，展示了加速药物重定位的潜力。
---

## 摘要
药物再利用是一种识别已批准药物新治疗用途的实用策略，可能减少与传统药物开发相关的时间和成本。我们提出了一种新颖的三阶段药物再利用管道，整合了基于知识图谱的基因预测、基于网络的药物-疾病关联分析，以及按治疗类别对候选药物进行系统分类。该管道整合了DGLinker预测新型疾病相关基因，SAveRUNNER识别药物再利用候选物，以及ATC类别富集分析（ATCEA）按药理类别对候选物进行优先级排序。

我们使用DrugBank和MEDI2-HPS作为验证资源，在十二种疾病上对该管道进行了基准测试。使用DGLinker扩展的疾病-基因集作为输入增加了预测的再利用药物数量，而整体区分性能在不同疾病中保持稳定（AUROC 0.71-0.77）。应用ATCEA一致地提高了精确率、F1分数和特异性，同时降低了召回率，反映了一种保守的优先级排序策略，该策略缩小了候选空间，同时保留了药理上一致的药物-疾病候选物。

我们进一步将该管道应用于肌萎缩侧索硬化症（ALS），一种治疗选择有限的神经退行性疾病，并对结果进行了更深入的基于文献的验证。整合DGLinker预测的基因显著增加了显著候选药物的数量，并发现了仅使用已知ALS基因无法识别的富集ATC类别，包括抗抑郁药和抗精神病药。此外，只有使用DGLinker预测的基因时，才识别出一些在文献中有支持证据的药物。总体而言，在显著富集的ATC类别中筛选出77种候选药物，其中一些得到了先前发表研究的支持。为了为这些发现提供探索性的真实世界支持，我们在国王学院医院2361名ALS患者的纵向电子健康记录（EHR）数据集中进一步评估了候选药物。尽管由于样本量限制，可评估的药物数量有限，但EHR分析为选定的优先药物和药理类别提供了额外的临床相关背景。

我们的管道展示了通过将互补的计算方法整合到过程的每一步来加速药物再利用的潜力，提供了一个端到端的框架，在基准测试实验和用例中表现出稳健的性能。

图形摘要

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=80 SRC="FIGDIR/small/736387v1_ufig1.gif" ALT="Figure 1">
View larger version (34K):
org.highwire.dtl.DTLVardef@8f390borg.highwire.dtl.DTLVardef@ea14f4org.highwire.dtl.DTLVardef@5a1b1org.highwire.dtl.DTLVardef@1ba7df0_HPS_FORMAT_FIGEXP  M_FIG C_FIG

## Abstract
Drug repurposing offers a practical strategy to identify new therapeutic uses for approved drugs, potentially reducing the time and cost associated with conventional drug development. We present a novel three-stage drug repurposing pipeline that integrates knowledge graph-based gene prediction, network-based drug-disease association analysis, and systematic classification of candidate drugs by therapeutic class. The pipeline integrates DGLinker to predict novel disease-associated genes, SAveRUNNER to identify drug repurposing candidates, and ATC Category Enrichment Analysis (ATCEA) to prioritise candidates by pharmacological class.

We benchmarked the pipeline across twelve diseases using DrugBank and MEDI2-HPS as validation resources. Utilising DGLinker-expanded disease-gene sets as input increased the number of predicted repurposed drugs, while overall discriminative performance remained stable across diseases (AUROC 0.71-0.77). Application of ATCEA consistently improved precision, F1-score, and specificity, while reducing recall, reflecting a conservative prioritisation strategy that contracts the candidate space while retaining pharmacologically coherent drug-disease candidates.

We further applied the pipeline to amyotrophic lateral sclerosis (ALS), a neurodegenerative disease with limited therapeutic options and performed a deeper literature-based validation of the results. Incorporation of DGLinker-predicted genes substantially increased the number of significant candidate drugs and uncovered enriched ATC categories not identified using known ALS genes alone, including antidepressants and antipsychotics. Moreover, several drugs with supporting evidence available in literature were identified only when DGLinker-predicted genes were used. Overall, 77 candidate drugs were prioritised within significantly enriched ATC categories, several of which are supported by previously published studies. To provide exploratory real-world support for these findings, we further evaluated candidate drugs in a longitudinal electronic health record (EHR) dataset of 2361 patients with ALS from Kings College Hospital. Although the number of evaluable drugs was limited due to sample size, the EHR analysis provided additional clinically relevant context for selected prioritised drugs and pharmacological classes.

Our pipeline demonstrates potential to accelerate drug repurposing by integrating complementary computational approaches to each step of the process, providing an end-to-end framework that showed robust performance across benchmarking experiments and use cases.

Graphical abstract

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=80 SRC="FIGDIR/small/736387v1_ufig1.gif" ALT="Figure 1">
View larger version (34K):
org.highwire.dtl.DTLVardef@8f390borg.highwire.dtl.DTLVardef@ea14f4org.highwire.dtl.DTLVardef@5a1b1org.highwire.dtl.DTLVardef@1ba7df0_HPS_FORMAT_FIGEXP  M_FIG C_FIG