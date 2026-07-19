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

## 速览
**TLDR**：生物医学数据日益庞大复杂，研究人员亟需自主分析工具。EcoXAI构建模块化容器化多智能体系统，集成知识图谱与智能体管理，提供透明可验证的推理。在阿尔茨海默病药物重定位中评估103个候选，发现79个新候选，其中Maraviroc的假设获文献支持。该框架加速了假设驱动的生物医学发现。 \
**Motivation**：解决生物医学数据复杂性和异构性带来的分析瓶颈，降低计算门槛，避免非专家用户的幻觉问题。 \
**Method**：开发模块化、可定制、容器化的多智能体系统，整合知识图谱与循环工程，实现结构化管道执行。 \
**Result**：在阿尔茨海默病药物重定位中，评估103个候选药物，识别79个新候选，预测优于随机基线，Maraviroc假设获文献验证。 \
**Conclusion**：知识图谱引导的AI智能体可提升假设驱动生物医学研究的透明性与可验证性。

---

## Abstract
MotivationAs biomedical datasets and knowledge graphs continue to grow in size, complexity, and heterogeneity, navigating and extracting actionable insights from them presents a major bottleneck for researchers. There is a clear need for autonomous analytical solutions that can utilize recent advancements in agentic AI such as agent harnessing and loop engineering without introducing hallucination or workflow fragmentation. Researchers, regardless of technical expertise, need tools that streamline complex data analysis and deliver meaningful, actionable insights grounded in both data and established biomedical knowledge. EcoXAI addresses this by introducing a modular, customizable, containerized multi-agent system that structures analysis into explicit pipeline execution stages, lowering the computational barrier for clinical and translational researchers.

ResultEcoXAI replaces monolithic AI text interfaces with an autonomous execution-driven framework with specialized bioinformatics agents for delivering proactive, data-driven insights grounded in established biological knowledge. Unlike purely LLM-driven or less integrated AI solutions prone to hallucinations or biologically implausible outcomes, EcoXAIs multi-agent framework, which leverages modern agentic management and explicit knowledge graph integration, provides greater transparency and verifiability in its reasoning. In our use case in drug repurposing for Alzheimers Disease, EcoXAI evaluated 103 drug candidates and identified 79 novel candidates whose predictive models exceeded a randomized baseline, including the CCR5 antagonist Maraviroc, whose generated hypothesis was subsequently supported by the literature. These results demonstrate the potential of knowledge graph-grounded AI agents to accelerate hypothesis-driven biomedical research.

Availability and implementationEcoXAI is available on GitHub at: https://github.com/EpistasisLab/EcoXAI.

Contactjason.moore@csmc.edu

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题**：生物医学数据集和知识图谱规模庞大、复杂且异质，传统分析管道将统计检验、预测建模、通路解读等任务孤立处理；通用AI系统（如纯LLM）易产生幻觉或生物学不合理结果，且缺乏工作流可追溯性。临床和转化研究人员亟需一种能简化分析、降低计算门槛、并提供可解释、可验证见解的自主工具。
- **背景**：现有框架要么是单一对话式AI，要么缺乏与结构化知识图谱的深度集成，导致发现过程碎片化或结果不可靠。EcoXAI旨在通过模块化、容器化多智能体系统，结合现代智能体驾驭（agent harnessing）和循环工程（loop engineering），实现端到端、知识图谱引导的自主科学发现。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：构建一个模块化、可定制的容器化多智能体框架，将生物医学分析分解为明确流水线阶段，并显式集成公共生物知识图谱，从而提供透明、可验证的推理。
- **关键技术细节**：
  - **架构**：基于微服务容器（Docker）实现高可移植性和可重复性。使用规划-编排层（planner-orchestrator）将分析分解为有序步骤：数据摄取、探索性数据分析（EDA）、数据归一化、预测分析、知识图谱引导的假设生成、假设执行和记忆管理。
  - **智能体能力**：LLM通过第三方API或本地部署接入；智能体配备可定制的技能，如数据归一化、EDA、假设生成/测试、知识图谱查询（使用Cypher语言）。
  - **假设生成与评估循环**：系统在每次循环中，结合用户研究问题、数据集信号和知识图谱上下文生成一组多样化的候选假设；然后并行评估所有假设，将已支持的假设存入“发现记忆”（语义向量格式），利用RAG和相似性搜索避免冗余。
  - **知识图谱集成**：对公共知识图谱（如AlzKB）进行自动模式检索、查询并返回路径、基因-疾病关联、药物-靶点关系等，用于引导假设生成和模型输出解释。
  - **假设评估**：针对不同类型假设采用特定评估方法（如预测性假设用模型性能指标，机制性假设用数据集佐证）。文中示例使用AUC对比随机基线（1000个XGBoost模型，随机基因集最多100个基因）。

## 3. 实验设计：使用的数据集、场景、benchmark、对比方法
- **数据集**：
  - **知识图谱**：AlzKB（阿尔茨海默病知识图谱）v1.21，包含基因、疾病、药物等实体及语义关系。
  - **基因型数据**：ADSP R4 v11 2023版本（3.46亿变异，36361样本），经质量控制后使用；GWAS汇总统计来自eMERGE队列；基于基因分数（Gene score = Σ(beta * genotype)/n_variants）计算得到20935个基因在11280个个体上的分数。
- **场景**：药物重定位（Drug Repurposing）用于阿尔茨海默病。
- **Benchmark**：随机基线（1000个XGBoost模型，训练于随机选择的基因集，最多100个基因，计算平均AUC为0.582）。
- **对比方法**：未直接对比其他方法，但提及与“纯LLM驱动或集成度较低的AI解决方案”相比的优势，以及“人类手动建模”的表现（最优模型AUC约0.6143）。主要对比对象为随机基线以及人类手动建模结果（来自Orlenko et al., 2025）。

## 4. 资源与算力
- **LLM**：使用本地部署的**Qwen 3.6 27B模型**，连续运行约**两天**。文中指出若使用Anthropic的Sonnet 4.6 API按token计费将超过300美元。
- **硬件细节**：未明确说明GPU型号、数量或显存。仅提及“本地Qwen 3.6 27B模型”和两年运行时长，表明算力需求中等。

## 5. 实验数量与充分性
- **实验数量**：
  - 针对阿尔茨海默病药物重定位，EcoXAI自主**生成、执行并评估了103个独立假设**（每个假设对应一个候选药物）。
  - 其中**79个候选药物**的模型AUC超过随机基线（0.582）。
  - 针对每个药物，智能体通过多种图遍历策略（直接靶点、一阶/二阶互作、共享生物过程、通路限制子网络等）构建不同基因集，最终选取最优模型。每个模型均通过交叉验证训练XGBoost。
  - 另对Maraviroc案例进行了深入分析（77基因网络、二阶桥接基因评估等）。
- **充分性评估**：
  - **优点**：覆盖了不同药物类别（免疫调节剂、激酶抑制剂、代谢药物、钙通道阻滞剂、GPCR靶向化合物），初步验证了框架的泛化性。且所有假设均在知识图谱中排除已知AD关联基因，增加了新颖性。
  - **不足**：
    1. 仅在一个知识图谱（AlzKB）和一种疾病（AD）上进行了全面测试，未评估在其他知识图谱（如DrugBank、STRING）或其他疾病上的表现。
    2. 未进行消融实验（如去掉知识图谱、去掉记忆模块、不同LLM对比等）。
    3. 对比基线仅设置了随机基因集，未与现有药物重定位方法（如基于网络的方法、传统机器学习基线）系统性对比。
    4. 评估指标仅使用AUC，未包含其他指标（如精确率、召回率、PR曲线等），也未进行统计显著性检验（如置换检验或置信区间）。
    5. 仅展示了一个药物（Maraviroc）的文献验证，未对其它78个候选进行相似验证（可能是由于资源限制），因此对假阳性率的评估不足。

## 6. 论文的主要结论与发现
- **主要结论**：EcoXAI作为一个基于知识图谱的多智能体框架，能够自主完成从EDA、假设生成、模型训练到生物学解释的全流程，在阿尔茨海默病药物重定位中成功识别出79个超越随机基线的候选药物，证明了知识图谱引导的自主AI在加速假设驱动的生物医学研究中的潜力。
- **关键发现**：
  - 直接药物靶点基因集在预测中往往表现不佳（接近或低于随机基线），而扩展的生物学网络（如互作子网络、共享通路）显著提升了预测性能，提示阿尔茨海默病风险更适宜用宽泛网络而非孤立分子靶点表示。
  - 自主发现的Maraviroc假设尽管出发点距离AD已知基因三跳，且明确排除了AD关联基因，仍被已有文献独立支持（CCR5表达升高、CCL5/CCR5轴参与淀粉样蛋白β和tau病理等），表明框架能发现生物学上有意义的机制。

## 7. 优点
- **模块化与可扩展性**：容器化、微服务架构，支持不同LLM（API或本地）、不同知识图谱、用户自定义技能，易于适配新任务。
- **透明性与可追溯性**：每一步（EDA、代码脚本、假设、报告）均持久化，允许研究者中途检验、修改或复现，缓解了“黑箱”问题。
- **知识图谱显式集成**：既为假设生成提供生物学上下文，又可通过结构化查询验证推理路径，减少幻觉。
- **自主循环与记忆机制**：通过语义向量存储和RAG，系统可避免重复假设，并逐步精炼发现过程，展示了持续学习能力。
- **低成本运行**：本地运行27B模型两天即可完成103个假设的评估，成本可控（文中对比API费用>300美元）。

## 8. 不足与局限
- **实验验证不足**：
  - 仅在一个疾病（AD）和一个知识图谱上测试，缺乏跨疾病、跨知识图谱的泛化性评估。
  - 未进行消融实验（如去除知识图谱、去除记忆、不同LLM对比），无法量化各模块贡献。
  - 仅有Maraviroc一个案例获得文献验证，其他78个候选的生物学合理性待实验或文献确认。
  - 评估指标单一（只有AUC），未使用多指标（如精确率、F1、PR-AUC）或统计显著性检验。
  - 与当前主流药物重定位方法（如基于网络、基于图神经网络、传统机器学习集成）没有直接对比，优势难以定量。
- **技术架构限制**：
  - 依赖外部知识图谱的质量和更新频率；若知识图谱不完整或存在偏差，将影响假设质量。
  - 系统对规划错误和级联故障敏感（论文已承认），尽管通过阶段隔离和持久化缓解，但仍需人工监控。
  - 使用LLM作为核心推理引擎，虽然本地化降低了幻觉风险，但LLM本身仍可能产生逻辑跳跃或不合理假设。
- **计算资源描述模糊**：未提供GPU型号、显存、具体训练/推理时长等细节，使得可重复性受影响（只说“本地Qwen 3.6 27B约两天”）。
- **应用限制**：当前版本对用户技术门槛有一定要求（Docker、知识图谱部署、LLM配置），离“零门槛”尚有一定距离。

（完）
