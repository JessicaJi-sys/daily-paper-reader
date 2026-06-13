---
title: "CAREPath: Semantic Context-Aware Reasoning Paths with Mechanism-Augmented Embeddings for Drug Repurposing"
title_zh: "CAREPath: 面向药物重定位的语义上下文感知推理路径与机制增强嵌入"
authors: "song, h., bang, d., koo, b., Kim, S., lee, s."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731247v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 使用KG-LLM推理路径进行药物重定位，方法可迁移到冷启动药物相互作用预测
tldr: "生物医学知识图谱在药物重定位中面临深层路径组合爆炸和hub基因噪声问题。CAREPath结合深度优先和广度优先推理，通过语义路径嵌入和机制上下文增强嵌入平衡特异性与可扩展性。在五个知识图谱上最佳AUPRC提升3.8%，尤其稀疏证据下鲁棒性增强。该框架为可解释的机制感知药物重定位提供了新方案。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有KG路径推理过长或过短导致机制推理不准确，需要平衡特异性与上下文恢复。
method: 提出CAREPath，DFS模块编码短路径为语义嵌入，BFS模块构建机制上下文嵌入并通过相似性增强。
result: "在五个生物医学KG上，AUPRC超越18个基线最高提升3.8%，稀疏证据下鲁棒性提升，GO功能一致性增强。"
conclusion: CAREPath作为可解释框架实现可扩展且机制感知的药物重定位。
---

## 摘要
包含药物、基因和疾病的生物医学知识图谱通过基因介导的多跳路径将药物与疾病联系起来，从而支持药物重定位，并实现作用机制推理。然而，更深的遍历并不一定能改善机制推理：长路径组合级数增长，且经常经过枢纽基因，产生无关的基因调控信号，而过度约束或稀疏的路径可能错过更广泛的生物学背景。我们提出CAREPath，这是一个受深度优先搜索和广度优先搜索推理启发的KG-LLM框架，旨在平衡机制特异性、可扩展性和上下文恢复。DFS类模块将遍历限制为短疾病-基因-药物路径，将每条路径转换为结构化提示，并使用生物医学语言模型编码以生成语义路径嵌入。作为补充，BFS类模块从一跳基因邻域构建实体级机制上下文嵌入，并通过使用药理学相关药物和基因特征相似疾病的相似性引导增强来丰富嵌入。在五个生物医学知识图谱上，CAREPath在18个基线中实现了最佳的整体AUPRC，性能提升高达3.8%。进一步分析表明，语义短路径编码对性能贡献最大，而机制上下文增强提高了稀疏证据下的鲁棒性，并增强了基因本体功能一致性。案例研究和最近FDA批准的适应症进一步证明了其实用相关性，使CAREPath成为可解释的可扩展且机制感知的药物重定位框架。源代码可在https://github.com/hamppy-song/CAREPath获取。

## Abstract
Biomedical knowledge graphs (BKGs) that include drugs, genes, and diseases support drug repurposing by connecting drugs to diseases through gene-mediated multi-hop paths, thereby enabling mechanism-of-action reasoning. However, deeper traversal does not necessarily improve mechanistic reasoning: long paths grow combinatorially and frequently pass through hub genes, producing irrelevant gene regulatory signals, whereas overly constrained or sparse paths may miss broader biological context. We propose CAREPath, a KG-LLM framework inspired by depth-first search (DFS)-like and breadth-first search (BFS)-like reasoning to balance mechanistic specificity, scalability, and context recovery. The DFS-like module constrains traversal to short disease-gene-drug paths, converts each path into a structured prompt, and encodes it with a biomedical language model to generate semantic path embeddings. Complementarily, the BFS-like module constructs entity-level mechanism-context embeddings from one-hop gene neighborhoods and enriches them through similarity-guided augmentation using pharmacologically related drugs and gene-signature-similar diseases. Across five biomedical KGs, CAREPath achieves the best overall AUPRC among 18 baselines, improving performance by up to 3.8%. Additional analyses show that semantic short-path encoding contributes most to performance, while mechanism-context augmentation improves robustness under sparse evidence and strengthens Gene Ontology functional agreement. Case studies and recently FDAapproved indications further demonstrate its practical relevance, positioning CAREPath as an interpretable framework for scalable and mechanism-aware drug repurposing. Source code is available at https://github.com/hamppy-song/CAREPath.