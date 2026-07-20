---
title: "MechAInistic: An LLM-guided Multi-Agent System for Reasoning over Genome-Scale Constraint-Based Metabolic Models"
title_zh: MechAInistic：一种基于LLM引导的多智能体系统，用于对基因组尺度约束代谢模型进行推理
authors: "Loecker, J., Pujara, N., Bryant, W., Puniya, B. L., Packrisamy, P., Hamed, A. A., Helikar, T."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.11.723319v3.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: LLM引导的多智能体系统用于全基因组代谢模型推理
tldr: 大型语言模型在科学推理中可能产生不可验证的流畅输出。为此提出MechAInistic，一种多智能体系统，通过独立的Reviewer智能体监督Architect智能体的规划与执行，所有推理都基于可执行的代谢模型分析而非纯文本。在类风湿关节炎和多发性硬化症的治疗假设生成任务中，MechAInistic能识别代谢重编程并提名候选药物，相比通用LLM系统保留了可审计的计算推理路径。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1697, \"height\": 387}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1692, \"height\": 663}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 723, \"height\": 742}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 906, \"height\": 420}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1661, \"height\": 861}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 864, \"height\": 736}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 683, \"height\": 340}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 971, \"height\": 317}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1705, \"height\": 307}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1555, \"height\": 561}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1712, \"height\": 354}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-05-11-723319-v3/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1715, \"height\": 871}]"
motivation: LLM智能体的输出虽流畅但可能脱离可验证的计算证据，限制其在生物医学假设生成中的可靠性。
method: 构建多智能体系统，包含规划Architect和监督Reviewer，Reviewer根据评分规则评估计划与中间结果，低于阈值时触发重新规划或执行，所有推理基于COBRApy约束代谢模型。
result: 在类风湿关节炎模型中识别线粒体代谢重编程并提名Devimistat；在多发性硬化症模型中提名IDH抑制剂ivosidenib和vorasidenib。
conclusion: MechAInistic通过可审计的计算推理路径，比通用LLM系统更可靠地生成基于模型证据的生物学假设。
---

## 摘要
LLM智能体越来越广泛地用于科学推理，但其流畅的输出可能偏离可验证的计算证据，从而限制了其在生物医学假设生成中的可靠性。我们开发了MechAInistic，一个多智能体系统，其中独立配置的评审智能体在工作流程的每个阶段监督规划架构师智能体，所有推理都基于可执行的机制模型分析，而不仅仅是语言模型文本。评审智能体根据预先指定的评分标准对计划和中间结果进行评分，并在分数低于阈值时触发重新规划或重新执行，从而生成从自然语言问题到模型推导证据和引用文献的可审计链条。我们使用COBRApy在成对的基于约束的代谢模型上实例化该系统，支持路径比较、扰动分析、药物靶点探索以及健康和疾病状态下的文献解读。我们在两个免疫细胞治疗假设生成任务上评估了MechAInistic。对于类风湿关节炎与健康幼稚B细胞模型，它识别了线粒体代谢重编程，并提名Devimistat/CPI-613作为以OGDH为中心的实验性假设。对于多发性硬化症CD4+ Th17与健康模型，它识别出NADP依赖性异柠檬酸脱氢酶作为候选靶点，并提出ivosidenib，以及vorasidenib作为机制互补的替代方案。与通用LLM系统的对比分析表明，合理的生物学叙述可能缺乏可审计的模型基础，而MechAInistic保留了从提示到结果的计算推理路径。

图形摘要

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=83 SRC="FIGDIR/small/723319v3_ufig1.gif" ALT="Figure 1">
查看更大版本（19K）：
org.highwire.dtl.DTLVardef@12ff92dorg.highwire.dtl.DTLVardef@8fff17org.highwire.dtl.DTLVardef@1b47ddeorg.highwire.dtl.DTLVardef@b37bb8_HPS_FORMAT_FIGEXP  M_FIG C_FIG

## Abstract
LLM agents are increasingly used for scientific reasoning, but their fluent-sounding outputs can diverge from verifiable computational evidence, limiting their reliability for biomedical hypothesis generation. We developed MechAInistic, a multi-agent system in which an independently configured Reviewer agent supervises a planning Architect agent at each stage of the workflow, with all reasoning grounded in executable mechanistic-model analyses rather than language-model text alone. The Reviewer scores plans and intermediate results against pre-specified rubrics and triggers re-planning or re-execution when scores fall below threshold, producing an auditable chain from a natural-language question to model-derived evidence and cited literature. We instantiate the system over paired constraint-based metabolic models using COBRApy, supporting pathway comparison, perturbation analysis, drug-target exploration, and literature interpretation across healthy and disease states. We evaluated MechAInistic on two immune-cell therapeutic hypothesis-generation tasks. For rheumatoid arthritis versus healthy naive B-cell models, it identified mitochondrial metabolic rewiring and nominated Devimistat/CPI-613 as an investigational OGDH-centered hypothesis. For multiple sclerosis CD4+ Th17 versus healthy models, it identified NADP-dependent isocitrate dehydrogenase as a candidate target and proposed ivosidenib, with vorasidenib as a mechanistically complementary alternative. Comparator analyses against general-purpose LLM systems showed that plausible biological narratives can lack auditable model grounding, whereas MechAInistic preserves the computational reasoning path from prompt to result.

GRAPHICAL ABSTRACT

O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=83 SRC="FIGDIR/small/723319v3_ufig1.gif" ALT="Figure 1">
View larger version (19K):
org.highwire.dtl.DTLVardef@12ff92dorg.highwire.dtl.DTLVardef@8fff17org.highwire.dtl.DTLVardef@1b47ddeorg.highwire.dtl.DTLVardef@b37bb8_HPS_FORMAT_FIGEXP  M_FIG C_FIG