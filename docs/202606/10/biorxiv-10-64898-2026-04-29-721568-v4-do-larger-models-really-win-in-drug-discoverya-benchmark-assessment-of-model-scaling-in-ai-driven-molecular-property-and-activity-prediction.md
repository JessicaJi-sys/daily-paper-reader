---
title: Do Larger Models Really Win in Drug Discovery?A Benchmark Assessment of Model Scaling in AI-Driven Molecular Property and Activity Prediction
title_zh: 更大模型真的在药物发现中更胜一筹吗？AI驱动的分子性质与活性预测中模型规模的基准评估
authors: "Guo, J., Ding, S."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.29.721568v4.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: LLM在药物性质预测中的基准评估，与LLM+DDI相关
tldr: "针对大型模型在药物发现中是否必然优于经典小模型的假设，构建了涵盖26个ADME/毒性/活性终点、165541个分子记录的基准，比较经典机器学习、图神经网络、预训练分子序列模型和大型语言模型。在156个比较中经典ML取得47.4%最优表现，GNN和序列模型在困难拆分下有竞争力但优势受训练设置影响。结果表明预测性能取决于模型与任务的匹配而非单纯规模，经典小模型仍非常有效。"
source: biorxiv
selection_source: fresh_fetch
motivation: 验证大型预训练模型是否在分子属性预测中全面超越经典小模型，纠正“规模越大越好”的片面认识。
method: 构建含26个终点、3种拆分协议的基准，比较经典ML、GNN、预训练序列模型和LLM在165541个分子记录上的表现。
result: "经典ML以47.4%最优占比领先，GNN和序列模型在困难拆分中部分胜出但受训练设置影响，LLM表现最差。"
conclusion: 模型规模化并非万能，紧凑专用模型仍高效，大型模型在低数据情境更有价值，预测需匹配模型、任务与验证场景。
---

## 摘要
分子基础模型与大语言模型(LLMs)的快速发展，催生了药物发现中AI领域以规模为中心的观点，即期望更大的预训练模型能够取代基于经典机器学习（经典ML）和针对单个任务训练的图神经网络（GNNs）的紧凑型化学信息学模型。我们在26个端点（分为ADME、毒性和生物活性三类）上检验了这一假设，涵盖了165,541条端点级化合物标签记录。该基准包含78个端点和划分条目，对应于在三种划分方案下评估的26个端点：随机划分、Murcko骨架划分以及结构分离的5折交叉验证。按难度从易到难，这些划分近似于对封闭库的回顾性评估、苗头到先导中的骨架扩展，以及新化学类型的库扩展。每个条目贡献两个任务和指标比较，共计156个比较。在这些比较中，经典ML提供了最佳表现条目的最大份额（47.4%），其次是预训练的分子序列模型（28.8%）、GNNs（21.8%）和基于LLM的SAR基线（1.9%）。经典ML主导了随机划分插值，并且总体上是最大的胜出家族。在主要最优保留读出下，GNN和序列模型在选定的更难划分方案中具有竞争力，但它们的严格胜出份额在固定最终窗口读出下下降，表明其中一些收益依赖于训练设置和模型选择。配对Bootstrap分析表明，单个模型间微小的数值差异不应被视为决定性胜利。训练折中的SAR知识改善了许多GPT5.5-SAR和Opus4.7-SAR指标，但并未使基于规则的推理成为监督预测器的普遍替代品。紧凑的专用模型在分子性质和活性预测中仍然非常有效。更大的模型在低数据情境下为SAR解释和推理增加了价值，但预测性能取决于模型、任务和验证场景之间的匹配，而不仅仅是规模本身。

## Abstract
The rapid growth of molecular foundation models and large language models (LLMs) has encouraged a scale centred view of AI in drug discovery, in which larger pretrained models are expected to supersede compact cheminformatics models based on classical machine learning (classical ML) and graph neural networks (GNNs) trained for individual tasks. We test this assumption across 26 endpoints grouped into ADME, toxicity and bioactivity classes, covering 165,541 endpoint level compound label records. The benchmark contains 78 endpoint and split entries, corresponding to 26 endpoints evaluated under three split protocols: random, Murcko scaffold and structure separated 5-fold cross validation (CV). Ordered from easiest to hardest, these splits approximate retrospective evaluation on a closed library, scaffold expansion in hit to lead, and library expansion on novel chemotypes. Each entry contributes two task and metric comparisons, giving 156 comparisons in total. Across these comparisons, classical ML provides the largest share of best performing entries (47.4%), followed by pretrained molecular sequence models (28.8%), GNNs (21.8%) and LLM based SAR baselines (1.9%). Classical ML dominates random split interpolation and remains the largest winner family overall. GNN and sequence models are competitive in selected harder split protocols under the primary optimal held-out readout, but their strict winner shares decrease under a fixed final-window readout, indicating that some of these gains depend on training settings and model selection. Paired bootstrap analyses indicate that small numerical differences between individual models should not be read as decisive victories. SAR knowledge from training folds improves many GPT5.5-SAR and Opus4.7-SAR metrics but does not make rule based reasoning a universal substitute for supervised predictors. Compact specialized models remain highly effective for molecular property and activity prediction. Larger models add value for SAR interpretation and reasoning in low data settings, but predictive performance depends on the fit among model, task and validation scenario, not on scale alone.