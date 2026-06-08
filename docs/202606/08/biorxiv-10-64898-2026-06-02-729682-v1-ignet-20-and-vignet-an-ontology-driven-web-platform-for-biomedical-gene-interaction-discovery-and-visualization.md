---
title: "Ignet 2.0 and Vignet: An Ontology-Driven Web Platform for Biomedical Gene Interaction Discovery and Visualization"
title_zh: Ignet 2.0 与 Vignet：面向生物医学基因相互作用发现与可视化的本体驱动网络平台
authors: "Asaduzzaman, S., Bansal, B., Combs, P., Zhang, J., Rehana, H., McGregor, B., He, Y., Hur, J."
date: 2026-06-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729682v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 基于本体的基因相互作用和药物关联平台，使用BioBERT，可视化知识图谱
tldr: 生物医学文献激增，亟需系统性、本体驱动的基因交互与疫苗机制发现工具。Ignet 2.0和Vignet双平台通过PubMed文本挖掘、BioBERT评分、集成INO/VO/HDO本体和DrugBank，实现基因-基因交互证据检索、基因集富集、AI摘要生成及疫苗专有探索。关键结果包括VacPair评分、VacNet疫苗-基因-药物-疾病网络构建，并提供REST API与MCP接口。该平台免费开放，支持实时数据集成，但用户需注意验证滞后性。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有平台（如STRING、DisGeNET）缺乏统一的本体驱动系统，无法整合疫苗焦点和AI辅助证据检索。
method: 基于PubMed挖掘，BioBERT对百万基因共现对评分，融合INO、VO、HDO本体及DrugBank；Vignet扩展VO引导的疫苗探索和VacNet网络。
result: Ignet 2.0支持基因对证据检索和BioSummarAI摘要；Vignet实现疫苗交互评分与异质网络可视化，并提供REST API和MCP端点。
conclusion: 平台实现本体引导的基因与疫苗知识发现，实时集成PubMed数据，但依赖已有文献，最新实验数据可能存在滞后。
---

## 摘要
背景：生物医学文献的扩展要求系统性的本体引导的基因相互作用、疫苗机制、药物关联和不良事件发现。现有平台如STRING、DisGeNET和PubTator未能提供一个统一的、免费可访问的系统，该系统整合了基于本体的语义相互作用分类、以疫苗为中心的异质性网络构建以及人工智能辅助的证据检索。结果：Ignet 2.0 和 Vignet 是免费可访问的双平台系统，结合了PubMed文献挖掘、基于BioBERT的数百万基因-基因共现对的相互作用评分，并整合了三个生物医学本体和一个整理药物资源：相互作用网络本体（INO）、疫苗本体（VO）、人类疾病本体（HDO）和DrugBank。Ignet 2.0 支持基因相互作用发现、BioBERT评分的基因对证据的基因集富集检索，以及通过BioSummarAI进行的人工智能辅助摘要。Vignet 通过VO引导的疫苗探索、VacPair相互作用评分以及在VacNet中创建疫苗、基因、药物和疾病网络扩展了这些功能。一个公共的表述状态转移应用编程接口（REST API）和模型上下文协议（MCP）端点支持实时集成，增强了对生物医学知识发现的信任。结论：Ignet 2.0 和 Vignet 是可扩展的、本体引导的生物医学知识平台，促进了基于证据的基因相互作用分析、以疫苗为中心的语义探索和人工智能辅助的知识发现。其实时PubMed数据集成确保了最新洞见；但用户应考虑验证过程和整合最新实验数据的潜在延迟，这可能影响即时数据的可靠性。可用性：Ignet 2.0：https://ignet.org/ignet；Vignet：https://ignet.org/vignet/

## Abstract
Background: The expansion of biomedical literature demands systematic ontology-guided discovery of gene interactions, vaccine mechanisms, drug associations, and adverse events. Existing platforms such as STRING, DisGeNET, and PubTator fall short of providing a unified, freely accessible system that integrates ontology-based semantic interaction classification, vaccine-focused heterogeneous network construction, and Artificial Intelligence-assisted evidence retrieval. Results: Ignet 2.0 and Vignet are freely accessible dual-platform systems that combine PubMed literature mining, BioBERT-based interaction scoring for millions of gene-gene co-occurrence pairs and integrate three biomedical ontologies and one curated drug resource, Interaction Network Ontology (INO), Vaccine Ontology (VO), Human Disease Ontology (HDO), and DrugBank. Ignet 2.0 supports gene interaction discovery, gene set enrichment retrieval of BioBERT-scored GenePair evidence, and AI-assisted summarization through BioSummarAI. Vignet extends these features with VO-guided Vaccine Exploration, VacPair interaction scoring, and the creation of vaccine, gene, drug, and disease networks in VacNet. A public Representational State Transfer Application Programming Interface (REST API) and Model Context Protocol (MCP) endpoint enable real-time integration, fostering trust in biomedical knowledge discovery. Conclusion: Ignet 2.0 and Vignet are scalable, ontology-guided biomedical knowledge platforms that facilitate evidence-based gene interaction analysis, vaccine-focused semantic exploration, and AI-assisted knowledge discovery. Their real-time PubMed data integration ensures up-to-date insights; however, users should consider validation processes and potential lags in incorporating the latest experimental data, which may affect the reliability of immediate data. Availability: Ignet 2.0: https://ignet.org/ignet; Vignet: https://ignet.org/vignet/