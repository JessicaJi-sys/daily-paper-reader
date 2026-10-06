---
title: Adaptive Mixture of Disentangled Experts for Dynamic Graph Out-of-Distribution Generalization
title_zh: 面向动态图分布外泛化的自适应解耦专家混合
authors: "Haibo Chen, Xin Wang, Guanheng Chen, Yuan Meng, Haoyang Li, Yang Yao, Zeyang Zhang, Zhiqiang Zhang, JUN ZHOU, Ling Feng, Wenwu Zhu"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=q0O5LO7X4I"
tags: ["query:ddi-moe"]
score: 8.0
evidence: 自适应专家混合捕捉演化分布漂移下的不变模式
tldr: 动态图上的分布外泛化因固定架构难以应对随时间演化的分布漂移而性能受限。作者提出自适应解耦专家混合架构，通过动态专家组合在演化分布漂移下提取不变模式。实验表明该设计在分布外泛化任务上优于固定架构方法，为不变表示学习与专家动态路由结合提供了新思路。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 动态图存在随时间演化的分布漂移，固定架构难以提取稳定的不变模式。
method: 提出自适应架构设计，用解耦专家混合动态捕捉演化漂移下的不变模式。
result: 在动态图分布外泛化任务上取得优于固定架构的表现。
conclusion: 表明自适应专家混合可有效应对演化分布漂移，助力不变泛化。
---

## Abstract
Dynamic graph out-of-distribution (OOD) generalization has drawn an increasing amount of attention in the research community, given its wide applicability in real-world scenarios. Existing methods typically employ a fixed-architecture design to extract invariant patterns. However, there may exist evolving distribution shifts in dynamic graphs, leading to suboptimal performance of fixed-architecture designs. To address this issue, we propose a novel adaptive-architecture design to handle evolving distribution shifts over time, to the best of our knowledge, for the first time. The proposed adaptive-architecture design introduces an adaptive mixture of architecture experts to capture invariant patterns under evolving distribution shifts, which imposes three challenges: 1) How to detect and characterize evolving distribution shifts to inform architectural decisions; 2) How to dynamically route different expert architectures to handle varying distribution characteristics; 3) How to ensure that the adaptive mixture of experts effectively discovers invariant patterns. To solve these challenges, we propose a novel **Ada**ptive **Mix**ture of Disentangled Experts (**AdaMix**) model to adaptively route architecture experts to varying distribution shifts and jointly learn spatio-temporal invariant patterns. Specifically, we propose a spatio-temporal distribution detector to infer evolving distribution shifts by jointly leveraging historical and current information. Building upon this, we develop a prototype-guided mixture of disentangled experts that adaptively routes experts with disentangled factors to different distribution shifts. Finally, we design a distribution-aware intervention mechanism that discovers invariant patterns based on expert selection of nodes. Extensive experiments on both synthetic and real-world datasets demonstrate that our proposed **AdaMix** model significantly outperforms state-of-the-art baselines.

---

## 论文详细总结（自动生成）

## 信息边界说明
- 提供的 PDF 提取文本实际为 OpenReview 的浏览器验证/CAPTCHA 页面，并非论文正文，因此无法获取完整方法、公式、实验表格、超参数与算力细节。
- 以下总结主要依据论文标题、作者、摘要、TLDR、motivation/method/result/conclusion 等元数据；未披露内容会明确标注为“未说明/无法核验”。

## 1. 核心问题与整体含义
- **研究背景**：动态图上的分布外（OOD）泛化具有广泛现实应用价值，近年来受到越来越多关注。
- **核心问题**：现有方法通常采用**固定架构设计**来提取不变模式，但动态图中可能存在**随时间演化的分布漂移**，导致固定架构性能次优。
- **整体含义**：论文提出一种**自适应架构设计**来应对随时间演化的分布漂移，作者声称这是首次将自适应架构用于动态图 OOD 泛化。其目标是在演化漂移下捕捉稳定的**时空不变模式**，提升动态图 OOD 泛化能力。

## 2. 方法论
- **核心思想**：提出 **AdaMix（Adaptive Mixture of Disentangled Experts）**，即“自适应解耦专家混合”模型，通过动态路由不同架构专家来适配不同分布漂移，并联合学习时空不变模式。
- **三个关键挑战**：
  - 如何检测并刻画演化分布漂移，以指导架构决策；
  - 如何动态路由不同专家架构，以处理变化的分布特征；
  - 如何确保专家混合真正发现不变模式，而非仅拟合环境差异。
- **关键技术细节**：
  - **时空分布检测器**：联合利用历史信息和当前信息，推断演化中的分布漂移。
  - **原型引导的解耦专家混合**：以原型引导方式，将具有解耦因子的专家自适应路由到不同分布漂移。
  - **分布感知干预机制**：基于节点层面的专家选择来发现不变模式。
- **算法流程（文字概括）**：
  - 输入动态图的历史与当前信息；
  - 时空分布检测器估计当前分布漂移；
  - 根据漂移特征，通过原型引导机制选择/组合解耦专家；
  - 通过分布感知干预，约束或筛选与不变模式相关的专家选择；
  - 最终联合学习时空不变表示，用于 OOD 泛化。
- **说明**：摘要未给出显式公式、损失函数、路由算法伪代码或复杂度分析，因此无法进一步还原数学细节。

## 3. 实验设计
- **数据集/场景**：摘要称在**合成数据集和真实世界数据集**上进行了大量实验，但未列出具体数据集名称、规模、动态图类型或 OOD 划分方式。
- **Benchmark**：未明确说明使用了哪个公开 benchmark、评价指标或 OOD 设定。
- **对比方法**：摘要仅称与**state-of-the-art baselines**比较，未列出具体基线方法名称。
- **可确认的实验结论**：AdaMix 在合成和真实数据上显著优于现有最优基线。
- **未披露内容**：数据集细节、baseline 列表、评价指标、训练/验证/测试划分、OOD 类型、统计显著性检验等均无法从当前文本中核验。

## 4. 资源与算力
- 当前提供的摘要与元数据中**未提及任何算力信息**，包括 GPU 型号、GPU 数量、训练时长、参数量、显存占用或计算开销。
- 因此无法总结其资源消耗，也无法判断该方法在真实大规模动态图上的计算可行性。

## 5. 实验数量与充分性
- 摘要声称进行了 **extensive experiments on both synthetic and real-world datasets**，说明实验至少覆盖合成与真实场景两类数据。
- 但未说明具体实验组数、数据集数量、消融实验数量、专家数量敏感性、路由机制分析、干预机制分析等。
- 元数据中显示该论文为 **ICLR-2026-Accepted**，score 为 **8.0**，可作为同行评审认可度的间接信号。
- 然而，仅凭摘要无法判断实验是否充分、客观、公平；例如是否与固定架构方法在同等参数量/计算量下比较，是否进行了多次随机种子实验，是否报告方差等均未知。

## 6. 主要结论与发现
- 固定架构在动态图演化分布漂移下存在性能瓶颈，难以稳定提取不变模式。
- 自适应专家混合架构能够根据分布漂移动态组合专家，从而更有效地捕捉不变模式。
- AdaMix 在合成与真实动态图 OOD 任务上显著优于现有 SOTA 基线。
- 该工作表明：将**不变表示学习**与**专家动态路由**结合，是应对动态图 OOD 泛化的一种有效新思路。

## 7. 优点
- **问题切入新颖**：针对动态图 OOD 中“演化分布漂移”问题，提出自适应架构而非固定架构，作者声称首次探索该方向。
- **方法设计系统**：同时覆盖漂移检测、专家路由和不变模式发现三个关键环节，形成较完整的技术闭环。
- **机制具有针对性**：
  - 时空分布检测器联合历史与当前信息；
  - 原型引导的解耦专家混合增强路由可解释性与适应性；
  - 分布感知干预机制从节点专家选择角度促进不变性。
- **实验覆盖类型较广**：至少包含合成与真实世界动态图，且摘要报告显著优于 SOTA。
- **发表信号积极**：ICLR-2026 接收、评分 8.0，说明方法创新性和实验质量获得一定程度认可。

## 8. 不足与局限
- **全文不可得导致核验受限**：当前 PDF 为验证页，无法检查公式、算法、实验表格和附录，因此许多结论只能依赖摘要。
- **实验细节缺失**：未披露数据集名称、benchmark、baseline、评价指标、OOD 设置、超参数和统计检验，难以判断公平性与可复现性。
- **算力与效率未说明**：专家混合和动态路由通常带来额外计算与存储开销，论文是否报告效率、可扩展性和推理成本未知。
- **潜在偏差风险**：分布漂移检测依赖历史与当前信息，可能对突变漂移、噪声边、稀疏节点或非平稳性强的真实图敏感。
- **应用限制**：若真实场景中漂移类型复杂、专家数量难以选择，或需要在线更新，AdaMix 的部署成本与稳定性仍需验证。
- **比较公平性未知**：自适应架构通常参数量更大，若未控制模型容量或计算预算，与固定架构基线的比较可能存在优势来源不明确的问题。

（完）
