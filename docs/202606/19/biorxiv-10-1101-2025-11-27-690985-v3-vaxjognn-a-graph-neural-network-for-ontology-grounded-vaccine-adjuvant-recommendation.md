---
title: "VaxjoGNN: A Graph Neural Network for Ontology-Grounded Vaccine Adjuvant Recommendation"
title_zh: VaxjoGNN：一种基于本体的疫苗佐剂推荐图神经网络
authors: "He, Y., Zheng, Y."
date: 2026-06-18
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.27.690985v3.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 基于知识图谱的未见过疾病（冷启动）佐剂推荐
tldr: "疫苗佐剂选择是开发瓶颈，现有工具多聚焦抗原发现。本文提出VaxjoGNN，基于生物医学本体构建异构知识图谱，将疾病-佐剂匹配视为top-k推荐任务，采用listwise排序训练图神经网络。在公共基准上，对已知疾病NDCG@10达0.59，对未知疾病达0.27（较随机基线提升5.4倍）。该框架为佐剂优先排序提供本体锚定方法，补充抗原发现工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 疫苗开发中佐剂选择困难，但现有计算工具主要针对抗原发现，缺乏佐剂优先排序方法。
method: 构建基于本体的异构知识图谱，整合机制通路与文本证据，使用VaxjoGNN图神经网络以listwise排序目标训练。
result: "在公共基准上，已知疾病NDCG@10为0.59，未知疾病为0.27，较随机基线提升5.4倍。"
conclusion: 提出本体锚定的佐剂优先排序框架，可补充现有抗原发现工具，助力疫苗开发。
---

## 摘要
选择有效的佐剂仍然是疫苗开发的一个瓶颈，但大多数计算工作都集中在抗原发现上，而非佐剂优先级排序。我们将疾病-佐剂匹配视为一个基于生物医学本体的异质知识图谱上的top-k推荐任务，整合了整理的事实、机制通路和文本证据。我们引入了VaxjoGNN，这是一种使用列表级排序目标训练的图神经网络。在一个公共基准测试中，VaxjoGNN在已知疾病上达到了0.59的NDCG@10，在先前未知疾病上达到了0.27（比随机基线提高了5.4倍）。该框架提供了一种基于本体的佐剂优先级排序方法，补充了现有的以抗原为中心的工具。

## Abstract
Selecting an effective adjuvant remains a bottleneck in vaccine development, but most computational efforts have targeted antigen discovery rather than adjuvant prioritization. We frame disease-adjuvant matching as a top-k recommendation task on a heterogeneous knowledge graph grounded in biomedical ontologies, integrating curated facts, mechanistic pathways, and textual evidence. We introduce VaxjoGNN, a graph neural network trained with a listwise ranking objective. On a public benchmark, VaxjoGNN achieves NDCG@10 of 0.59 on seen diseases and 0.27 on previously unseen diseases (a 5.4 times improvement over a random baseline). The framework provides an ontology-anchored approach to adjuvant prioritization that complements existing antigen-focused tools.