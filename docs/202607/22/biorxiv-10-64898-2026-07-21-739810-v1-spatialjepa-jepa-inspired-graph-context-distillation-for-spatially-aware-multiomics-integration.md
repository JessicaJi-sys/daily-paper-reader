---
title: "SpatialJEPA: JEPA-inspired graph-context distillation for spatially aware multiomics integration"
title_zh: SpatialJEPA：受JEPA启发的图上下文蒸馏用于空间感知的多组学整合
authors: "Mann-Krzisnik, D., Li, Y."
date: 2026-07-22
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.21.739810v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 教师-学生框架用于图上下文蒸馏，可迁移至药物相互作用预测
tldr: 整合空间基因组学模态需要多分子层表示学习，但许多RNA-ATAC配对数据是解离的且缺乏空间坐标。为此提出SpatialJEPA，一个受JEPA启发的师生框架，通过将教师的空间邻域图替换为自身份图来掩码空间上下文，使学生学习匹配嵌入，从而可应用于解离数据。在鼠脑多组学中，该表示支持源-目标对齐，恢复空间组织的转录组和染色质可及性程序，并与非空间参考相比显示配体-受体通路结构一致性。该方法为解离多组学数据赋予了空间上下文感知能力，显著提升了整合效果。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739810-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1649, \"height\": 835, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739810-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1659, \"height\": 1621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-21-739810-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1640, \"height\": 1257, \"label\": \"Figure\"}]"
motivation: 现有整合框架无法处理缺乏空间坐标的解离多组学数据，需引入空间上下文迁移方法。
method: 采用JEPA师生框架，训练时掩码教师的空间邻域图，强迫学生从无空间上下文中学习匹配嵌入。
result: 在鼠脑多组学中实现源-目标对齐，恢复空间基因表达和染色质可及性模式，并符合配体-受体通路结构。
conclusion: SpatialJEPA有效将空间上下文从空间数据迁移到非空间数据，提升解离多组学整合的空间感知能力。
---

## 摘要
用于整合空间基因组学模态的计算框架扩展了跨分子层的基于细胞的表示学习，但许多配对的RNA-ATAC数据集是解离的且缺乏空间坐标。我们提出SpatialJEPA，一种受JEPA启发的教师-学生框架，用于将空间上下文从空间多组学数据转移到非空间多组学数据。与补丁或特征掩码目标不同，SpatialJEPA通过在学生训练期间用仅自身的恒等图替换教师的空间邻域图来掩码空间上下文，使得空间样本对学生而言显得解离。学生学会从这种图上下文受限的视角匹配教师嵌入，因此在推理时可应用于解离的RNA-ATAC数据。在小鼠脑多组学中，得到的表示支持源-目标对齐，恢复空间组织的转录组和染色质可及性程序，并与非空间参考相比显示出与配体-受体通路结构的一致性。已被CIBB 2026会议接收（https://cibb2026.teralab.ai/）

## Abstract
Computational frameworks for integrating spatial genomics modalities extend cell-based representation learning across molecular layers, but many paired RNA-ATAC datasets are dissociated and lack spatial coordinates. We introduce SpatialJEPA, a JEPA-inspired teacher-student framework for transferring spatial context from spatial multiomics data to non-spatial multiome data. In contrast to patch- or feature-masking objectives, SpatialJEPA masks spatial context by replacing the teacher's spatial neighborhood graph with a self-only identity graph during student training, making the spatial sample appear dissociated to the student. The student learns to match teacher embeddings from this graph-context-restricted view and can therefore be applied to dissociated RNA-ATAC data at inference time. In mouse brain multiomics, the resulting representation supports source-target alignment, recovers spatially organized transcriptomic and chromatin-accessibility programs, and shows concordance with ligand-receptor pathway structure compared with non-spatial references. Accepted at the CIBB 2026 conference (https://cibb2026.teralab.ai/)