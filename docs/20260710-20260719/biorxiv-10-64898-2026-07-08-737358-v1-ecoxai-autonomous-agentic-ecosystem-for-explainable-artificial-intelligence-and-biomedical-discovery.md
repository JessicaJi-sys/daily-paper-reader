---
title: "EcoXAI: Autonomous Agentic Ecosystem for Explainable Artificial Intelligence and Biomedical Discovery"
title_zh: EcoXAI：面向可解释人工智能与生物医学发现的自主智能体生态系统
authors: "Matsumoto, N., Choi, H., Freda, P. J., Hernandez, M. E., Wang, Z. P., Moore, J. H."
date: 2026-07-13
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.08.737358v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 模块化多智能体系统用于生物医学发现
tldr: 生物医学数据复杂异构，研究者难以提取可操作见解。EcoXAI提出模块化容器化多智能体框架，显式集成知识图谱，将分析分解为流水线阶段。在阿尔茨海默病药物重定位中评估103个候选，识别79个新候选（超越随机基线），其中CCR5拮抗剂Maraviroc的假设获文献支持。该框架为临床研究者提供透明、可验证的推理，加速假设驱动生物医学发现。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-08-737358-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1770, \"height\": 773, \"label\": \"Figure\"}]"
motivation: 生物医学数据集与知识图谱日益庞大复杂，现有AI易产生幻觉或碎片化，急需自主分析工具以避免这些缺陷。
method: 采用模块化容器化多智能体架构，显式集成知识图谱，将生物分析分解为明确流水线阶段，实现自主执行与可验证推理。
result: 在阿尔茨海默病药物重定位中评估103个候选，识别79个新候选（超随机基线），其中Maraviroc的假设获文献支持。
conclusion: 知识图谱赋能的智能体系统可提升数据透明性与可验证性，有效加速假设驱动生物医学研究。
---

## 摘要
动机随着生物医学数据集和知识图谱在规模、复杂性和异质性上持续增长，从中导航并提取可操作洞察对研究人员而言成为主要瓶颈。亟需能够利用智能体AI最新进展（如智能体驾驭和循环工程）而不引入幻觉或工作流碎片化的自主分析解决方案。无论技术背景如何，研究人员都需要能简化复杂数据分析、提供基于数据和已有生物医学知识的有意义、可操作洞察的工具。EcoXAI通过引入模块化、可定制、容器化的多智能体系统应对这一挑战，将分析结构化地划分为明确的流水线执行阶段，降低了临床和转化研究人员的计算门槛。

结果EcoXAI用自主执行驱动的框架取代了单体AI文本界面，该框架配备专门的生物信息学智能体，基于已建立的生物学知识提供主动、数据驱动的洞察。与纯LLM驱动或集成度较低的AI解决方案（易产生幻觉或生物学上不合理的结果）不同，EcoXAI的多智能体框架利用了现代智能体管理和显式知识图谱集成，在其推理中提供了更高的透明度和可验证性。在我们针对阿尔茨海默病的药物重定位用例中，EcoXAI评估了103个候选药物，识别出79个新候选药物，其预测模型超越了随机基线，包括CCR5拮抗剂马拉维罗，其生成的假设随后得到了文献支持。这些结果展示了基于知识图谱的AI智能体在加速假设驱动的生物医学研究方面的潜力。

可用性与实现EcoXAI在GitHub上可用：https://github.com/EpistasisLab/EcoXAI。

联系jason.moore@csmc.edu

## Abstract
MotivationAs biomedical datasets and knowledge graphs continue to grow in size, complexity, and heterogeneity, navigating and extracting actionable insights from them presents a major bottleneck for researchers. There is a clear need for autonomous analytical solutions that can utilize recent advancements in agentic AI such as agent harnessing and loop engineering without introducing hallucination or workflow fragmentation. Researchers, regardless of technical expertise, need tools that streamline complex data analysis and deliver meaningful, actionable insights grounded in both data and established biomedical knowledge. EcoXAI addresses this by introducing a modular, customizable, containerized multi-agent system that structures analysis into explicit pipeline execution stages, lowering the computational barrier for clinical and translational researchers.

ResultEcoXAI replaces monolithic AI text interfaces with an autonomous execution-driven framework with specialized bioinformatics agents for delivering proactive, data-driven insights grounded in established biological knowledge. Unlike purely LLM-driven or less integrated AI solutions prone to hallucinations or biologically implausible outcomes, EcoXAIs multi-agent framework, which leverages modern agentic management and explicit knowledge graph integration, provides greater transparency and verifiability in its reasoning. In our use case in drug repurposing for Alzheimers Disease, EcoXAI evaluated 103 drug candidates and identified 79 novel candidates whose predictive models exceeded a randomized baseline, including the CCR5 antagonist Maraviroc, whose generated hypothesis was subsequently supported by the literature. These results demonstrate the potential of knowledge graph-grounded AI agents to accelerate hypothesis-driven biomedical research.

Availability and implementationEcoXAI is available on GitHub at: https://github.com/EpistasisLab/EcoXAI.

Contactjason.moore@csmc.edu