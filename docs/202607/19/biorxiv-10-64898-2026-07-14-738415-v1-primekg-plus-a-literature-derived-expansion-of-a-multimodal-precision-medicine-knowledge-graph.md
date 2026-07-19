---
title: "PrimeKG-Plus: a literature-derived expansion of a multimodal precision medicine knowledge graph"
title_zh: PrimeKG-Plus：一个文献驱动的多模态精准医学知识图谱的扩展
authors: "Nguyen, T. T. D., Nguyen-Phuong, T., Nguyen, Q.-H., Abbasi, A. M., Le Phan, H.-D., Nguyen, L. B.-A., Phan, N.-T., Curabaz, N. N., Hauser, A. S., Tanoli, Z., Nguyen, D. T., Kooistra, A. J."
date: 2026-07-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738415v1.full.pdf"
tags: ["query:cold-ddi"]
score: 8.0
evidence: 扩展生物医学知识图谱，包含药物相互作用信息
tldr: 现有疾病知识图谱PrimeKG发布后未更新，过时且缺乏罕见病关联。本文提出PrimeKG-Plus，通过更新20个原始数据源至2025年12月版本，整合OpenTargets等新资源，并利用LLM从637篇文献中抽取关系，经UMLS同义词映射和专家审核，扩展了图谱。新增447288条药物-蛋白-疾病路径，连接先前不可达的药物-疾病对，并捕获55个2021年6月后获批的新FDA药物。该图谱提升了药物-疾病3-6跳网络连通性，为网络药物重定位和罕见病精准医学提供了最新资源。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1697, \"height\": 1003, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1690, \"height\": 1021, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1698, \"height\": 872, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1682, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1668, \"height\": 989, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1538, \"height\": 2367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1677, \"height\": 984, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1709, \"height\": 1114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738415-v1/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1696, \"height\": 918, \"label\": \"Figure\"}]"
motivation: 现有知识图谱PrimeKG数据截止于2021年6月，缺乏后续文献和罕见病关联，限制了药物重定位应用。
method: 更新原始20个数据源并整合OpenTargets等新资源，用LLM从637篇PubMed文献提取关系，经UMLS映射和专家审核。
result: 新增447288条药物-蛋白-疾病路径，连接不可达药物-疾病对，捕获55个新FDA药物，改善网络连通性。
conclusion: PrimeKG-Plus提供持续更新的知识图谱，支持罕见病药物重定位和精准医学研究。
---

## 摘要
生物医学知识快速演化，但大多数以疾病为中心的知识图谱在发布后保持不变。我们推出PrimeKG-Plus，它是PrimeKG的扩展，将所有20个原始数据资源更新到2025年12月可用的版本，并整合了额外资源，包括OpenTargets、RepurposeDrugs和nSIDES。该图谱进一步通过使用大语言模型辅助筛选工作流从637篇PubMed摘要和PMC全文文章中提取的关系进行了扩展。提取的关系通过标准化、基于UMLS的同义词映射、基于SapBERT嵌入的相似性排序和人类专家评审进行精炼，以确保数据质量。这一文献驱动的扩展专注于罕见的神经疾病，包括Canavan病、C型尼曼-匹克病、泰-萨克斯病和巴顿病。网络拓扑分析表明，扩展后的图谱改善了通过图谱的3-6跳的间接药物-疾病连接，同时增加了447,288条药物-蛋白质-疾病路径，连接了以前无法到达的药物-疾病对。时间FDA验证在2021年6月PrimeKG数据截止后捕获了55个新的分子实体作为药物节点，其中46个在原版PrimeKG中缺失。通过将新整合和更新的资源与系统筛选的文献衍生关联相结合，PrimeKG-Plus为基于网络的药物重定位和精准医学应用提供了最新的知识图谱。数据和代码公开可用。

## Abstract
Biomedical knowledge evolves rapidly, yet most disease-centered knowledge graphs remain unchanged after publication. We present PrimeKG-Plus, an extension of PrimeKG that updates all 20 original data resources to releases available as of Dec 2025 and incorporates additional resources, including OpenTargets, RepurposeDrugs, and nSIDES. The graph is further expanded with relations extracted from 637 PubMed abstracts and PMC full-text articles using a large-language-model-assisted curation workflow. Extracted relations were refined through normalization, UMLS-based synonym mapping, SapBERT embedding based similarity ranking, and human expert review to ensure data quality. This literature-driven expansion focuses on rare neurological disorders, including Canavan disease, Niemann-Pick disease type C, Tay-Sachs disease and Batten disease. Network topology analyses indicate that the expanded graph improves indirect drug-disease connectivity of 3-6 hops through the graph while adding 447,288 Drug-Protein-Disease paths linking drug-disease pairs that were previously unreachable. Temporal FDA validation captured 55 new molecular entities after the June 2021 PrimeKG data cut-off as drug nodes, 46 absent from the original PrimeKG. By integrating newly incorporated and updated resources with systematically curated literature-derived associations, PrimeKG-Plus provides an up-to-date knowledge graph for network-based drug repurposing and precision medicine applications. Data and code are publicly available.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义（研究动机和背景）
- **背景**：现有主流生物医学知识图谱 PrimeKG 整合了 20 个数据源的超过四百万条关系，但数据截止于 2021 年 6 月。此后生物医学数据库（如 DrugBank、CTD、MONDO）经历了多次更新，大量新知识仅出现在文献中，尤其对罕见疾病，传统数据库覆盖不足。
- **核心问题**：PrimeKG 过时且缺乏针对罕见病的文献关联，限制了其在药物重定位和精准医学中的网络分析能力。
- **整体含义**：通过更新数据源、整合新资源、并利用 LLM 辅助的文献挖掘，构建一个持续更新的知识图谱 PrimeKG-Plus，以支持更准确的网络药物发现和罕见病研究。

### 2. 方法论：核心思想、关键技术细节、算法流程
- **核心思想**：在保留 PrimeKG 原有架构的基础上，从三个方向扩展：
  1. **更新原始 20 个数据源**至 2025 年 12 月版本（如 STRING v12、DrugBank 5.1.13、Bgee 2025、CTD Oct 2025 等）；
  2. **整合新资源**：OpenTargets（疾病-基因关联）、RepurposeDrugs（批准适应症）、nSIDES（药物不良反应）；
  3. **文献衍生关系提取**：关注四种罕见神经退行性疾病（Canavan、Niemann-Pick C、Tay-Sachs、Batten）。
- **关键技术细节**：
  - **LLM 辅助提取**：使用 NotebookLM（内置 Gemini 模型）对 637 篇文献进行结构化关系提取，预定义 30 种关系类型（与 PrimeKG 兼容）。
  - **实体归一化三阶段**：
    1. UMLS 映射与语义类型验证；
    2. 未映射实体通过 SapBERT 嵌入做语义恢复，再用 SBERT 重排名；
    3. 二次 UMLS 验证后过滤。
  - **专家审核**：医学生初筛 + 博士级专家复核，确保生物合理性。
  - **UMLS-MONDO 双射词典**：避免原 PrimeKG 中多对多映射导致的重复边。
  - **图谱整合**：所有节点映射到 PrimeKG 兼容 ID，新实体创建新节点。
- **算法流程**（文字说明）：
  - 文献检索 → LLM 提取三元组 → 实体归一化（UMLS + SapBERT + SBERT 重排） → 人工审核 → 图谱链接 → 去重后写入最终边列表。

### 3. 实验设计：数据集、基准、对比方法
- **数据集**：
  - 基础图谱来源于 20 个公共数据库（STRING、DrugBank、DisGeNET、MONDO、HPO、GO、Reactome、Bgee、CTD、SIDER 等）。
  - 文献部分：876 篇 PubMed 摘要/PMC 全文（四种罕见病），实际使用 637 篇。
  - 验证数据：2021.07–2025.12 期间 FDA 批准的 149 个 NME（新分子实体）。
- **基准（Benchmark）**：
  - 与原始 PrimeKG（2021 年 6 月版本）进行对比。
- **对比方法**：
  - 无其他知识图谱对比；主要对比 PrimeKG-Plus 与原始 PrimeKG 在节点数、边数、拓扑连通性（k-hop reachability）、罕见病子图富集度等方面的变化。
- **具体实验**：
  - **覆盖度比较**：节点分布、边类型分布。
  - **时间覆盖验证**：FDA 新药是否存在于图谱。
  - **网络拓扑分析**：计算非直接指示的 drug-disease 对在 2-6 跳内的可达比例。
  - **罕见病富集分析**：每种疾病锚点周边的新边和路径数量。
  - **案例研究**：Avacopan、Daridorexant 的 Drug→Protein→Disease 路径。

### 4. 资源与算力
- **文中未明确提及**使用的 GPU 型号、数量或训练时长。
- 使用了 **NotebookLM（Google）**，底层模型为 Gemini 2.5 Flash 或 Gemini 3，但平台未暴露生成参数（如 temperature），因此无法控制算力细节。
- **提示**：文献提取在 NotebookLM 环境中分批进行，未提及训练。

### 5. 实验数量与充分性
- **实验数量**：
  - 覆盖全部 20 个数据源的更新 + 3 个新资源。
  - 文献处理：637 篇文章提取 6,438 条原始三元组，经归一化后 1,290 条被接受，最终 550 条新边被融入图谱。
  - 网络拓扑分析：基于 104,738,152 个 drug-disease 对。
- **充分性评价**：
  - **优点**：对比对象明确（与原始 PrimeKG），且从多个维度（节点/边统计、拓扑连通性、时间覆盖、罕见病案例）验证，实验覆盖面较广。
  - **不足**：
    - 未做下游预测任务（如 link prediction、drug repurposing benchmark）来直接评估改进的实用性。
    - 缺乏消融实验（如单独去掉 LLM 提取或新资源的效果）。
    - 文献仅针对四种罕见病，泛化性未测试。
  - **客观性**：数据源版本和过滤条件均有详细说明，手工审核流程可复现，总体较客观。

### 6. 论文的主要结论与发现
- PrimeKG-Plus 提供了比 PrimeKG 更及时、更丰富的知识图谱：
  - 添加 **447,288 条 Drug→Protein→Disease 路径**，连接之前不可达的药物-疾病对。
  - 捕获 **55 个 2021 年 6 月后获批的 FDA 新药**（其中 46 个原版缺失）。
  - 疾病节点增 16.4%，药物节点增 17.9%，疾病-蛋白边增 221%。
  - 3-6 跳 drug-disease 可达比例提升（3 跳：33.09%→39.28%；4 跳：75.69%→85.78%）。
  - 专家验证的文献关系为四种罕见病增加了新的机制路径和候选药物。
- **结论**：PrimeKG-Plus 可作为网络药物重定位和精准医学的基础资源，且代码与数据完全公开。

### 7. 优点
- **时效性强**：系统更新至 2025 年底，且集成最新数据库。
- **罕见病聚焦**：用 LLM + 专家审核填补罕见病知识空白，实现从文献到结构化知识的有效转化。
- **实体归一化流程严谨**：UMLS + SapBERT + SBERT 的多阶段验证 + 人工审核，保证质量。
- **兼容性**：保留 PrimeKG 架构，可直接应用于现有基于 PrimeKG 的方法和基准。
- **FAIR 原则**：数据与代码公开，可复现。

### 8. 不足与局限
- **文献覆盖有限**：仅针对四种罕见病，其他疾病未涉及；且文献提取依赖 LLM 可能存在偏见（如位置偏差），虽分批缓解但未完全消除。
- **未做下游预测任务**：没有通过 link prediction 或药物重定位实验直接验证改进的实际效果，仅依赖拓扑指标。
- **节点映射冲突**：发现 865 个疾病名称在不同版本之间映射不同身份节点，可能导致引用混乱。
- **UMLS 映射精度**：部分实体即使通过 UMLS 获取 CUI，也无法映射到图谱中已有节点，最终有 664 条关系未被整合。
- **数据许可限制**：部分原始数据库（如 DrugBank、UMLS）需各自申请，不能直接重新分发。
- **算力描述缺失**：未提供 LLM 提取环节的计算资源信息，影响可复现性。

（完）
