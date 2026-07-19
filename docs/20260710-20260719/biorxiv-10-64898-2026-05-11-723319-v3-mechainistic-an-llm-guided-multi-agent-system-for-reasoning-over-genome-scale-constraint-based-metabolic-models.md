---
title: "MechAInistic: An LLM-guided Multi-Agent System for Reasoning over Genome-Scale Constraint-Based Metabolic Models"
title_zh: MechAInistic：一种LLM引导的多智能体系统，用于在基因组规模约束性代谢模型上进行推理
authors: "Loecker, J., Pujara, N., Bryant, W., Puniya, B. L., Packrisamy, P., Hamed, A. A., Helikar, T."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.11.723319v3.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: LLM引导的多智能体系统用于代谢模型生物医学推理;可迁移至DDI推理
tldr: 大型语言模型用于科学推理时可能产生流畅但不基于计算证据的输出，限制了其在生物医学假设生成中的可靠性。MechAInistic采用多智能体架构，由独立Reviewer监督Architect，所有推理基于COBRApy约束性代谢模型的可执行分析，支持路径比较、扰动分析和药物靶点探索。在类风湿关节炎对比健康B细胞模型中识别出线粒体代谢重编程，并提名OGDH抑制剂Devimistat；在多发性硬化症Th17模型中识别NADP依赖性IDH为候选靶点，提出ivosidenib及vorasidenib作为替代。与通用LLM系统对比，MechAInistic保留了从自然语言问题到模型证据的完整审计链，显著提升了科学推理的可信度与可复制性。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1697, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1692, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 723, \"height\": 742, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 906, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1661, \"height\": 861, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 864, \"height\": 736, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 683, \"height\": 340, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 971, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1705, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1555, \"height\": 561, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1712, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1715, \"height\": 871, \"label\": \"Table\"}]"
motivation: 大型语言模型进行科学推理时容易产生流畅但不基于计算证据的输出，需要将推理过程锚定于可执行的机械模型分析以确保可靠性。
method: MechAInistic采用多智能体架构，由独立Reviewer根据评分规则监督Architect的规划与执行，所有推理基于COBRApy代谢模型的可执行分析。
result: 在类风湿关节炎B细胞模型中发现线粒体代谢重编程并提名Devimistat，在多发性硬化症Th17模型中识别IDH靶点并提出ivosidenib。
conclusion: MechAInistic通过引入审计机制和模型基础推理，避免了纯文本LLM的不可靠性，提升了生物医学假设生成的科学可信度。
---

## 摘要
LLM智能体越来越多地被用于科学推理，但它们流畅的输出可能偏离可验证的计算证据，限制了其在生物医学假设生成中的可靠性。我们开发了MechAInistic，这是一个多智能体系统，其中独立配置的评审智能体在工作流的每个阶段监督规划架构智能体，所有推理都基于可执行的机制性模型分析，而不仅仅是语言模型文本。评审员根据预先指定的评分标准对计划和中间结果进行评分，并在分数低于阈值时触发重新规划或重新执行，从而产生从自然语言问题到模型衍生证据和引用文献的可审计链。我们使用COBRApy在成对的约束性代谢模型上实例化该系统，支持通路比较、扰动分析、药物靶点探索以及健康和疾病状态下的文献解释。我们评估了MechAInistic在两个免疫细胞治疗假设生成任务上的表现。对于类风湿关节炎与健康初始B细胞模型，它识别了线粒体代谢重编程，并提名Devimistat/CPI-613作为以OGDH为中心的实验性假设。对于多发性硬化症CD4+ Th17与健康模型，它识别了依赖NADP的异柠檬酸脱氢酶作为候选靶点，并提出了艾伏尼布（ivosidenib），同时以vorasidenib作为机制性互补的替代方案。与通用LLM系统的对比分析表明，看似合理的生物学叙事可能缺乏可审计的模型基础，而MechAInistic保留了从提示到结果的计算推理路径。

图形摘要

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=83 SRC="FIGDIR/small/723319v3_ufig1.gif" ALT="Figure 1">
查看更大版本（19K）：
org.highwire.dtl.DTLVardef@3d1482org.highwire.dtl.DTLVardef@d9531org.highwire.dtl.DTLVardef@1bdd04dorg.highwire.dtl.DTLVardef@b68190_HPS_FORMAT_FIGEXP  M_FIG C_FIG

## 速览
**TLDR**：LLM智能体在科学推理中可能产生流畅但不可靠的叙述。本文提出MechAInistic，一种LLM引导的多智能体系统，通过Reviewer智能体监督Architect智能体，确保推理基于COBRApy约束性代谢模型的可执行分析。系统在类风湿关节炎与多发性硬化症的免疫细胞治疗假设生成任务中，识别出线粒体代谢重编程及多个靶点候选药物。相比通用LLM系统，MechAInistic提供了从问题到模型结果的完整可审计路径，提升了假设生成的可信度。 \
**Motivation**：现有LLM智能体在科学推理中输出可能偏离可验证计算证据，限制了其在生物医学假设生成中的可靠性。 \
**Method**：提出MechAInistic多智能体系统，包含Reviewer和Architect智能体，所有推理基于COBRApy约束性代谢模型分析，实现可审计推理。 \
**Result**：在类风湿关节炎B细胞模型上识别线粒体代谢重编程并提名Devimistat；在多发性硬化症Th17模型上发现IDH靶点并建议ivosidenib。 \
**Conclusion**：MechAInistic确保从自然语言问题到模型证据的完整可审计推理链，避免纯文本虚构，显著提升了科学推理的可靠性。

---

## Abstract
LLM agents are increasingly used for scientific reasoning, but their fluent-sounding outputs can diverge from verifiable computational evidence, limiting their reliability for biomedical hypothesis generation. We developed MechAInistic, a multi-agent system in which an independently configured Reviewer agent supervises a planning Architect agent at each stage of the workflow, with all reasoning grounded in executable mechanistic-model analyses rather than language-model text alone. The Reviewer scores plans and intermediate results against pre-specified rubrics and triggers re-planning or re-execution when scores fall below threshold, producing an auditable chain from a natural-language question to model-derived evidence and cited literature. We instantiate the system over paired constraint-based metabolic models using COBRApy, supporting pathway comparison, perturbation analysis, drug-target exploration, and literature interpretation across healthy and disease states. We evaluated MechAInistic on two immune-cell therapeutic hypothesis-generation tasks. For rheumatoid arthritis versus healthy naive B-cell models, it identified mitochondrial metabolic rewiring and nominated Devimistat/CPI-613 as an investigational OGDH-centered hypothesis. For multiple sclerosis CD4+ Th17 versus healthy models, it identified NADP-dependent isocitrate dehydrogenase as a candidate target and proposed ivosidenib, with vorasidenib as a mechanistically complementary alternative. Comparator analyses against general-purpose LLM systems showed that plausible biological narratives can lack auditable model grounding, whereas MechAInistic preserves the computational reasoning path from prompt to result.

GRAPHICAL ABSTRACT

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=83 SRC="FIGDIR/small/723319v3_ufig1.gif" ALT="Figure 1">
View larger version (19K):
org.highwire.dtl.DTLVardef@3d1482org.highwire.dtl.DTLVardef@d9531org.highwire.dtl.DTLVardef@1bdd04dorg.highwire.dtl.DTLVardef@b68190_HPS_FORMAT_FIGEXP  M_FIG C_FIG