---
title: "EBD-DTI: Episodic Bridge Diffusion for Zero-Shot Cold-Start Drug-Target Interaction Prediction"
title_zh: EBD-DTI：面向零样本冷启动药物-靶标相互作用预测的片段桥接扩散
authors: "Liu, J., Le, J., Wei, C., Liu, M., Yin, Z."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738384v1.full.pdf"
tags: ["query:cold-ddi"]
score: 9.0
evidence: 零样本冷启动药物-靶点相互作用预测，使用情景训练；直接适用于冷启动DDI
tldr: "药物-靶点冷启动预测是计算药物发现的难题，现有图模型依赖全局扩散或需要少量已知交互。EBD-DTI通过情景式冷启动训练（每个epoch掩蔽部分实体作为伪冷启动）结合桥接条件局部子图与多跳扩散，为零样本图推理提供关系上下文。在BioSNAP、BindingDB、DrugBank基准上严格零样本评估中，AUC提升高达12%，达到或超越现有方法。该框架无需任何未知实体的已知交互，实现了图模型在零样本场景下的有效泛化。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1769, \"height\": 781, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1759, \"height\": 581, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 874, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1797, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1793, \"height\": 524, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 500, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 588, \"height\": 806, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1428, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738384-v1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 833, \"height\": 469, \"label\": \"Table\"}]"
motivation: 现有图模型在完全未见药物或蛋白质的冷启动场景下表现不足，需要不依赖已知交互的零样本推理方法。
method: 采用情景式训练，随机掩蔽训练实体作为伪冷启动，通过桥接条件局部子图与多跳扩散为冷实体提供最近观察邻居的关系上下文。
result: "在三个标准零样本评估中，AUC相比基线提升最高12%，性能匹敌甚至超过需少量交互的少样本方法。"
conclusion: EBD-DTI为图模型提供了有效的零样本冷启动DTI预测方案，无需任何已知交互，具有实际应用价值。
---

## 摘要
预测完全未见过的药物或蛋白质的相互作用——即冷启动问题——仍然是计算药物发现中的关键挑战。尽管基于序列的方法天然支持零样本泛化，但它们通常忽略关系拓扑，而现有的基于图的方法要么依赖全局扩散（模糊了归纳与转导评估的边界），要么在测试时需要少量已知相互作用样本（少样本）。我们提出EBD-DTI，一个在基于图的DTI模型中实现零样本推理的框架，无需未见实体任何已知相互作用。关键创新在于片段式冷启动训练：每个epoch，随机遮蔽部分训练实体并视为伪冷启动，迫使模型通过显式梯度监督学习冷启动推理。一个桥接条件的局部子图，结合多跳扩散，为冷实体提供来自其最近观测邻居的关系上下文。在三个基准（BioSNAP、BindingDB和DrugBank）上的实验表明，在严格的零样本评估下，EBD-DTI与最先进方法相比达到具有竞争力或更优的性能，片段式训练使AUC提升高达12%。

## Abstract
Predicting drug-target interactions (DTI) for entirely unseen drugs or proteins---the cold-start problem---remains a critical challenge in computational drug discovery. While sequence-based methods naturally support zero-shot generalization, they often ignore relational topology, and existing graph-based approaches either rely on global diffusion that blurs the boundary between inductive and transductive evaluation or require a few known interaction samples at test time (few-shot). We present EBD-DTI, a framework that enables zero-shot inference in graph-based DTI models without requiring any known interactions for unseen entities. The key innovation is episodic cold-start training: at each epoch, a random subset of training entities is masked and treated as pseudo-cold, forcing the model to learn cold-start inference with explicit gradient supervision. A bridge-conditioned local subgraph, together with multi-hop diffusion, provides cold entities with relational context from their nearest observed neighbors. Experiments on three benchmarks (BioSNAP, BindingDB, and DrugBank) demonstrate that EBD-DTI achieves competitive or superior performance compared to state-of-the-art methods under strict zero-shot evaluation, with episodic training improving AUC by up to 12%.

---

## 论文详细总结（自动生成）

# 论文详细中文总结：EBD-DTI

## 1. 核心问题与整体含义

- **研究动机**：在计算药物发现中，预测全新药物或蛋白质（冷启动实体）与已知实体之间的相互作用是关键瓶颈。现有图神经网络（GNN）方法在转导设置下表现良好，但无法处理图中完全无边的冷实体；基于序列的方法虽支持零样本，但忽略关系拓扑；少样本元学习则依赖测试时的少量已知交互，不符合真实场景。
- **整体含义**：提出一个**图模型下的零样本冷启动DTI预测框架**，使得模型能在未见实体无任何已知交互的情况下，利用其与训练实体的特征相似性构建局部子图并进行推理，从而弥合训练-测试分布不匹配。

## 2. 方法论

### 核心思想
- **片段式冷启动训练**：每个epoch随机遮蔽20%的训练实体作为伪冷启动，强制桥接模块在监督信号下学习如何为冷实体检索邻居并传播信息。
- **桥接条件局部子图**：对每个冷实体，基于特征余弦相似度选出top-k个最近可见训练实体，加上这些邻居的已知交互伙伴，构建小规模二分图。
- **局部多跳扩散**：在局部子图上执行T=3步扩散，融合桥接权重，最后通过残差连接生成冷实体表示。

### 关键技术细节
1. **节点特征**：
   - 药物：1024位Morgan指纹 + 10个RDKit描述符 → 1034维 → 两层MLP投影至128维。
   - 蛋白：ESM-2（650M参数）均值池化得1280维 → 两层MLP投影至128维。
2. **桥接构建**（公式3.2）：`N_k(d_c) = top-k_{d_s∈D_train} cos(z_{d_c}, z_{d_s})`，权重softmax归一化。
3. **局部扩散**（公式3.3～3.4）：`Z^{(t)} = A_local Z^{(t-1)}`，`Z^* = Σα_t Z^{(t)} + βZ^{(0)}`，其中`A_local`是行归一化的局部邻接矩阵（无自环），`α_t`可学习，`β=0.5`。
4. **链路预测**（公式3.8）：`ŷ = σ(MLP([z_d^* ∥ z_p^* ∥ z_d^*⊙z_p^* ∥ |z_d^* - z_p^*| ∥ c_ij]))`。
5. **损失**（公式3.7）：二元交叉熵，Adam优化器（lr=1e-3），早停（patience=10，max 60 epochs）。

## 3. 实验设计

- **数据集**：BioSNAP（13,830正对，密度0.14%）、BindingDB（20,674正对，0.05%）、DrugBank（17,511正对，0.06%）。
- **冷启动协议**：严格零样本——从训练图中完全移除测试实体的所有边，20%实体作为冷测试集。
- **对比方法**：
  - 序列模型：MolTrans、HyperAttentionDTI、DrugBAN、MlanDTI、ColdstartCPI（使用原始特征重跑）。
  - 图模型：GCN、GraphSAGE、GAT、APPNP（使用与EBD-DTI相同的特征，去除测试实体边，无KNN增强）。
- **评估指标**：AUC、AUPR、F1（均值±标准差，3个随机种子520,521,522）。

## 4. 资源与算力

文中**未明确说明**使用的GPU型号、数量以及具体训练时长。仅给出超参数：embedding维度128，batch size 256，学习率1e-3，最大60 epochs。从早停设置和数据集规模推断，单次训练可在单卡上数小时内完成。

## 5. 实验数量与充分性

- **主要实验**：2个设置（冷-drug、冷-target）×3个数据集×3个种子，报告均值±标准差，与10种基线对比（表2、表3）。
- **消融实验**（图2、表4）：5种配置（全模型、w/o QE、w/o episodic、w/o bridge+diffusion、纯特征），在3个数据集上验证。
- **敏感度分析**（表5～表7）：
  - mask比例ρ（0.05～0.40，表5）。
  - top-k（3～30）、扩散步T（1～7）、残差权重β（0～1）（表6）。
  - 4种片段策略（单-drug、单-target、同时、交替，表7）。
- **充分性与公平性**：实验覆盖多种场景，消融验证了关键贡献成分，基线在相同特征和冷启动划分下重跑，参数鲁棒性分析全面。但需注意Human数据集因方差大而被排除，未纳入主要评估。

## 6. 主要结论与发现

1. **片断式冷启动训练是性能首要驱动**：去除后，BindingDB冷-target AUC从0.850降至0.735（−13.5%）；BioSNAP冷-target AUC从0.901降至0.843（−6.4%）。
2. **冷-target比冷-drug更难**：因为蛋白特征（ESM-2均值池化）不如药物Morgan指纹对结合位点具有判别性；模型在冷-target上显著低于冷-drug。
3. **桥接模块在片断训练后能学习到结构相关邻居**：被选中的邻居与冷实体的特征相似度显著高于随机；参数top-k在3～30内AUC变化<0.005，表明扩散有效聚合多邻居信息。
4. **局部子图+局部扩散**满足DTI图直径2～3跳的特性，T=3足够，增加步骤收益微小。
5. **Query Edges**可为冷-target带来额外1.4～3.4% AUC提升，且不泄露测试信息（仅使用训练交互）。

## 7. 优点

- **创新性**：首次将**训练-测试分布对齐**引入冷启动DTI，通过片断模拟直接为桥接模块提供梯度监督，解决了“桥接从未被训练”的根本问题。
- **架构简洁有效**：无需复杂组件（如对比学习、课程学习），简单的局部扩散+残差连接在充分训练下即达到最好效果。
- **严格的零样本协议**：测试时不使用任何KNN增强或预计算结构，避免了转导泄露，更贴近真实应用。
- **参数鲁棒**：mask比例、top-k、扩散步长等在宽范围内性能稳定，易于部署。
- **实验公正**：重跑所有基线，使用相同特征和冷启动划分，比较基线包含序列和图两类主流方法。

## 8. 不足与局限

- **Human数据集排除**：因样本量小、方差大（AUC跨度±0.05）被移出主实验，限制了在人类蛋白上的验证。
- **蛋白特征缺陷**：ESM-2全序列均值池化丢掉局部结合口袋信息，导致冷-target与冷-drug的performance差距。作者建议未来使用AlphaFold2结构特征。
- **仅覆盖单实体冷启动**：未处理“完全盲冷启动”（药物和蛋白同时未见），这是更困难但实际常见的场景。
- **算力资源未公开**：未给出具体GPU型号和训练时间，影响可复现性的精确评估。
- **偏差风险**：负采样采用1:1平衡策略，可能高估模型在真实不平衡分布下的表现；数据集均为公开基准，可能存在数据选择偏差。

（完）
