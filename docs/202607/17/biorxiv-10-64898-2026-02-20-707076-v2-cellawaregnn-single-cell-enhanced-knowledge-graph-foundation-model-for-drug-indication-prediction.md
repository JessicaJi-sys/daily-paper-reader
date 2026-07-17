---
title: "CellAwareGNN: Single-Cell Enhanced Knowledge Graph Foundation Model for Drug Indication Prediction"
title_zh: CellAwareGNN：单细胞增强的知识图谱基础模型用于药物适应症预测
authors: "Zhang, X., Jeong, E., Yan, C., Feng, Y., Lyu, L., Guo, X., Chen, Y."
date: 2026-07-13
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.20.707076v2.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 使用图基础模型进行知识图谱补全以促进药物发现
tldr: "现有生物医学知识图谱缺乏细胞类型特异性表达信息，限制了疾病机制的捕获和药物重定位性能。本文首先更新PrimeKG至PrimeKG-U并训练更强基线TxGNN-U，然后通过整合OneK1K数据集的细胞类型特异性基因表达签名，构建单细胞增强知识图谱scPrimeKG，包含1400万边和14.7万节点。在此基础上提出CellAwareGNN图基础模型，预训练后用于药物适应症预测，在全部疾病覆盖评估中AUPRC达到0.826，对自身免疫疾病达0.864，分别比TxGNN提升3.4%和6.0%，并识别出Ocrelizumab等重定位候选药物。该工作证明了融入单细胞表达上下文能显著提升图药物重定位的预测性能与生物学可解释性。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1776, \"height\": 741, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 882, \"height\": 1041, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 890, \"height\": 1125, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1885, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1876, \"height\": 157, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 894, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 895, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1846, \"height\": 1321, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1841, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-02-20-707076-v2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1841, \"height\": 243, \"label\": \"Table\"}]"
motivation: 现有知识图谱缺少细胞类型特异性表达，无法捕获如免疫细胞通路等疾病机制，且评估仅覆盖部分疾病。
method: 更新PrimeKG为PrimeKG-U，整合单细胞表达签名构建scPrimeKG，并预训练CellAwareGNN进行全疾病药物适应症预测。
result: CellAwareGNN在药物适应症预测中AUPRC达0.826，对自身免疫疾病为0.864，优于TxGNN和TxGNN-U。
conclusion: 整合单细胞基因组学提升图模型预测性能与可解释性，为药物重定位提供新范式。
---

## 摘要
图基础模型已成为强大的药物重定位工具，能够从大型生物医学知识图谱中预测新的药物-疾病适应症。一个代表性例子是TxGNN，它先前基于PrimeKG（一个覆盖超过17,000种疾病的综合性生物医学知识图谱）开发并训练。虽然TxGNN表现出色，但现有生物医学知识图谱缺乏细粒度的、细胞类型特异性的表达背景。这限制了它们捕获由失调细胞程序驱动的疾病机制的能力，例如自身免疫疾病中的免疫细胞特异性通路。此外，先前的评估通常仅测试随机选择的疾病子集，导致许多疾病未被检查，从而限制了关于模型在整个疾病谱上性能的结论。

为应对这些局限性，我们首先通过纳入扩展和精选的生物医学知识将PrimeKG更新为PrimeKG-U，然后开发TxGNN-U作为更强的基于图的基线。在此基础之上，我们引入了CellAwareGNN，一个将单细胞基因组学整合到PrimeKG-U中的图基础模型。我们通过纳入OneK1K数据集的细胞类型特异性基因表达特征，构建了一个单细胞增强的知识图谱scPrimeKG，将PrimeKG从约810万条边和12.9万个节点扩展到超过1400万条边和14.7万个节点。CellAwareGNN在scPrimeKG的所有关系类型上进行预训练，并在药物适应症预测上进行评估，明确覆盖知识图谱中的所有疾病。

CellAwareGNN持续优于TxGNN和TxGNN-U。在药物适应症预测中，CellAwareGNN的AUPRC达到0.826，比TxGNN-U（0.816）提高1.2%，比TxGNN（0.799）提高3.4%。值得注意的是，对于自身免疫疾病，CellAwareGNN的AUPRC达到0.864，比TxGNN-U（0.847）提高2.0%，比TxGNN（0.815）提高6.0%。重要的是，CellAwareGNN优先排序了有前景的重定位候选药物，包括通过表达CD20的B细胞治疗天疱疮的奥瑞珠单抗、通过T细胞和B细胞中的DHFR和ATIC活性治疗天疱疮的甲氨蝶呤，以及通过PPAR-γ激活治疗类风湿关节炎的罗格列酮。这些结果证明了纳入细胞类型特异性表达背景对于提高基于图的药物重定位的预测性能和生物学可解释性的价值。

CCS概念：应用计算→健康信息学；生物信息学；计算方法→知识表示与推理；神经网络。

ACM参考文献格式：Xinmeng Zhang, Eugene Jeong, Chao Yan, Yubo Feng, Linshuoshuo Lyu, Xingyi Guo, and You Chen. 2026. CellAwareGNN：单细胞增强的知识图谱基础模型用于药物适应症预测. In Proceedings of the 32nd ACM SIGKDD Conference on Knowledge Discovery and Data Mining V.2 (KDD 2026), 2026年8月9-13日, 韩国济州岛. ACM, 纽约, NY, USA, 12页. https://doi.org/10.1145/3770855.3819012

## Abstract
Graph foundation models have emerged as powerful tools for drug repurposing by enabling the prediction of novel drug-disease indications from large biomedical knowledge graphs. A representative example is TxGNN, which was previously developed and trained on PrimeKG, a comprehensive biomedical knowledge graph covering over 17,000 diseases. While TxGNN demonstrates strong performance, existing biomedical knowledge graphs largely lack fine-grained, cell-type-specific expression context. This limits their ability to capture disease mechanisms driven by dysregulated cellular programs, such as immune cell-specific pathways in autoimmune diseases. Moreover, prior evaluations typically test only randomly selected subsets of diseases, leaving many diseases unexamined and limiting conclusions about model performance across the full disease spectrum.

To address these limitations, we first update PrimeKG to PrimeKG-U by incorporating expanded and curated biomedical knowledge and then develop TxGNN-U as a stronger graph-based baseline. Building on this foundation, we introduce CellAwareGNN, a graph foundation model that integrates single-cell genomics into PrimeKG-U. We construct a single-cell-enhanced knowledge graph, scPrimeKG, by incorporating cell-type-specific gene expression signatures from the OneK1K dataset, expanding PrimeKG from approximately 8.1 million edges and 129k nodes to over 14 million edges and 147k nodes. CellAwareGNN is pre-trained on all relation types in scPrimeKG and evaluated on drug indication prediction with explicit coverage of all diseases in the knowledge graph.

CellAwareGNN consistently outperforms TxGNN and TxGNN-U. For drug indication prediction, CellAwareGNN achieves an AUPRC of 0.826, representing a 1.2% improvement over TxGNN-U (0.816) and a 3.4% improvement over TxGNN (0.799). Notably, for autoimmune diseases, CellAwareGNN attains an AUPRC of 0.864, improving by 2.0% over TxGNN-U (0.847) and 6.0% over TxGNN (0.815). Importantly, CellAwareGNN prioritizes promising repurposing candidates, including Ocrelizumab for Pemphigus via CD20-expressing B cells, Methotrexate for Pemphigus through DHFR and ATIC activity in T and B cells, and Rosiglitazone for Rheumatoid Arthritis through PPAR-{gamma} activation. These results demonstrate the value of incorporating cell-type-specific expression context to improve both predictive performance and biological interpretability in graph-based drug repurposing.

CCS ConceptsO_LIApplied computing [-&gt;] Health informatics; Bioinformatics;
C_LIO_LIComputing methodologies [-&gt;] Knowledge representation and reasoning; Neural networks.
C_LI

ACM Reference FormatXinmeng Zhang, Eugene Jeong, Chao Yan, Yubo Feng, Linshuoshuo Lyu, Xingyi Guo, and You Chen. 2026. CellAwareGNN: Single-Cell Enhanced Knowledge Graph Foundation Model for Drug Indication Prediction. In Proceedings of the 32nd ACM SIGKDD Conference on Knowledge Discovery and Data Mining V.2 (KDD 2026), August 9-13, 2026, Jeju Island, Republic of Korea. ACM, New York, NY, USA, 12 pages. https://doi.org/10.1145/3770855.3819012