---
title: "PhenoXtract: combining Large Language Model and Knowledge Graph embedding to extract phenotypes from clinical descriptions"
title_zh: PhenoXtract：结合大型语言模型与知识图谱嵌入从临床描述中提取表型
authors: "Berardelli, S., BRIERE, G., Loire, B., De Paoli, F., Gazzo, A. M., Limongelli, I., Magni, P., Zucca, S., Baudot, A."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733382v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 结合大语言模型和知识图谱嵌入进行表型提取，方法可迁移至冷启动药物相互作用预测
tldr: 标准化表型描述对精准诊断至关重要，但人工从文献或病历中提取并映射到人类表型本体（HPO）耗时费力。PhenoXtract结合大语言模型与知识图谱嵌入，构建多步流水线，从临床描述中提取候选表型实体并映射至增强版HPO知识图谱。在专家验证数据集上，召回率为0.70，精确率为0.85，每个文本处理仅需10-20秒，且在三个基准测试中两个优于现有工具。该研究展示了混合方法在大规模自动化临床表型提取中的潜力。
source: biorxiv
selection_source: fresh_fetch
motivation: 临床诊断需标准化表型描述，但手动提取与映射至HPO效率低下，亟需自动化方法。
method: PhenoXtract采用LLM提取候选表型实体，再通过知识图谱嵌入匹配至富化后的HPO知识图谱。
result: 在专家验证数据集上召回0.70、精确0.85，多数基准测试优于现有工具，耗时10-20秒/文本。
conclusion: LLM与知识图谱嵌入的混合方法可扩展应用于自动化临床表型提取，前景广阔。
---

## 摘要
动机：标准化的表型描述对于准确诊断至关重要，然而临床医生和研究人员在从科学文献或患者临床记录中手动提取和映射表型到人类表型本体时面临挑战。近期深度学习的进展为自动化提供了新的机遇。我们开发了PhenoXtract，一种结合大型语言模型与知识图谱嵌入的新型表型提取方法。PhenoXtract是一个多步骤流水线，以临床描述为输入，使用大型语言模型提取候选表型实体，并将其映射到经过丰富的人类表型本体（以知识图谱形式处理）中的术语。结果：在专家策划的基准数据集上的评估显示，PhenoXtract的召回率为0.70，精确率为0.85，与手动提取的表型具有一致性，每段文本分析的计算时间为10-20秒。此外，在三个基准数据集中的两个上，PhenoXtract超越了基于规则和基于深度学习的最先进工具。这些结果表明，结合大型语言模型与知识图谱嵌入的混合方法为大规模的自动化临床表型分析提供了有前景的方向。

## Abstract
Motivation: Standardized phenotypic descriptions are essential for accurate diagnosis, yet clinicians and researchers face challenges in manually extracting and mapping phenotypes from scientific literature or patient clinical records to the Human Phenotype Ontology. Recent advances in deep learning offer new opportunities for automation. We developed PhenoXtract, a novel phenotype extraction approach that combines Large Language Models and Knowledge Graph embedding. PhenoXtract is a multistep pipeline that takes clinical descriptions as input, extracts candidate phenotype entities using large language models, and maps them to terms from an enriched version of the Human Phenotype Ontology, processed as a knowledge graph. Results: Evaluation against expert-curated ground-truth datasets show a recall of 0.70 and precision of 0.85 for PhenoXtract, demonstrating concordance with manually extracted phenotypes, with a computation time of 10-20 seconds for each text analyzed. Moreover, PhenoXtract surpasses rule-based and deep learning-based state-of-the-art tools in two out of the three ground-truth datasets evaluated. These results suggest that hybrid approaches combining Large Language Models and Knowledge Graph embeddings represent a promising direction for automated clinical phenotyping at scale.