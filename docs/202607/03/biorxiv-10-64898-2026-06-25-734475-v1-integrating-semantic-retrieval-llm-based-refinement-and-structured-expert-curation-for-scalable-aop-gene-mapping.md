---
title: "Integrating Semantic Retrieval, LLM-based Refinement, and Structured Expert Curation for Scalable AOP Gene Mapping"
title_zh: 整合语义检索、基于大语言模型的精炼与结构化专家审核的可扩展AOP基因映射
authors: "Schaffert, A., Fratello, M., Kangas, K., Torres Maia, M., del Giudice, G., Mobus, L., Accardi, C., Al-Abdulraheem, Z., Campini, L., Galardo, F., Federico, A., Ciancaleoni, G., Juppi, H.-K., Paparella, M., Serra, A., Greco, D."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.25.734475v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 整合LLM细化和语义检索进行生物医学映射
tldr: 毒理基因组学在监管毒理学中的应用受限于从分子响应到机制性解释的转化困难，而AOP框架为转化提供支持但现有方法难以可扩展地将关键事件（KE）映射到基因。本文提出一个AI辅助多步工作流，结合基于嵌入的语义检索、LLM精炼和双专家独立策展与规则整合，生成KE到基因的映射及置信度分数。在AOP-Wiki上应用，覆盖1254个KE和523个AOP，链接15833个人类基因，映射性能优于传统NLP方法且更贴合专家判断。该工作流和资源为毒理基因组学与AOP机制解释搭建了实用桥梁，支持持续更新和未来扩展。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有KE到基因映射依赖人工策展，难以扩展且效率低，限制了AOP框架在毒理基因组学中的大规模应用。
method: 提出语义检索（嵌入相似度）→LLM精炼→双专家独立策展+规则整合的工作流，对KE标题中的基因和蛋白明确基础化，并分配策展理由代码。
result: 在AOP-Wiki生成覆盖1254个KE、523个AOP、15833个人类基因的KE-基因映射资源，相比早期NLP方法性能提升且更符合专家判断。
conclusion: 该工作流实现了可扩展、可更新的AOP-基因映射，为毒理基因组学机制解释提供高质量基础，支持未来整合更多组学层。
---

## 摘要
毒理基因组学可支持监管毒理学，但其应用受限于将分子反应转化为机制性的、与决策相关的解释的难度。不良结局通路（AOPs）为此转化提供了框架，然而组学应用需要将关键事件（KEs）可扩展地映射到分子特征。在此，我们提出一种AI辅助的多步骤KE-基因映射工作流，该工作流利用基于嵌入的语义检索识别候选本体/通路术语，借助大语言模型辅助精炼以过滤这些候选，并通过双独立专家组审核与基于规则的整合来最终确定映射并得出置信度分数。与早期基于NLP的方法相比，该工作流提高了KE到本体/通路的映射性能，生成的候选注释更符合专家判断，同时显著减少了手动扩充的需求。此外，对KE标题中明确提到的基因和蛋白质进行基础化处理以提高特异性，并为每个审核后的映射分配审核者原因代码，以支持透明、可追踪且考虑置信度的复用。将该工作流应用于AOP-Wiki，生成了一个涵盖523个AOP中1,254个KE并链接15,833个人类基因的综合KE-基因集资源。通过基于CTD的策划参考化学组AOP指纹图谱展示了其实用性，突出了在AOP背景下化学相关基因签名的扩展覆盖和基于置信度的解释。该工作流及所得资源为毒理基因组学与基于AOP的机制解释之间架起了实用桥梁，并支持常规更新及未来扩展到OECD Omics2AOP中的其他组学层面。

## Abstract
Toxicogenomics can support regulatory toxicology, but its use is limited by the difficulty of translating molecular responses into mechanistic, decision-relevant interpretations. Adverse Outcome Pathways (AOPs) provide a framework for this translation, yet omics applications require scalable mapping of Key Events (KEs) to molecular features. Here, we present an AI-assisted, multi-step workflow for KE-to-gene mapping that uses embedding-based semantic retrieval to identify candidate ontology/pathway terms, large language model-assisted refinement to filter these candidates, and double-independent expert group curation with rule-based consolidation to finalize mappings and derive confidence scores. Compared with earlier NLP-based approaches, the workflow improves KE-to-ontology/pathway mapping performance and generates candidate annotations that better align with expert judgment while substantially reducing the need for manual augmentation. Explicit gene and protein mentions in KE titles were additionally grounded to improve specificity, and each curated mapping was assigned curator reason codes to support transparent, traceable, and confidence-aware reuse. Applied across AOP-Wiki, the workflow produced a comprehensive KE-to-gene set resource covering 1,254 KEs across 523 AOPs and linking 15,833 human genes. Utility is demonstrated through CTD-based AOP fingerprinting of curated reference chemical groups, highlighting expanded coverage and confidence-informed interpretation of chemical-associated gene signatures in an AOP context. The workflow and resulting resource provide a practical bridge between toxicogenomics and AOP-based mechanistic interpretation and support routine updating and future extension to additional omics layers within OECD Omics2AOP.