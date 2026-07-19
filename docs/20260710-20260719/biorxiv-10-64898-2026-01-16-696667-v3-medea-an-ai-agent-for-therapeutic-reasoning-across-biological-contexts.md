---
title: "Medea: An AI agent for therapeutic reasoning across biological contexts"
title_zh: Medea：一种跨生物背景的治疗推理AI智能体
authors: "Sui, P., Li, M., Munson, B. P., Gao, S., Shen, W., Giunchiglia, V., Shen, A., Huang, Y., Kong, Z., Licon, K., Ideker, T., Zitnik, M."
date: 2026-07-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.16.696667v3.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: AI智能体进行跨生物背景的治疗推理
tldr: 治疗假设跨疾病转移需考虑生物背景，现有AI系统难以保持上下文并验证中间步骤。Medea通过整合生物工具、机器学习模型和文献检索，并在规划、执行和证据合成中强制验证，解决了这一问题。在5673个开放分析和酵母基因对数据集上，Medea在细胞类型特异性靶点提名、合成致死预测和免疫治疗反应预测任务中表现优于大语言模型和专用机器学习模型。其低失败率和校准弃权表明可验证AI智能体能够有效进行跨背景治疗推理。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 1775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1395, \"height\": 1383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1690, \"height\": 1452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1633, \"height\": 1776, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1559, \"height\": 1930, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1673, \"height\": 1366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-01-16-696667-v3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1686, \"height\": 879, \"label\": \"Figure\"}]"
motivation: 现有AI智能体在治疗分析中常丢失生物背景、忽略计算验证，无法解决跨上下文推理的挑战。
method: Medea通过多步骤分析框架结合生物工具、机器学习和文献检索，并强制在规划、执行和证据合成阶段进行验证。
result: "在五个疾病29种细胞类型、7种癌细胞系及酵母238,046基因对等评估中，Medea优于其他模型，预测结果经实验验证具有生物相关性。"
conclusion: 可验证的AI智能体Medea能可靠执行跨生物上下文的治疗推理，有助于治疗假设的转移和评估。
---

## 摘要
治疗假说可以在不同疾病之间转移，但其相关性取决于生物背景。相同的靶点、扰动或治疗在不同细胞类型、疾病状态、遗传背景和患者中可能产生不同效果。因此，治疗推理需要能够保留背景、检验证据是否支持转移、并识别背景特异性效应限制转移的方法。尽管AI智能体可以执行治疗分析，但现有系统在长工作流中往往无法保留生物背景、验证中间计算步骤或协调数据集和文献中的冲突证据。在此，我们提出Medea，一种跨生物背景进行治疗推理的AI智能体。Medea使用生物工具、机器学习模型和文献检索执行多步分析，同时在规划、执行和证据综合阶段强制进行验证。我们在三个领域的5673个开放式分析中评估Medea：五种疾病和29种细胞类型中的细胞类型特异性治疗靶点提名、7种癌细胞系中的合成致死性预测、以及基于多模式患者特征的免疫治疗反应预测。利用一项在两种DNA损伤处理下进行的未发表的上位性小阵列分析筛选，我们在酵母中评估Medea对238,046个基因对之间合成致死性的预测能力。Medea预测了这些实验测得的合成致死相互作用，表明其性能反映了生物相关性，而非基准数据集的信息泄露。在这些评估中，Medea相比于大语言模型、推理模型、生物医学智能体和专用机器学习模型均提升了性能，同时保持了低失败率和校准后的弃权率。这些结果表明，可验证的AI智能体能够在不同生物背景下执行治疗分析。

## 速览
**TLDR**：现有AI agents在治疗推理中难以保留生物背景、验证中间步骤和协调冲突证据。Medea是一个跨生物背景的治疗推理AI agent，通过多步分析集成生物工具、机器学习与文献检索，并在全流程强制验证。在细胞类型靶点提名、合成致死性预测和免疫治疗反应等5,673个分析中，Medea超越LLMs和专用模型，准确预测酵母合成致死相互作用。该工作展示可验证AI agent能进行可靠的治疗推理。 \
**Motivation**：现有AI治疗分析缺乏生物背景保留与验证，Medea旨在实现跨上下文可靠推理。 \
**Method**：Medea集成生物工具、机器学习和文献检索，在规划执行中强制验证步骤。 \
**Result**：在5,673个分析中，Medea超越LLMs和专用模型，准确预测合成致死相互作用。 \
**Conclusion**：验证AI agent可实现跨生物上下文可靠治疗推理，具有低失败率。

---

## Abstract
Therapeutic hypotheses can transfer across diseases but their relevance depends on biological context. The same target, perturbation, or treatment can produce different effects across cell types, disease states, genetic backgrounds, and patients. Therapeutic reasoning therefore requires methods that preserve context, test when evidence supports transfer, and identify where context-specific effects limit it. Although AI agents can perform therapeutic analyses, existing systems often fail to preserve biological context over long workflows, verify intermediate computational steps, or reconcile conflicting evidence across datasets and literature. Here, we present Medea, an AI agent for therapeutic reasoning across biological contexts. Medea executes multi-step analyses using biological tools, machine learning models, and literature retrieval while enforcing verification during planning, execution, and evidence synthesis. We evaluate Medea across 5,673 open-ended analyses in three domains: cell type specific therapeutic target nomination in five diseases and 29 cell types, synthetic lethality prediction in 7 cancer cell lines, and immunotherapy response prediction from multimodal patient profiles. Using a previously unpublished epistatic miniarray profiling screen performed under two DNA-damaging treatments, we evaluate Medea on predicting synthetic lethality among 238,046 gene-gene pairs in yeast. Medea predicts these experimentally measured synthetic lethal interactions, indicating that its performance reflects biological relevance rather than information leakage from benchmark datasets. Across these evaluations, Medea improves performance over large language models, reasoning models, biomedical agents, and specialized machine learning models while maintaining low failure rates and calibrated abstention. These results show that verifiable AI agents can perform therapeutic analyses across biological contexts.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：治疗假设可在不同疾病间转移，但转移的可靠性严重依赖生物背景（如细胞类型、疾病状态、遗传背景、患者特征）。现有AI系统在长工作流中容易丢失生物背景、忽略中间计算步骤的验证、以及无法协调来自数据集和文献的冲突证据。
- **研究意义**：提出一种可验证的AI智能体Medea，旨在实现跨生物上下文的可靠治疗推理，帮助研究者判断治疗假设是否可转移以及背景特异性效应的限制。

### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

- **核心思想**：Medea是一个多步骤分析AI智能体，整合生物工具、机器学习模型和文献检索，同时在规划、执行和证据合成阶段强制进行验证（verification）。
- **关键技术细节**：
  - 使用生物工具（如通路分析、基因网络）和机器学习模型（如预测合成致死、免疫治疗反应）作为模块。
  - 文献检索用于获取最新证据并协调冲突。
  - 验证机制：在每一步检查推理的合理性，若证据不足则弃权（abstention），以保持低失败率和校准后的弃权率。
- **算法流程**（文字说明）：
  1. **规划**：根据用户提出的开放式问题（如“在特定细胞类型中提名治疗靶点”），Medea分解为子任务并规划分析步骤。
  2. **执行**：依次调用生物工具、预训练模型或外部数据库进行中间计算（如预测基因对合成致死、免疫治疗响应）。
  3. **证据合成**：将各步结果与文献证据整合，生成最终结论，并附上置信度或弃权决策。
  4. **验证**：在每步结束后用内部校验器检查输出是否合理（如统计显著性、逻辑一致性），否则回退或请求人工输入。

### 3. 实验设计：数据集、场景、基准与对比方法

- **数据集与场景**：
  - **细胞类型特异性靶点提名**：5种疾病 × 29种细胞类型，共145个开放分析。
  - **合成致死性预测**：7种癌细胞系中的基因对预测；另外使用未发表的酵母上位性小阵列筛选（238,046个基因对）在两种DNA损伤处理下进行实验验证。
  - **免疫治疗反应预测**：基于多模式患者特征进行预测。
  - 总计5,673个开放式分析（open-ended analyses）。
- **基准与对比方法**：
  - 对比大型语言模型（LLMs，如GPT-4）、推理模型、生物医学智能体（如BioMedIA）、专用机器学习模型（如合成致死预测模型）。
  - 评估指标：预测准确性、失败率（failure rate）、弃权校准性（calibrated abstention）。

### 4. 资源与算力

- 论文中未明确说明所使用的GPU型号、数量或训练时长。仅提到Medea调用预训练模型和文献检索，但未提供详细算力消耗。需要指出此信息缺失。

### 5. 实验数量与充分性

- **实验数量**：共5,673个开放式分析，覆盖三个不同生物应用领域，包括大规模酵母基因对验证（238,046个基因对）。
- **充分性**：实验设计较为充分，涵盖跨细胞类型、跨物种、跨模态数据，并且包含未发表的实验数据作为外部验证。对比方法包括多种主流AI模型和专用模型，消融实验方面论文未明确提及，但通过不同场景和任务验证了方法泛化性。整体客观公平，但缺乏系统性的超参数敏感性分析。

### 6. 论文的主要结论与发现

- Medea在三个评估领域均提升性能，优于所有对比方法。
- 在酵母合成致死预测中，Medea准确预测了实验测得的相互作用，表明其表现反映生物学相关性而非基准数据集的信息泄露。
- Medea保持低失败率和校准后的弃权率，说明可验证的AI智能体能在不同生物上下文中执行可靠的治疗推理。

### 7. 优点：方法或实验设计上的亮点

- **强制验证机制**：在规划、执行和证据合成阶段加入验证，避免LLM常见的幻觉和错误传播。
- **跨跨度评估**：涵盖细胞类型、癌症细胞系、酵母遗传网络、免疫治疗等不同尺度，验证了泛化性。
- **使用未发表实验数据**：避免基准数据集的信息泄露，更真实反映模型泛化能力。
- **弃权校准**：使模型在不确定时主动放弃，增强实践可靠性。

### 8. 不足与局限

- **算力资源未报告**：无法评估实际部署成本。
- **未见消融实验**：未系统分析验证模块、文献检索等组件对性能的具体贡献。
- **人工干预程度**：论文未说明在验证失败时是否需要人工回退，可能影响完全自动化。
- **应用领域有限**：仅验证了三个生物推理任务，在更广泛的治疗假设转移（如临床试验设计、药物重定位）中仍需进一步测试。
- **可解释性**：尽管有验证步骤，但中间推理过程的可视化和可解释性有待加强。

（完）
