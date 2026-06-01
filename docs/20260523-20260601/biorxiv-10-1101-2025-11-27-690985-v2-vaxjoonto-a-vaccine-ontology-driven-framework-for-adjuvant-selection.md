---
title: "VaxjoOnto: A Vaccine Ontology-driven Framework for Adjuvant Selection"
title_zh: VaxjoOnto：一种基于疫苗本体论的佐剂选择框架
authors: "He, Y., Zheng, Y."
date: 2026-05-27
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.27.690985v2.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 知识图谱用于药物-佐剂匹配，类似药物相互作用预测
tldr: "疫苗佐剂选择是开发瓶颈，现有计算多聚焦抗原发现。VaxjoOnto将疾病-佐剂匹配视为异构知识图谱上的top-k推荐任务，集成事实、通路和文本证据，采用列表排序图神经网络训练。在公开基准上，对已知疾病NDCG@10达0.59，未知疾病达0.27，较随机基线提升5.4倍。该框架提供基于本体的佐剂优先级排序，补充抗原发现工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有计算工具多关注抗原发现，缺乏针对佐剂选择的系统性方法，疾病与佐剂匹配效率低。
method: 基于生物医学本体构建异构知识图谱，使用图神经网络和列表排序损失进行疾病-佐剂匹配推荐。
result: "VaxjoOnto在已知疾病上NDCG@10为0.59，未知疾病上为0.27，比随机基线高5.4倍。"
conclusion: 提出一种本体驱动的佐剂优先级框架，可有效补充现有抗原发现工具，提升疫苗开发效率。
---

## 摘要
选择有效的佐剂仍然是疫苗开发中的一个瓶颈，但大多数计算工作针对的是抗原发现而非佐剂优先排序。我们将疾病-佐剂匹配建模为基于生物医学本体论的异构知识图谱上的top-k推荐任务，整合了策展事实、机制通路和文本证据。我们提出了VaxjoOnto，一种使用列表排序目标训练的图神经网络。在公开基准测试中，VaxjoOnto在已知疾病上的NDCG@10达到0.59，在未见疾病上达到0.27（比随机基线提高5.4倍）。该框架提供了一种基于本体论的佐剂优先排序方法，补充了现有的以抗原为中心的工具。

## Abstract
Selecting an effective adjuvant remains a bottleneck in vaccine development, but most computational efforts have targeted antigen discovery rather than adjuvant prioritization. We frame disease-adjuvant matching as a top-k recommendation task on a heterogeneous knowledge graph grounded in biomedical ontologies, integrating curated facts, mechanistic pathways, and textual evidence. We introduce VaxjoOnto, a graph neural network trained with a listwise ranking objective. On a public benchmark, VaxjoOnto achieves NDCG@10 of 0.59 on seen diseases and 0.27 on previously unseen diseases (a 5.4x improvement over a random baseline). The framework provides an ontology-anchored approach to adjuvant prioritization that complements existing antigen-focused tools.