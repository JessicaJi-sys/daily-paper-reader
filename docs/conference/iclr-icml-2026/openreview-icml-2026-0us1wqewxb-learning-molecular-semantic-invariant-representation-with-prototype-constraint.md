---
title: Learning Molecular Semantic Invariant Representation with Prototype Constraint
title_zh: 基于原型约束的分子语义不变表示学习
authors: "Zhiqiang Li, Jianqing Liang, Zhiqiang Wang, Xizhao Luo, Jiye Liang"
date: 2026-04-30
pdf: "https://openreview.net/pdf/0411a143ba0a735554d14de38bb9c101d4c739a5.pdf"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 面向OOD泛化的分子语义不变表示
tldr: 分子表示学习在性质预测上进步显著，但训练数据仅覆盖部分化学空间，导致模型依赖环境相关因素，在骨架或功能组成变化时难以迁移。本文提出MoSIR，将纠缠的分子嵌入投影到可学习的语义原型空间，提取语义不变表示并隔离环境敏感变异。基于该分解进行优化以提升分布外泛化。该工作为稳定药物泛化的不变表示学习提供了直接可借鉴的方法。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 训练数据仅覆盖有限化学空间，模型依赖环境相关因素，在化学结构变化时OOD泛化困难。
method: 提出MoSIR，将分子嵌入投影到可学习语义原型空间，提取不变表示并隔离环境敏感变异。
result: 该分解优化提升了分子性质预测的分布外泛化能力。
conclusion: 为稳定药物泛化的不变表示学习提供了有效范式。
---

## Abstract
Molecular representation learning has achieved remarkable progress in molecular property prediction, yet out-of-distribution (OOD) generalization remains challenging. In practice, training data typically cover only a limited portion of the chemical space, causing models to rely on environment-dependent factors that fail to transfer when scaffold structures or functional compositions shift. To address this issue, we propose MoSIR, a framework for learning molecular semantic invariant representation with prototype constraint, which projects entangled molecular embeddings into a learnable semantic prototype space to extract semantic invariant representation while isolating environment-sensitive variations. Building upon this decomposition, we optimize a bi-level min-max objective that introduces representation perturbations to simulate plausible environment shifts and enforce semantic stability. We further provide theoretical guarantees for MoSIR by deriving an OOD generalization bound under distribution shifts. Extensive experiments on multiple molecular OOD benchmarks demonstrate that MoSIR consistently outperforms strong baselines across diverse shift settings, and qualitative analyses confirm that the learned prototypes capture meaningful chemical semantics.

---

## 论文详细总结（自动生成）

# 论文总结：基于原型约束的分子语义不变表示学习（MoSIR）

> 说明：提供的 PDF 提取文本实际为 OpenReview 浏览器验证页面，未包含论文正文、实验细节或附录。以下总结主要依据论文摘要与元数据生成；凡摘要未明确说明之处，均标注为“未说明/无法确认”。

## 1. 核心问题与整体含义

- **研究背景**：分子表示学习在分子性质预测上已取得显著进展，但**分布外（OOD）泛化**仍是关键难题。
- **核心问题**：实际训练数据通常只覆盖有限化学空间，导致模型依赖**环境相关因素**；当分子骨架结构或功能组成发生变化时，模型难以迁移。
- **整体含义**：论文提出 **MoSIR**，试图学习分子语义不变表示，将“语义不变”与“环境敏感变异”分离，从而提升分子性质预测在分布偏移下的稳定性。
- **应用指向**：元数据指出，该工作为**稳定药物泛化的不变表示学习**提供了可借鉴范式。

## 2. 方法论

- **核心思想**：MoSIR 将纠缠的分子嵌入投影到**可学习的语义原型空间**，从中提取语义不变表示，同时隔离环境敏感变异。
- **关键机制**：
  - 通过原型空间约束，使分子表示向具有化学语义的原型对齐。
  - 将表示分解为“语义不变部分”和“环境敏感部分”，以减少对环境相关因素的依赖。
- **优化目标**：在分解基础上，优化一个**双层 min-max 目标**。
  - 引入表示扰动，用于模拟可能的环境偏移。
  - 通过对抗式/鲁棒式优化，强制语义表示在扰动下保持稳定。
- **理论保证**：论文声称推导了分布偏移下的 **OOD 泛化界**，为 MoSIR 提供理论支撑。
- **算法流程（据摘要概括）**：
  1. 输入分子嵌入；
  2. 将嵌入投影到可学习语义原型空间；
  3. 分离语义不变表示与环境敏感变异；
  4. 构造表示扰动以模拟环境变化；
  5. 通过双层 min-max 优化提升语义稳定性与 OOD 泛化。
- **未说明细节**：原型数量、距离度量、损失函数具体形式、扰动生成方式、训练算法伪代码等，均无法从提供文本确认。

## 3. 实验设计

- **实验场景**：论文称在**多个分子 OOD benchmark** 上进行评估，并覆盖**多种分布偏移设置**。
- **对比方法**：摘要称与**强基线**进行比较，但未列出具体基线名称。
- **评估内容**：
  - 定量评估：MoSIR 在多样偏移设置下持续优于强基线。
  - 定性分析：验证学习到的原型能够捕获有意义的化学语义。
- **具体数据集/ benchmark**：未说明。提供文本未给出数据集名称、划分方式、评价指标、任务类型等。
- **对比方法清单**：未说明。无法确认具体对比了哪些分子表示学习、不变学习或 OOD 泛化方法。

## 4. 资源与算力

- 提供文本与摘要中**未提及**以下信息：
  - GPU 型号与数量；
  - 训练时长；
  - 参数量、计算开销或能耗；
  - 是否使用分布式训练或特定硬件加速。
- 因此，**无法总结算力资源与训练成本**。

## 5. 实验数量与充分性

- 从摘要可知，实验至少包括：
  - 多个分子 OOD benchmark；
  - 多种分布偏移设置；
  - 与强基线的对比；
  - 对学习原型的定性分析。
- 但提供文本**未说明**：
  - 具体实验组数；
  - 消融实验数量与设计；
  - 重复次数、随机种子、统计显著性检验；
  - 基线调参是否公平、是否使用相同数据划分。
- **充分性判断**：若仅依据摘要，实验覆盖了 OOD 评估的主要维度，具有一定说服力；但由于缺少细节，**无法客观判断实验是否充分、公平和可复现**。

## 6. 主要结论与发现

- MoSIR 在多个分子 OOD 基准和不同偏移设置下，**一致优于强基线**。
- 学习到的语义原型能够捕获**有意义的化学语义**。
- 通过原型约束与双层 min-max 分解优化，可提升分子性质预测的**分布外泛化能力**。
- 该工作为稳定药物泛化中的不变表示学习提供了有效范式。

## 7. 优点

- **问题重要**：直指分子表示学习在化学空间偏移下的 OOD 泛化难题。
- **方法思路清晰**：用可学习语义原型空间分离不变语义与环境敏感变异，概念上简洁。
- **优化设计有针对性**：双层 min-max 与表示扰动模拟环境偏移，符合不变学习/鲁棒优化的思路。
- **理论支撑**：声称给出分布偏移下的 OOD 泛化界，增强方法可信度。
- **评估维度较全面**：包含多 OOD benchmark、多偏移设置、强基线对比与定性语义分析。

## 8. 不足与局限

- **材料限制**：当前 PDF 提取文本为验证页面，未包含正文；无法验证方法细节、实验设置与结论可靠性。
- **实验细节缺失**：未列出数据集、基线、指标、消融实验和统计检验，难以判断实验覆盖与公平性。
- **算力与复现性未说明**：缺少 GPU、训练时长、超参数等信息，复现成本未知。
- **理论假设未知**：OOD 泛化界依赖的分布假设、正则条件等未在提供文本中说明，实际适用性无法评估。
- **应用限制**：主要面向分子性质预测与药物泛化；对更广泛化学任务、不同模态数据或极端分布偏移的泛化能力尚不明确。
- **可解释性依赖原型设计**：原型捕获化学语义的结论来自定性分析，其稳定性、可解释性和对超参数的敏感性仍需更多验证。

（完）
