---
title: "BIFO: A Biological Information Flow Ontology for Directed Propagation in Heterogeneous Biomedical Knowledge Graphs"
title_zh: BIFO：一种用于异构生物医学知识图谱中定向传播的生物信息流本体
authors: "Taylor, D. M., Mohseni Ahooyi, T., Stear, B., Zhang, Y., Lahiri, A. M., Simmons, J. A., Chinwalla, A., Nemarich, C., Callahan, T. J., Silverstein, J. C."
date: 2026-05-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.25.727605v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 用于知识图谱中生物学信号传播的本体，支持药物相互作用预测方法
tldr: "生物医学知识图谱中，并非所有边都能传播生物信号，层次、词汇和统计边可能产生无意义路径。BIFO本体定义了14种实体类和基于G+CH→RNA→P→PW→C→PH→DS的主干流分类，通过可接受性约束和四步协议将原始图转化为仅含可传播边的条件图。在Data Distillery知识图上，33.6M边中保留23.7M（70.7%）为BIFO分类关系，其中13.3M为可传播机制性边，10.5M为不可传播观察关联。BIFO提供图无关的规范，支持方向感知、生物学可解释的传播分析。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有知识图谱传播方法忽略边的生物学可传播性，导致信号沿非生物路径扩散，需明确定义哪些边能传递生物信息。
method: 提出BIFO本体，定义14种实体类和主干流分类，设置可接受性约束，通过四步协议将原始图转化为条件传播图。
result: "在DDKG上，70.7%的边被分类，其中56.2%是可传播机制性边，支持BIFO-PPR通路评分，有效区分机制与观察关系。"
conclusion: BIFO是可复用的生物信息流规范，通过方向感知的边分类，为生物医学知识图谱提供更生物学可解释的传播分析基础。
---

## 摘要
生物医学知识图谱通过多种关系类型连接多种实体类型，从而集成异构数据。对这些图谱进行信号传播的计算分析（随机游走、扩散和消息传递）隐含地假设每条可遍历的边都能携带生物信号。在异构知识图谱中，这很少成立：层级边、词汇边和纯统计边本身并不能定义可允许的有向状态变换，遍历它们会使信号沿着无生物学意义的路径传播。我们提出了生物信息流本体（BIFO），这是一种与图无关的规范，规定了哪些有向变换对于可计算信息流是生物学上可允许的。BIFO定义了十四种实体类、一个围绕主干G+CH [-&gt;]RNA [-&gt;]P [-&gt;]PW [-&gt;]C [-&gt;]PH [-&gt;]DS组织的流类分类、一组可允许性约束，以及一个两级CURIE映射，该映射无需特定模式的代码即可应用于任何其标识符和谓词可通过BIFO映射表解析或扩展的图。一个四步条件化协议将原始属性图转换为条件化传播图，其中仅保留可允许的、方向感知的边。我们在Data Distillery知识图谱（DDKG）上提供了参考实现；将独立于队列、以基因为锚点的子图条件化为BIFO基质，包含3360万条边，其中2370万条（70.7%）被保留为BIFO分类关系，将1330万条传播机制边与1050万条保留但不传播的观察关联明确分开，并确认通路概念被配置为BIFO-PPR通路评分的累积端点。BIFO是知识图谱上信号可计算传播的可允许性规范。它作为开放规范发布，附带版本化映射表和工具，为生物医学知识图谱的生物学可解释、方向感知分析提供了可复用的基质。

## Abstract
Biomedical knowledge graphs integrate heterogeneous data by connecting many entity types through many relationship types. Computational analyses that propagate signal across these graphs (random walks, diffusion, and message passing) implicitly assume that every traversable edge can carry a biological signal. In a heterogeneous KG this is rarely true: hierarchical, lexical, and purely statistical edges do not, by themselves, define an admissible directed state transformation, and traversing them propagates signal along paths that are not biologically meaningful. We present the Biological Information Flow Ontology (BIFO), a graph-agnostic specification of which directed transformations are biologically admissible for computable information flow. BIFO defines fourteen entity classes, a taxonomy of flow classes organized around the backbone G+CH [-&gt;]RNA [-&gt;]P [-&gt;]PW [-&gt;]C [-&gt;]PH [-&gt;]DS, a set of admissibility constraints, and a two-level CURIE mapping that can be applied without schema-specific code to any graph whose identifiers and predicates are resolvable through, or extendable to, the BIFO mapping tables. A four-step conditioning protocol converts a raw property graph into a conditioned propagation graph in which only admissible, direction-aware edges remain. We provide a reference implementation on the Data Distillery Knowledge Graph (DDKG); conditioning a cohort-independent, gene-anchored subgraph as a BIFO substrate of 33.6 million edges retained 23.7 million (70.7%) as BIFO-classified relationships, cleanly separating 13.3 million propagating mechanistic edges from 10.5 million retained-but-non-propagating observational associations, and confirming that pathway concepts are configured as scoring accumulation endpoints for BIFO-PPR pathway scoring. BIFO is an admissibility specification for computable propagation of signal over knowledge graphs. It is released as an open specification with versioned mapping tables and tooling, providing a reusable substrate for biologically interpretable, direction-aware analysis of biomedical knowledge graphs.