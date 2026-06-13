---
title: Scaling SMILES-Based Chemical Language Models for Therapeutic Peptide Engineering
title_zh: 基于SMILES的化学语言模型在治疗性多肽工程中的规模化应用
authors: "Feller, A. L., Secor, M., Swanson, S., Wilke, C. O., Deibler, K."
date: 2026-06-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.06.697994v4.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 化学语言模型用于治疗性肽工程，可直接应用于涉及肽的药物相互作用预测
tldr: 治疗性肽兼具蛋白高特异性和小分子化学多样性，但现有蛋白模型限于天然氨基酸，化学模型难以处理聚合物序列。为此开发了基于SMILES的化学语言模型PeptideCLM-2，在超1亿分子上训练，原生表示复杂肽化学。基准测试表明，预测膜扩散、生物学功能和半衰期等开发终点性能优于以往方法。该工作填补了治疗性肽的计算盲区，扩展了机器学习模型工具包。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有蛋白和化学模型无法有效处理治疗性肽，导致依赖静态描述符或定制多嵌入管道。
method: 提出PeptideCLM-2，基于SMILES的化学语言模型，在超过1亿分子上训练。
result: 在预测膜扩散、生物学功能和半衰期等开发终点上，性能优于现有方法。
conclusion: PeptideCLM-2扩展了治疗性肽的机器学习模型工具包，弥合了计算盲区。
---

## 摘要
治疗性多肽在药物发现中占据独特的中介地位，兼具蛋白质相互作用的高特异性和小分子的化学多样性，但目前却处于计算盲区。现有基础模型无法有效处理它们：蛋白质模型局限于天然氨基酸，而化学模型难以处理大型类聚合物序列。这种脱节迫使该领域不得不依赖静态化学描述符（无法捕捉细微化学细节）或针对特定数据集定制的复杂多嵌入流程。为填补这一空白，我们提出PeptideCLM-2，这是一套基于超过1亿分子训练的化学语言模型，能够原生表征复杂的多肽化学。该建模方法扩展了治疗性多肽的机器学习模型工具包。基准测试结果显示，在预测膜扩散、生物功能和半衰期等开发终点指标方面，该方法相较于先前方法表现出强劲性能。

## Abstract
Therapeutic peptides occupy a unique middle ground in drug discovery, offering the high specificity of protein interactions with the chemical diversity of small molecules, yet they currently fall in a computational blind spot. Existing foundation models cannot handle them effectively: protein models are restricted to natural amino acids, while chemical models struggle to process large, polymer-like sequences. This disconnect has forced the field to rely on static chemical descriptors that fail to capture subtle chemical details or on complex multi-embedding pipelines that are custom tailored to specific datasets. To bridge this gap, we present PeptideCLM-2, a suite of chemical language models trained on over 100 million molecules to natively represent complex peptide chemistry. This modeling approach expands the available toolkit of machine learning models for therapeutic peptides. Benchmarking results show strong performance versus prior methods for predicting development endpoints including membrane diffusion, biological function, and half life.

TOC Graphic

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=111 SRC="FIGDIR/small/697994v4_ufig1.gif" ALT="Figure 1">
View larger version (51K):
org.highwire.dtl.DTLVardef@d8c6cborg.highwire.dtl.DTLVardef@1e34211org.highwire.dtl.DTLVardef@1066e22org.highwire.dtl.DTLVardef@128a7d7_HPS_FORMAT_FIGEXP  M_FIG C_FIG