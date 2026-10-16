---
title: Learning Invariant Modality Representation for Robust Multimodal Learning from a Causal Inference Perspective
title_zh: 从因果推断视角学习鲁棒多模态学习的不变模态表示
authors: "Sijie Mai, Shiqin Han"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://aclanthology.org/2026.acl-long.2119.pdf"
tags: ["query:ood-inv"]
score: 8.0
evidence: 因果解耦将因果不变表示与环境相关虚假表示分离
tldr: 该文关注多模态情感计算中模型学习虚假相关而损害分布偏移下泛化的问题。作者提出因果模态不变表示学习框架CmIR，基于因果推断将每种模态解耦为因果不变表示与环境相关虚假表示。框架确保不变表示保持稳定的预测关系，从而在分布偏移或模态噪声下更鲁棒，为解耦不变与虚假特征提供了理论支撑的方法。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1889, \"height\": 736}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 1662, \"height\": 622}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-003.webp\", \"caption\": \"\", \"page\": 5, \"index\": 3, \"width\": 2673, \"height\": 963}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 2234, \"height\": 1517}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 2234, \"height\": 1515}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-006.webp\", \"caption\": \"\", \"page\": 9, \"index\": 6, \"width\": 2645, \"height\": 2070}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-007.webp\", \"caption\": \"\", \"page\": 9, \"index\": 7, \"width\": 2645, \"height\": 2070}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-008.webp\", \"caption\": \"\", \"page\": 9, \"index\": 8, \"width\": 2092, \"height\": 1334}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-009.webp\", \"caption\": \"\", \"page\": 9, \"index\": 9, \"width\": 2090, \"height\": 1334}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-010.webp\", \"caption\": \"\", \"page\": 9, \"index\": 10, \"width\": 2096, \"height\": 1344}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-011.webp\", \"caption\": \"\", \"page\": 9, \"index\": 11, \"width\": 2088, \"height\": 1332}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2119/fig-012.webp\", \"caption\": \"\", \"page\": 19, \"index\": 12, \"width\": 2418, \"height\": 1826}]"
motivation: 多模态模型常学到虚假相关，在分布偏移或模态噪声下泛化变差。
method: 提出CmIR框架，基于因果推断将各模态解耦为因果不变表示与环境相关虚假表示。
result: 不变表示保持稳定预测关系，提升分布偏移与噪声下的鲁棒性。
conclusion: 因果解耦可有效分离不变特征与虚假特征。
---

## Abstract
Multimodal affective computing aims to predict humans’ sentiment, emotion, intention, and opinion using language, acoustic, and visual modalities. However, current models often learn spurious correlations that harm generalization under distribution shifts or noisy modalities. To address this, we propose a causal modality-invariant representation (CmIR) learning framework for robust multimodal learning. At its core, we introduce a theoretically grounded disentanglement method that separates each modality into ‘causal invariant representation’ and ‘environment-specific spurious representation’ from a causal inference perspective. CmIR ensures that the learned invariant representations retain stable predictive relationships with labels across different environments while preserving sufficient information from the raw inputs via invariance constraint, mutual information constraint, and reconstruction constraint. Experiments across multiple multimodal benchmarks demonstrate that CmIR achieves state-of-the-art performance. CmIR particularly excels on out-of-distribution data and noisy data, confirming its robustness and generalizability.

---

## 论文详细总结（自动生成）

### 1. 核心问题与整体含义
- **研究动机**：多模态情感计算（MAC）利用语言、声学、视觉信号预测情感、意图、观点等，但现有模型常从训练数据中学到**虚假跨模态相关**，而非真实因果机制。
- **核心问题**：当测试分布与训练分布不同，或模态存在噪声时，模型泛化显著下降；现有域适应、解耦学习缺乏因果解释，部分因果方法又依赖特定偏差类型或先验假设。
- **整体含义**：论文提出 **CmIR（Causal modality-Invariant Representation）**，从因果推断视角将每种模态解耦为“因果不变表示”和“环境特定虚假表示”，仅用不变表示预测，以提升分布偏移和模态噪声下的鲁棒性。

### 2. 方法论
- **核心思想**：基于结构因果模型（SCM），假设存在环境变量 \(E\) 导致分布偏移；每种模态 \(X_m\) 可分解为：
  - \(Z^{inv}_m\)：与标签 \(Y\) 保持稳定因果关系的因果不变表示；
  - \(Z^{spu}_m\)：环境相关、非因果的虚假表示。
  - 假设 \(Y\) 仅由 \(\{Z^{inv}_m\}\) 因果影响，且独立于 \(E\) 与 \(\{Z^{spu}_m\}\)。
- **理论支撑**：
  - **定理 1**：定义因果不变模态表示，即跨环境条件分布 \(P(Y|\phi_m(X_m),E)\) 不变。
  - **定理 2**：证明在预测损失、不变约束、互信息约束、重构约束下，可提取出满足环境独立性和因果充分性的解耦表示。
  - **定理 3**：证明基于不变表示的预测器在最坏情况 OOD 风险上优于原始特征预测器。
- **实现流程**：
  - 每个模态经编码器 \(g_m\) 得到 \((Z^{inv}_m,Z^{spu}_m)\)，解码器 \(r_m\) 负责重构原始输入。
  - **预测损失** \(L_{pred}\)：用预测头 \(h\) 融合各模态 \(Z^{inv}_m\) 预测标签。
  - **不变约束**：通过虚拟环境模拟，给原始特征加入环境相关噪声 \(\tilde X^{(e)}_m=X_m+\alpha(e)\epsilon_m\)，其中 \(\alpha(e)=\alpha(1)\cdot e\)；编码后最小化不同环境下 \(Z^{inv}_m\) 的 L1 距离。
  - **互信息约束**：用正交性作为互信息最小化代理，对归一化后的 \(Z^{inv}_m\) 与 \(Z^{spu}_m\) 计算相关矩阵 \(C_m\)，最小化 \(\|\text{diag}(C_m)+\alpha(C_m-\text{diag}(C_m))\|_F\)。
  - **重构约束**：最小化 \(X_m\) 与 \(\hat X_m=r_m(Z^{inv}_m,Z^{spu}_m)\) 的 MSE。
  - **总目标**：\(L=L_{pred}+\sum_m(\lambda_1 R^{inv}_m+\lambda_2 R^{dec}_m+\lambda_3 R^{rec}_m)\)。

### 3. 实验设计
- **任务与数据集**：
  - 多模态情感分析（MSA）：CMU-MOSI、CMU-MOSEI、CH-SIMS-v2；
  - 分布外场景：CMU-MOSI (OOD)；
  - 多模态幽默检测（MHD）：UR-FUNNY；
  - 多模态讽刺检测（MSD）：MUStARD。
- **评价指标**：
  - CMU-MOSI/MOSEI：Acc7、Acc2、F1、MAE、Corr；
  - CH-SIMS-v2：Acc5、Acc3、Acc2、F1、MAE、Corr；
  - MHD/MSD：二分类准确率。
- **对比方法**：
  - MSA：Self-MM、ConFEDE、FDMER、SuCI、C-MIB、EMOE、Multimodal Boosting、ITHP、Diffusion Bridge、GSCon 等；
  - CH-SIMS-v2：MISA、MAG-BERT、Self-MM、MMIM、AV-MC、KuDA、DLF、Diffusion Bridge 等；
  - OOD：CLUE、GEAR、MulDeF、Self-MM、ITHP、KAN-MCP；
  - 噪声鲁棒：TMDC、C-MIB、Multimodal Boosting；
  - MHD/MSD：MulT、Self-MM、MMIM、HKT、DMD、DMD+SuCI、AtCAF、MAG-XLNet、MCL、MGCL、ITHP、MISA、MIL 等。
- **额外实验**：消融实验、超参鲁棒性、高斯噪声与 OOD 噪声、t-SNE 可视化、显著性 t-test、模型复杂度、探测实验、不同不变约束对比、噪声强度敏感性分析。

### 4. 资源与算力
- 文中明确提到：使用 **PyTorch 1.13.1**，在 **NVIDIA RTX3090 GPU**（CUDA 11.6）上训练，优化器为 AdamW。
- 超参通过 **50 次随机网格搜索**确定，并用最佳配置重训 **5 次**取平均。
- **未明确说明**：GPU 数量、总训练时长、总 GPU 时、显存占用、碳排放等。因此算力报告不完整。

### 5. 实验数量与充分性
- 实验覆盖 **6 个数据集、3 类任务**，包含标准、OOD、噪声场景。
- 做了多组消融：Vanilla、去掉不变约束、去掉互信息约束、去掉重构约束。
- 做了超参分析：\(\lambda_1,\lambda_2,\lambda_3,K,\alpha(1)\)。
- 做了噪声率 0.1–0.7 的鲁棒性测试，以及 Laplace 噪声和随机擦除的 OOD 噪声测试。
- 还包含 t-SNE、探测实验、复杂度分析、显著性检验、不同不变约束对比。
- **充分性**
