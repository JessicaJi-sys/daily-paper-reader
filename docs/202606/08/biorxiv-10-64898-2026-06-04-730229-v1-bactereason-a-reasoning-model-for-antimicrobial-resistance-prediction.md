---
title: "BacteReason: A Reasoning Model for Antimicrobial Resistance Prediction"
title_zh: BacteReason：用于抗菌药物耐药性预测的推理模型
authors: "Oikawa, Y., Kawashima, S., Kinjo, A. R., Demizu, Y., Tamura, R., Tsuda, K."
date: 2026-06-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.730229v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 使用大语言模型和知识图谱进行抗菌药物耐药性预测，类似药物相互作用
tldr: "抗菌素耐药性（AMR）快速蔓延，现有机器学习预测缺乏机制解释而可信度低。本文提出BacteReason，一个基于大型语言模型的推理模型，不仅预测细菌对抗生素的敏感性，还提供分子机制理由。该模型通过微调开源LLM，利用临床数据及由教师模型生成的理由进行训练，教师模型借助TogoMCP访问知识图谱。在泛化测试中，BacteReason准确率相对未调基线提升43%，表明推理监督显著提升预测性能，增强了模型的可信度与实用性。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有AMR预测模型因缺乏机制可解释性而可信度低，迫切需要具备推理能力的可解释模型。
method: 微调开源LLM，使用临床数据与教师模型生成的分子机制理由，并结合知识图谱证据进行训练。
result: "在泛化基准上，BacteReason准确率相对未调基线提升43%，相对无理由微调提升38%。"
conclusion: 推理监督可有效提升AMR预测的准确性和可解释性，为临床决策提供可信支持。
---

## 摘要
抗菌药物耐药性（AMR）的快速全球蔓延给临床决策带来了前所未有的压力。存在基于机器学习对抗菌药物敏感性进行预测的方法，但这些方法缺乏机制基础，限制了其可信度。我们提出了BacteReason，一个能够预测细菌对目标抗菌药物敏感性并提供机制依据的推理型大型语言模型（LLM）。BacteReason通过在临床敏感性数据上微调一个开放权重的LLM获得，这些数据附带了解释分子机制的理由。这些理由由一个专有教师LLM生成，该模型被提示解释已知的敏感性结果。教师模型通过TogoMCP与一组生物医学知识图谱数据库接口连接，从而将每个推理步骤建立在检索到的证据基础上。在一个外推基准测试中，BacteReason相较于未调优的基线模型相对改进43%，相较于在同一基础LLM上未使用理由进行微调的模型改进38%，表明推理监督提高了预测准确性。

## Abstract
The rapid global spread of antimicrobial resistance (AMR) has placed unprecedented pressure on clinical decision-making. Machine learning predictors of antibiotic susceptibility exist, but their lack of mechanistic grounding limits credibility. We present BacteReason, a reasoning large language model (LLM) that predicts bacterial susceptibility to a target antibiotic, together with a mechanistic rationale. BacteReason is obtained by fine-tuning an open-weight LLM on clinical susceptibility data augmented with rationales that explain the molecular mechanisms. These rationales are produced by a proprietary teacher LLM prompted to explain known susceptibility outcomes. The teacher is interfaced via TogoMCP with a collection of biomedical knowledge-graph databases, grounding each reasoning step in retrieved evidence. On an extrapolation benchmark, BacteReason achieves a relative improvement of 43% over the untuned baseline and 38% over the same base LLM fine-tuned without rationales, demonstrating that reasoning supervision improves prediction accuracy.