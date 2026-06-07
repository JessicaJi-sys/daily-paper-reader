---
title: "BacteReason: A Reasoning Model for Antimicrobial Resistance Prediction"
title_zh: BacteReason：一种用于抗菌药物耐药性预测的推理模型
authors: "Oikawa, Y., Kawashima, S., Kinjo, A. R., Demizu, Y., Tamura, R., Tsuda, K."
date: 2026-06-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.730229v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 使用LLM和KG进行药物敏感性预测，方法可迁移至冷启动DDI
tldr: "抗菌药物耐药性（AMR）的快速传播给临床决策带来压力，现有机器学习预测缺乏机械基础。本文提出BacteReason，通过微调开放权重大语言模型，利用教师LLM经知识图谱生成的机理理由进行监督训练。在推广泛化基准上，BacteReason相比未调优基线准确率相对提升43%，比无理由微调提升38%。结果表明，引入机理推理监督能显著提升预测准确性，增强模型可信度。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有AMR预测模型缺乏机械解释，限制了临床可信度。
method: 微调开放权重大语言模型，使用教师LLM结合TogoMCP从知识图谱生成机理理由作为训练监督。
result: "在推广泛化基准上，BacteReason相对基线准确率提升43%，相比无理由微调提升38%。"
conclusion: 推理监督能显著提升AMR预测准确性，并增强模型的可解释性。
---

## 摘要
抗菌药物耐药性（AMR）的快速全球传播给临床决策带来了前所未有的压力。存在基于机器学习的抗生素敏感性预测方法，但它们缺乏机制基础，限制了可信度。我们提出BacteReason，这是一种推理型大语言模型（LLM），能够预测细菌对目标抗生素的敏感性，并提供机制解释。BacteReason通过在一个增强有解释分子机制理由的临床敏感性数据上微调开源权重LLM而获得。这些理由由一个专有的教师LLM生成，该教师被提示解释已知的敏感性结果。教师通过TogoMCP与一组生物医学知识图谱数据库接口，将每个推理步骤基于检索到的证据。在外推基准测试中，BacteReason相对于未微调的基线实现了43%的相对改进，相对于没有理由微调的同一基础LLM实现了38%的相对改进，表明推理监督提高了预测准确性。

## Abstract
The rapid global spread of antimicrobial resistance (AMR) has placed unprecedented pressure on clinical decision-making. Machine learning predictors of antibiotic susceptibility exist, but their lack of mechanistic grounding limits credibility. We present BacteReason, a reasoning large language model (LLM) that predicts bacterial susceptibility to a target antibiotic, together with a mechanistic rationale. BacteReason is obtained by fine-tuning an open-weight LLM on clinical susceptibility data augmented with rationales that explain the molecular mechanisms. These rationales are produced by a proprietary teacher LLM prompted to explain known susceptibility outcomes. The teacher is interfaced via TogoMCP with a collection of biomedical knowledge-graph databases, grounding each reasoning step in retrieved evidence. On an extrapolation benchmark, BacteReason achieves a relative improvement of 43% over the untuned baseline and 38% over the same base LLM fine-tuned without rationales, demonstrating that reasoning supervision improves prediction accuracy.