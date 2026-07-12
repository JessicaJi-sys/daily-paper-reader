---
title: "Interaction-finder: automated literature-based discovery of biological entity associations with quote-level provenance"
title_zh: 交互发现器：基于文献自动发现生物实体关联并附带引用级来源
authors: "Chapman, T. E., Lassmann, T."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.07.736901v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 利用大语言模型引导文献发现生物实体关联，可用于药物相互作用提取
tldr: 从文献中手工收集生物学实体关联效率低下且易遗漏。Interaction-finder利用大语言模型引导迭代搜索，从全文提取候选关联并附带原文引证。在细胞类型-标记物、疾病-基因、配体-受体三个领域，它比单次提示和现成框架多召回1.2-4.3倍已知关联，未验证候选与基准关联得分相近。该工具生成交互式HTML报告，支持快速筛选，以MIT许可证开源。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1307, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1187, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1405, \"height\": 810, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1575, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736901-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1634, \"height\": 497, \"label\": \"Table\"}]"
motivation: 现有数据库覆盖不全，研究者需手动检索大量文献，过程耗时且容易遗漏关键关联。
method: 通过LLM引导的迭代搜索发现相关文献，从全文提取候选关联，并引用原文段落作为出处，最终生成排序列表。
result: 在60个主题上，Tool召回已知关联数量是单次提示的1.2-4.3倍，排名前20的召回率达0.61，未验证候选中与基准关联得分相近。
conclusion: Interaction-finder自动化了实体关联发现，提供可验证的引证证据，显著提升文献挖掘效率。
---

## 摘要
识别生物实体之间的相互作用是分子研究的基石，但从文献中整理此类列表既缓慢又繁琐。对于许多研究问题，并不存在精心整理的数据库，研究人员只能自行查阅相关文献。我们提出了交互发现器（interaction-finder），这是一个自动化该过程的工具：给定主题字符串和用户定义的实体类型，它通过LLM引导的迭代搜索发现相关文献，从全文文章中提取候选关联，并生成一个排序列表，其中每个关联都有经过源文本验证的引用段落支持。一个自包含的交互式HTML报告能够快速对结果进行分类。在三个领域（细胞类型-细胞标记物、疾病-基因和配体-受体）的60个主题上进行评估，交互发现器回忆的已知关联数量是单次提示和现成深度研究框架的1.2-4.3倍，所有提取的引用均经过源文本验证。为了评估黄金标准数据库中未识别的候选对象，我们使用独立于工具推理的LLM评判器对每个候选对象进行评分。在三个领域中，未验证的候选对象得分与黄金标准关联相似。我们发现黄金标准关联在排序候选对象的顶部富集，总体recall@20为0.61。交互发现器可在https://github.com/tecosaur/interaction_finder免费获取，采用MIT许可证。

## Abstract
Identifying interactions between biological entities is a cornerstone of molecular research, but assembling such lists from the literature is slow and tedious. For many research questions, no curated database exists, leaving researchers to survey the relevant literature themselves. We present interaction-finder, a tool that automates this process: given a topic string and user-defined entity types, it discovers relevant literature through LLM-guided iterative search, extracts candidate associations from full-text articles, and produces a ranked list where every association is backed by quoted passages verified against the source text. A self-contained interactive HTML report enables rapid triage of the results. Evaluated across 60 topics in three domains (celltype-cellmarker, disease-gene, and ligand-receptor), interaction-finder recalls 1.2-4.3x as many known associations as single-shot prompting and an off-the-shelf deep-research framework, with all extracted quotes verified against source text. To assess candidates unrecognised from the gold-standard databases, we scored each candidate using an independent LLM judge blind to the tool's reasoning. Across the three domains, unverified candidates score similarly to gold-standard associations. We find the gold-standard associations are enriched at the top of our ranked candidates, with an overall recall@20 of 0.61. Interaction-finder is freely available at https://github.com/tecosaur/interaction_finder under an MIT licence.