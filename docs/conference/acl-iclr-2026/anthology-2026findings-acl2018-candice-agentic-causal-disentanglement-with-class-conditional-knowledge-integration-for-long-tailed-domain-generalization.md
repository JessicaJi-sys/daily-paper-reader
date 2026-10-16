---
title: "CANDICE: Agentic Causal Disentanglement with Class Conditional Knowledge Integration for Long Tailed Domain Generalization"
title_zh: CANDICE：面向长尾域泛化的类条件知识融合代理式因果解耦
authors: "Midhat Urooj, Ayan Banerjee, Sandeep Gupta"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://aclanthology.org/2026.findings-acl.2018.pdf"
tags: ["query:ood-inv"]
score: 7.0
evidence: 面向域泛化的域不变特征因果解耦
tldr: 该文针对临床场景中域泛化与长尾识别并存的问题，指出强制域不变性会压制长尾所需的类判别信号。作者提出CANDICE框架，通过代理式因果解耦并融入临床专家知识作为因果干预，将不变特征与类相关信号分离整合。方法在保持域泛化的同时缓解长尾识别退化，为因果解耦与不变学习结合提供范例。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2820, \"height\": 1504}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 2912, \"height\": 1464}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 725, \"height\": 1040}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-005.webp\", \"caption\": \"\", \"page\": 16, \"index\": 5, \"width\": 1181, \"height\": 808}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-006.webp\", \"caption\": \"\", \"page\": 16, \"index\": 6, \"width\": 1629, \"height\": 710}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl2018/fig-007.webp\", \"caption\": \"\", \"page\": 16, \"index\": 7, \"width\": 1103, \"height\": 220}]"
motivation: 临床部署同时面临域泛化与长尾识别，强制域不变性会压制类判别信号。
method: 提出CANDICE框架，用代理式因果解耦并融合临床专家知识作为因果干预。
result: 方法在保持域泛化的同时缓解长尾识别性能退化。
conclusion: 因果解耦与知识融合可平衡不变性与类判别性。
---

## Abstract
Deep learning models deployed in clinical settings face two major challenges: domain generalization (DG) and long-tailed (LT) recognition. DG requires learning domain-invariant features to ensure robustness across heterogeneous acquisition protocols and patient populations. However, we identify a fundamental trade-off: objectives that enforce domain invariance often suppress class-discriminative signals essential for long-tailed recognition.To address this, we propose the Agentic Causal Disentanglement (CANDICE) Framework , a modular architecture that integrates explicit clinical expertise from sonographers, radiologists, and specialists as a form of causal intervention. The framework combines clinical reasoning, causal representation learning, and automated pipeline construction to disentangle domain-invariant and class-discriminative features. By incorporating domain-specific causal knowledge, it effectively decouples the objectives of DG and LT learning. We evaluate CANDICE on 10 diverse medical imaging datasets spanning four modalities. The framework achieves an average performance improvement of 10.3% across both multi-domain and in-domain long-tailed tasks, demonstrating its effectiveness in handling distribution shifts while preserving minority class performance.

---

## 论文详细总结（自动生成）

# CANDICE 论文中文总结

## 1. 核心问题与整体含义
- **研究背景**：临床部署的深度学习模型同时面临两类挑战：**域泛化（DG）**要求学习跨机构、跨设备、跨人群稳定的域不变特征；**长尾识别（LT）**要求对稀疏但关键的罕见病理类别保持判别力。
- **核心矛盾**：论文指出二者存在“鲁棒性—尾部权衡”。过度追求域不变性会压制类判别信号，导致罕见类流形坍缩；而过度拟合长尾细粒度结构又会捕获非因果、域相关的伪影，无法泛化。
- **问题本质**：真实医学数据同时存在 \(P(Y)\) 与 \(P(X|Y)\) 偏移，单纯数据驱动方法难以解耦类身份与不稳定伪相关。
- **整体含义**：作者将稳健医学诊断重新表述为**代理式流水线构建问题**，而非单一预测器训练问题。CANDICE 通过 LLM 代理、因果表示学习与自动化代码生成，将领域知识作为因果干预，试图解耦 DG 与 LT 目标。

## 2. 方法论
### 2.1 核心思想
- 引入**域不变知识空间 \(K\)**，假设 \(P(K|Y)\) 编码全局有效的因果语义。
- 将推理分解为：
  \[
  P(Y|X,D)=\sum_z P(Y|X,z)P(z|X,K,D)
  \]
  其中 \(z\) 为 CDA 选择的潜在决策路径，\(X\) 为输入，\(Y\) 为标签，\(D\) 为域，\(K\) 为外部知识。
- 通过知识空间锚定表示，分离类特定因果因素与域相关伪影，同时学习：
  - 视觉因果特征空间：用于域泛化；
  - 知识特征空间：用于类特定保真，尤其是罕见类。

### 2.2 三代理架构
- **CRA：Clinical/Conceptual Reasoning Agent**
  - 从可信医学语料检索证据，分解为原子事实。
  - 构建类条件因果链，连接可观测输入、中间概念与类别结果。
  - 对每个推理步骤进行忠实性验证，输出因果主张、证据链接、不确定性标记。
  - 不输出最终预测，只提供软因果约束。
- **CDA：Causal Disentanglement Agent**
  - 作为约束规划器，评估输入可用性、可提取性、工具/模型选择。
  - 在因果相关性、类不确定性与域敏感性之间权衡，选择类条件决策路径 \(z\)。
  - 目标是同时保持鲁棒性与尾部类保真度，避免统一推理带来的误差传播。
- **CGA：Code Generation Agent**
  - 将 CRA 规格与 CDA 计划转化为可执行 Python 流水线。
  - 通过执行验证、失败诊断与自调试迭代修正代码。
  - 使抽象推理与可观测计算对齐，防止符号推理“看似合理但静默失败”。

### 2.3 CoCKTAIL 集成学习器
- 全称：**Conditional Cascaded Knowledge-and-Tail-Aware Integration Learner**。
- 在决策级融合知识驱动分类器 \(h_K(x)\) 与深度模型 \(h_D(x)\)。
- 算法流程：
  - 维护当前工作集 \(A\)。
  - 对候选假设计算 **Entropy Imbalance Gain（EIG）**，选择增益最大的假设进行划分。
  - 若罕见类 \(c_r\) 出现在划分中，用 **Gini 纯度**判断是否继续级联；不纯则继续，纯则终止。
  - 若罕见类未出现在划分中，则限制到保留罕见类的子分支。
  - EIG 接近时用置信度打破平局，并要求超过可信阈值 \(\delta^\dagger\)。
- 效果：头部类更多走数据驱动假设，尾部类更多走知识驱动假设，从而在决策层面解耦“平滑/鲁棒”与“锐利/尾部”目标。

## 3. 实验设计
- **数据集与场景**：论文称在 10 个医学数据集、4 类模态上评估，覆盖四个应用：
  - **Seizure Onset Zone（SOZ）定位**：rs-fMRI，独立成分分析，极端稀有类约每受试者 5 个 SOZ ICs；跨中心 PCH 训练、UNC 测试。
  - **Diabetic Retinopathy（DR）分级**：APTOS、EyePACS、MESSIDOR、MESSIDOR2；5 类 DR 分级与 SDG/MDG。
  - **Cardiac Function Assessment**：EchoNet-Dynamic 超声心动图视频，估计 LVEF 与心衰分类。
  - **Coronary Artery Disease（CAD）检测**：Mayo Integrated Stress Center 运动负荷 ECG，726 训练、227 测试。
- **Benchmark 与对比方法**：
  - 总体对比：Vision-only、RAG+Vision、ReAct 风格代理、LangGraph 固定流水线。
  - DG 对比：Fishr、SPSD-ViT、SD-ViT、ViT 等。
  - Agent 层面对比：LLM 无检索、RAG 无
