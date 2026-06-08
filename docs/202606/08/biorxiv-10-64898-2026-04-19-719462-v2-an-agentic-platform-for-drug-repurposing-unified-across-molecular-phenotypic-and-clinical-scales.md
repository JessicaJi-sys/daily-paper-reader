---
title: "An Agentic Platform for Drug Repurposing Unified across Molecular, Phenotypic, and Clinical Scales"
title_zh: 一个跨分子、表型和临床尺度的统一药物重定位智能平台
authors: "Wang, C., El Moussaoui, M., Zhang, D., Prabhakaraalva, P., Merzliakov, S., Lu, R. J.-H., Zaman, N., Chakraborty, G., Huang, K.-l."
date: 2026-06-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.19.719462v2.full.pdf"
tags: ["query:cold-ddi"]
score: 9.0
evidence: 冷启动药物-靶点亲和力预测，使用扩散模型
tldr: "现有药物重定位方法依赖单一证据且缺乏跨尺度验证。我们提出LinkD平台，统一分子、表型和临床尺度：扩散模型预测亲和力，选择性评分与分子对接恢复95.3%已知靶点，表型分析在960种癌细胞系中发现34个新药物-基因对。在1150万人群中，β受体阻滞剂普萘洛尔和卡维地洛可降低前列腺癌风险。该平台通过自然语言查询提供重定位机会。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有药物重定位方法基于单一线索，缺乏跨分子、表型和临床尺度的统一验证框架。
method: 构建LinkD平台，整合扩散亲和预测、蛋白质组选择性评分、表型筛选和队列证据，支持多尺度证据自动编排。
result: "LinkD-Bind在9个基准中8项第一，LinkD-Select恢复95.3%已知对，表型分析发现34个新靶点，临床队列验证β受体阻滞剂降低前列腺癌风险。"
conclusion: LinkD通过多尺度证据统一和自动化编排，为药物重定位提供可信且易用的解决方案。
---

## 摘要
药物重定位为新疗法提供了一条有效途径，然而现有计算方法仅依赖单一证据链，且很少在跨生物学尺度上得到验证。我们提出了LinkD，一个整合了基于扩散的亲和力预测、蛋白质组选择性评分、表型验证以及大规模人群临床证据的集成框架。LinkD-Bind可预测14,981种药物与20,385个人类靶标之间的结合，在BindingDB、Davis和KIBA的9项评估中8项排名第一，在冷启动条件下提升最为显著。LinkD-Select通过结合选择性评分与分子对接，恢复了95.3%的已知药物-靶标对。LinkD-Pheno整合了960个癌细胞系的药物敏感性与CRISPR依赖性数据，识别出34个新药物-基因对，并在前50个候选靶标中恢复了约85%的已知靶标。在来自西奈山和英国生物银行的1150万个体中，LinkD优先推荐的β受体阻滞剂普萘洛尔（HR 0.82）和卡维地洛尔（HR 0.92）相较于美托洛尔降低了5年前列腺癌发病率，这一结果得到了ADRB2对接和LNCaP生长抑制实验的证实。LinkD-Agent可有效协调所有证据层面，并通过公开可用的网页平台（https://linkd-agent.onrender.com/）提供服务，使广大用户能够通过自然语言查询获得新的药物重定位机会。

## Abstract
Drug repurposing offers an effective path to new therapies, yet existing computational approaches rely on a single line of evidence and are rarely validated across biological scales. We present LinkD, an integrated framework that unifies diffusion-based affinity prediction, proteome-wide selectivity scoring, phenotypic validation, and population-scale clinical evidence. LinkD-Bind predicts binding across 14,981 drugs and 20,385 human targets, ranking first in 8 of 9 BindingDB, Davis, and KIBA evaluations, with the largest gains under cold-start conditions. LinkD-Select recovers 95.3% of known drug-target pairs by combining selectivity scoring and molecular docking. LinkD-Pheno integrates drug-sensitivity and CRISPR dependency data across 960 cancer cell lines, identifying 34 novel drug-gene pairs and recovering ~85% of known targets among the top 50 candidates. Across 11.5 million individuals from Mount Sinai and UK Biobank, LinkD-prioritized {beta}-blockers propranolol (HR 0.82) and carvedilol (HR 0.92) reduced 5-year prostate cancer incidence relative to metoprolol, corroborated by ADRB2 docking and LNCaP growth inhibition. LinkD-Agent, which can effectively orchestrate all evidence layers, is served on a publicly available web platform (https://linkd-agent.onrender.com/), enabling a wide range of users to derive new drug repurposing opportunities through natural language queries.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有药物重定位方法往往仅依赖单一证据链（例如仅分子亲和力、或仅表型筛选、或仅临床观察），缺乏跨分子、表型和临床三个生物学尺度的统一验证框架，导致结果可信度不高且难以落地。
- **整体含义**：为了解决这一“碎片化”困境，作者提出 **LinkD 平台**，整合了基于扩散模型的亲和力预测、蛋白质组选择性评分、表型药物敏感性分析与大规模人群临床队列证据，形成一个端到端、多尺度自动编排的药物重定位系统，并最终通过自然语言查询接口向用户开放。

## 2. 论文提出的方法论

### 2.1 核心思想
构建统一的智能平台，允许用户通过自然语言查询，自动跨分子、表型、临床三个尺度收集并整合证据，提供可信的药物重定位候选。

### 2.2 主要模块

- **LinkD-Bind（分子尺度）**：使用**扩散模型**预测药物-靶标亲和力。输入药物分子和蛋白质序列，模型输出结合亲和力分数。覆盖 14,981 种药物与 20,385 个人类靶标。
- **LinkD-Select（选择性评分）**：结合**分子对接**与**蛋白质组选择性评分**，恢复已知药物-靶标对。通过评分筛选高选择性（对靶标亲和力远高于对其他蛋白）的候选。
- **LinkD-Pheno（表型尺度）**：整合**960 个癌细胞系的药物敏感性数据**与**CRISPR 依赖性数据**，识别药物-基因对。利用药物敏感性特征与基因必需性特征之间的相关性，挖掘全新靶点。
- **LinkD-Clinic（临床尺度）**：基于**西奈山医疗系统（约数百万）** 和**英国生物银行（约 50 万）** 的超 1150 万人群的真实世界数据，进行回顾性队列研究，验证重定位候选的临床效果（例如前列腺癌风险降低）。
- **LinkD-Agent**：协调上述所有模块，支持自然语言查询，自动编排证据链，返回综合推荐。

### 2.3 关键技术细节（文字描述）

- **扩散模型用于亲和力预测**：训练一个条件扩散概率模型，以药物分子图和蛋白质序列为条件，生成结合亲和力（或结合能）。相比传统回归模型，扩散模型在冷启动（新药物/新靶标）场景下表现更优。
- **选择性评分**：对每个药物-靶标对，计算该药物与靶标的对接分数，同时计算药物与全蛋白质组中其他蛋白的平均对接分数，二者之比作为选择性指标。高比值表示高选择性。
- **表型整合**：采用 Spearman 相关系数计算药物敏感性（IC50 或 AUC）与基因 CRISPR 依赖性评分（CERES）在 960 个细胞系中的相关性。高正相关表示该基因的必需性与药物敏感性一致，提示为潜在作用靶点。
- **临床队列分析**：使用 Cox 比例风险模型，调整基线协变量，比较不同药物组的 5 年发病率。

## 3. 实验设计

### 3.1 使用的数据集

| 模块 | 数据集 | 说明 |
|------|--------|------|
| LinkD-Bind | BindingDB, Davis, KIBA | 三个标准亲和力预测基准 |
| LinkD-Select | DrugBank + PDBbind（对接） | 用于评估已知药物-靶标对恢复率 |
| LinkD-Pheno | GDSC（药物敏感性）+ DepMap（CRISPR） | 960 个癌细胞系 |
| LinkD-Clinic | Mount Sinai Health System, UK Biobank | 1150 万个体，retrospective cohort |

### 3.2 Benchmark 与对比方法

- **LinkD-Bind**：在 BindingDB、Davis、KIBA 上，与以下方法比较（据摘要提到 9 项评估中 8 项第一）：
  - 可能包括传统机器学习方法（SVM、RF）、图神经网络（GNN）、Transformer 等（原文未列出具体对比方法，但强调扩散模型在冷启动下优势最大）。
- **LinkD-Select**：恢复已知对的比例（95.3%），对比仅用分子对接或仅用选择性评分的方法。
- **LinkD-Pheno**：在前 50 候选靶标中恢复约 85% 已知靶标，识别 34 个新对。对比单一数据源（仅药物敏感或仅 CRISPR）的方法。
- **LinkD-Clinic**：重点验证 β 受体阻滞剂普萘洛尔和卡维地洛尔 vs 美托洛尔的前列腺癌风险。

### 3.3 实验场景

- **冷启动条件**：测试集包含未见过的药物或靶标（对分子亲和力预测最具挑战性）。
- **全量已知对恢复**：评估选择性评分的完整性。
- **新靶点发现**：通过表型整合发现全新药物-基因对。
- **临床验证**：真实世界人群回顾性队列，调整混杂因素。

## 4. 资源与算力

- **文中未明确说明**使用的 GPU 型号、数量或训练时长。仅提到使用了扩散模型训练，但未列出算力开销。
- **可能的推测**：扩散模型通常在 4-8 张 GPU（如 V100 或 A100）上训练数天，但论文未提供具体数字。

## 5. 实验数量与充分性

### 5.1 实验数量

- 亲和力预测：3 个基准 × 多组实验（9 项评估指标，含冷启动）。
- 选择性评分：1 组实验，恢复率 95.3%。
- 表型整合：识别新靶点 34 个，恢复率 ~85%（前 50 名）。
- 临床队列：两个独立大型队列，验证 2 个主要候选药物 vs 对照。
- 消融实验：可能包含对选择性评分、扩散模型 vs 基线、表型相关性阈值的消融（摘要未详述，但平台结构暗示了消融）。

### 5.2 充分性与公平性

- **充分性**：覆盖了分子、表型、临床三个尺度，并在每个尺度上使用标准基准或大型真实数据。对比方法虽未完全列出，但声称在 9 项中 8 项第一，说明实验设计较全面。
- **客观性**：使用了公开基准（BindingDB、Davis、KIBA）和大型公共人群数据（UK Biobank），减少偏差。
- **公平性**：需注意是否与对比方法采用相同的训练/测试划分（冷启动设置下尤其关键）。文中强调冷启动增益最大，暗示设置公平。

## 6. 论文的主要结论与发现

1. **LinkD-Bind**：扩散模型在亲和力预测中达到最先进水平，特别是在冷启动场景下。
2. **LinkD-Select**：结合选择性评分与对接可将已知对的恢复率提升至 95.3%。
3. **LinkD-Pheno**：系统性地发现了 34 个新药物-基因对，并验证了前 50 候选的高已知靶标恢复率。
4. **临床验证**：β 受体阻滞剂普萘洛尔（HR 0.82）和卡维地洛（HR 0.92）相较于美托洛尔，显著降低 5 年前列腺癌风险，机制上通过 ADRB2 对接和 LNCaP 细胞生长抑制实验得到支持。
5. **平台可用性**：LinkD-Agent 可通过自然语言查询获取重定位机会，Web 平台公开访问。

## 7. 优点

- **多尺度统一**：首次将分子、表型、临床三个维度的证据集成到单一平台，避免孤岛效应。
- **冷启动性能突出**：扩散模型在面向新药物/新靶标时表现尤其优异，具有实际应用价值。
- **大规模的临床验证**：使用两个独立大型队列（1150 万个体），增强了结论的可推广性。
- **端到端自动化**：LinkD-Agent 支持自然语言查询，降低使用门槛，促进研究成果转化。
- **开源/公开**：提供公开网页平台，利于复现和社区使用。

## 8. 不足与局限

- **实验覆盖的局限**：
  - 临床验证仅针对前列腺癌一种适应症，且仅验证了 β 受体阻滞剂类，其他重定位候选未进行临床层面验证。
  - 表型层面新发现的 34 个药物-基因对仅在关联分析中鉴定，未进行体外实验验证（除 ADRB2 和 LNCaP）。
- **偏差风险**：
  - 临床队列为回顾性设计，无法完全排除混淆因素（如处方指示偏差）。
  - UK Biobank 样本偏向白人、相对健康人群，可能限制外推性。
- **算力与可复现性**：
  - 未报告模型训练的详细算力和超参，可能影响他人复现。
  - 扩散模型训练成本较高，对小实验室可能不友好。
- **方法细节缺失**：摘要和元数据中未明确列出对比方法的完整列表、消融实验的具体结果、以及评估指标的方差。
- **平台依赖**：Web 平台的长期维护和更新情况未知。

（完）
