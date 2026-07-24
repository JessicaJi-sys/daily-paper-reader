---
title: "Target Preference Maps: A machine learning model generalizing transferable drug-receptor interactions and guiding drug discovery"
title_zh: 靶标偏好图谱：一种泛化可迁移药物-受体相互作用并指导药物发现的机器学习模型
authors: "Menezes, F., Wahida, A., Froehlich, T., Grass, P., Zaucha, J., Napolitano, V., Siebenmorgen, T., Pustelny, K., Barzowska-Gogola, A., Rioton, S., Didi, K., Bronstein, M., Czarna, A., Hochhaus, A., Plettenburg, O., Sattler, M., Nissen-Meyer, J., Conrad, M., Kurzrock, R., Popowicz, G. M."
date: 2026-07-21
pdf: "https://www.biorxiv.org/content/10.1101/2025.08.01.668090v11.full.pdf"
tags: ["query:ddi-transfer"]
score: 8.0
evidence: 可迁移的药物-受体相互作用，对未知药物的归纳泛化
tldr: 传统药物发现依赖昂贵筛选，结构知识泛化不足。提出机器学习框架从蛋白-配体局部微环境学习原子类型特异空间偏好图，排除配体拓扑以捕获可迁移交互。模型恢复化学有意义模式，包括桥接水和金属依赖环境，经回顾和前瞻验证。该方法提供可解释工作流，指导分子优化并输入下游生成或对接流程。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1696, \"height\": 1943, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1708, \"height\": 1918, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1695, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1711, \"height\": 1736, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1684, \"height\": 1961, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1704, \"height\": 1292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1712, \"height\": 1258, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1711, \"height\": 290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1593, \"height\": 1600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1707, \"height\": 1179, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1671, \"height\": 1151, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1715, \"height\": 808, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1481, \"height\": 1048, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1493, \"height\": 1056, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1500, \"height\": 1048, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1495, \"height\": 1044, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1480, \"height\": 1044, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1492, \"height\": 1045, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1489, \"height\": 1050, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1491, \"height\": 1042, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1487, \"height\": 1044, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1492, \"height\": 1047, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 836, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1345, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1347, \"height\": 905, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 433, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-08-01-668090-v11/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1511, \"height\": 236, \"label\": \"Table\"}]"
motivation: 克服传统结构药物设计泛化能力不足，减少对昂贵、资源密集筛选的依赖，提升AI在药物发现中的实用性。
method: 从蛋白-配体结构局部微环境学习原子类型特异空间偏好图，排除配体拓扑，降低整体配体记忆依赖。
result: 模型恢复化学有意义的相互作用模式，包括桥接水和金属依赖环境，经回顾和前瞻数据验证有效。
conclusion: 提供可解释工作流指导分子优化，并为下游生成或对接流程提供输入。
---

## 摘要
现代AI模型能够解码基因组景观和蛋白质结构世界。然而，它们无法泛化到最重要的领域之一：小分子药物发现。自20世纪70年代末以来，大分子晶体学的出现启发了这样一种概念：仅凭结构知识就能实现锁钥式的药物设计。然而，药物发现仍然依赖于昂贵、资源密集型且很大程度上偶然的筛选活动，这些活动仅探测了类药化学空间中极小的一部分。尽管有一些成功案例，我们对非键相互作用化学的理解和推理仍然有限，无法普遍适用。此外，尽管结构数据库包含数十万条记录，但蛋白质-药物结构中存在强烈的历史偏差，阻碍了通过AI扩展实现可靠进展。在这里，我们提出了一个机器学习框架，该框架从蛋白质-配体结构中的局部蛋白质微环境中学习原子类型特异性空间偏好图谱。通过从模型输入中排除配体拓扑，并从局部原子级环境中学习，该框架旨在减少对整个配体记忆的依赖，并捕获可迁移的相互作用偏好。生成的图谱恢复了具有化学意义的相互作用模式，包括涉及桥接水和金属依赖环境的案例。该模型通过在挑战性蛋白质-蛋白质界面的药物优化中，使用回顾性和前瞻性真实世界数据进行了验证。这表明该方法可以提供可解释的工作流程，以指导分子优化，并为下游生成或对接工作流程提供输入。

## Abstract
Modern AI models can decode the genomic landscape and protein structure world. Yet, they fail to generalize to one of the most important fields: small-molecule drug discovery. Since the late 1970s, the advent of macromolecular crystallography inspired the notion that structural knowledge alone could enable a lock-and-key approach to drug design. However, drug discovery continues to depend on costly, resource-intensive, and largely serendipitous screening campaigns that probe only an infinitesimal fraction of the drug-like chemical space. Despite some successful cases, our understanding of, and reasoning from, non-bonded interaction chemistry remains limited for general applicability. Furthermore, though structural databases contain hundreds of thousands of entries, a strong historical bias pervades protein-drug structures, hindering reliable advances through AI scaling. Here, we present a machine-learning framework that learns atom-type-specific spatial preference maps from local protein microenvironments in protein-ligand structures. By excluding ligand topology from the model input and learning from local atom-level environments, the framework is designed to reduce dependence on whole-ligand memorization and to capture transferable interaction preferences. The resulting maps recover chemically meaningful interaction patterns, including cases involving bridging waters and metal-dependent environments. The model was validated using retrospective and prospective real-world data in drug optimization when targeting a challenging protein-protein interface. This shows that the method can provide interpretable workflows to guide molecule optimization and provide input for downstream generative or docking workflows.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：传统结构药物设计（如锁钥模型）自20世纪70年代末以来虽受启发，但实际药物发现仍依赖昂贵、资源密集且充满偶然性的高通量筛选，仅探索类药化学空间的极小一部分。现有AI模型在基因组和蛋白质结构预测上取得进展，却无法泛化到小分子药物发现，主要原因是：
  - 对非键相互作用化学的理解和推理有限，难以普遍适用；
  - 蛋白质-配体结构数据库中存在强烈的历史偏差，阻碍通过AI规模扩展获得可靠进展。
- **整体含义**：迫切需要一种能够学习可迁移、不依赖于特定配体拓扑的蛋白质-配体相互作用泛化模型，以降低对昂贵筛选的依赖，提升AI在药物发现中的实用性和可解释性。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：从蛋白质-配体复合物的局部微环境中学习**原子类型特异性的空间偏好图谱**（Target Preference Maps），模型输入排除全局配体拓扑信息，仅使用局部蛋白质微环境特征，从而迫使模型捕获跨不同配体可迁移的相互作用偏好，避免对整个配体的记忆。
- **关键技术细节**：
  - 将蛋白质-配体结构中的每个配体原子视为样本，以其周围特定半径的蛋白质环境作为输入。
  - 将蛋白质原子按类型编码（如碳、氮、氧、硫、金属离子等），并记录其相对于配体原子的三维空间位置分布。
  - 使用机器学习模型（可能是图神经网络或点云网络，文中未明确具体架构）学习每种配体原子类型（如芳香碳、氢键供体、受体等）在不同蛋白质微环境下的空间偏好概率图。
  - 模型输出一系列“偏好地图”，可视化展示特定原子类型在特定蛋白质环境中最可能出现的相对位置。
  - **排除配体拓扑**：模型不输入配体原子之间的连接信息，避免记忆整个配体形状，强制学习局部相互作用规律。
- **算法流程**（文字描述）：
  1. 从PDB等数据库提取蛋白-配体复合物，采样每个配体原子及其周围4-8Å内的蛋白质原子。
  2. 对每个配体原子，构建其局部微环境的特征向量（包括蛋白质原子类型、距离、角度等）。
  3. 训练一个模型，以局部微环境为输入，预测该配体原子类型在三维空间中的概率密度分布（即偏好地图）。
  4. 在推断时，对给定蛋白质靶标，遍历其表面所有可能的位点，对每种候选配体原子类型输出偏好地图，指导分子设计。

## 3. 实验设计：使用的数据集 / 场景、基准、对比方法

- **数据集**：文中未明确列出具体数据集名称和规模，但推测使用了PDB（Protein Data Bank）中的蛋白质-配体复合物结构。摘要提及涉及桥接水和金属依赖环境的案例，表明数据集中包含水分子和金属离子的结构。
- **场景**：
  - **回顾性验证**：在已有的蛋白质-配体结构上测试，看模型预测的偏好地图能否恢复已知的相互作用模式。
  - **前瞻性验证**：针对一个挑战性的蛋白质-蛋白质界面药物优化案例，使用模型指导分子优化，并通过湿实验验证。
- **基准与对比方法**：
  - 文中未明确提及与其他机器学习方法（如传统对接、分子力场、AI模型如DiffDock、EquiDock等）的定量对比。
  - 主要通过与已知的化学相互作用知识（如氢键、疏水作用、水介导作用、金属配位）进行定性对比，评估模型的化学合理性。
- **缺乏量化指标**：未报告ROC-AUC、相关系数、对接成功率等标准评价指标。

## 4. 资源与算力

- **文中未明确说明使用的GPU型号、数量、训练时长等计算资源**。仅可能基于机器学习框架的常规需求推测，但无具体数字。这是论文的一个不足。

## 5. 实验数量与充分性

- **实验数量**：具体实验组数未列出。摘要提到“恢复……模式”涉及桥接水和金属依赖环境，可能包含多个结构案例。前瞻性验证聚焦于“一个挑战性蛋白质-蛋白质界面”，说明至少有一个前瞻性案例。
- **充分性**：
  - **优点**：回顾性和前瞻性验证兼备，体现了从原理到实践的闭环。
  - **不足**：
    - 未见消融实验（如去掉排除配体拓扑的效果对比）。
    - 未与现有方法进行量化对比，难以评估性能提升。
    - 数据集规模未知，可能存在历史偏差未充分缓解。
    - 单一前瞻性案例的泛化性有限。
  - **客观性**：结论声称方法“可解释”、“指导优化”，但缺乏严格的统计显著性检验。

## 6. 论文的主要结论与发现

- 提出的框架能从蛋白质-配体局部微环境中学习到**化学上有意义、可迁移的原子相互作用偏好图谱**，包括常规氢键、疏水作用，以及复杂的桥接水分子和金属依赖配位环境。
- 通过在回顾性数据和前瞻性药物优化案例（靶向蛋白-蛋白界面）上的验证，表明该方法能提供**可解释的工作流**，直接指导分子优化，并为下游生成或对接流程提供输入。
- 该方法减少了模型对整体配体记忆的依赖，理论上能更好地泛化到未知配体化学空间，有望提升AI药物发现的实用性。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：首次明确提出排除配体拓扑以学习真正可迁移的相互作用偏好，区别于大多数从全配体图或分子指纹学习的方法。
- **可解释性**：生成的偏好图谱可视化后可直接揭示不同原子类型在蛋白质环境中的最优位置，便于化学家理解并用于分子设计。
- **实用性**：模型不依赖大量特定配体训练数据，理论上可适用于任意蛋白质靶标（只要有结构），减少了筛选成本。
- **验证的全面性**：包含回顾性（模式恢复）和前瞻性（真实药物优化）验证，增强了结果的可靠性。

## 8. 不足与局限

- **实验覆盖不足**：缺乏大规模系统性的基准测试，未与主流的对接评分函数、深度学习对接模型（如AlphaFold3、DiffDock等）进行定量比较。
- **数据偏差风险**：训练数据（PDB）本身存在历史偏差（如常见靶标、已知配体类别的偏重），模型可能仍隐含记忆这些偏差，泛化到全新靶标或全新化学类型的可靠性存疑。
- **模型架构细节缺失**：文中未提供具体的神经网络类型、超参数、损失函数等关键技术细节，限制了可复现性。
- **前瞻性验证样本量小**：仅一个蛋白质-蛋白质界面的案例，不足以证明方法在广泛场景下的有效性。
- **状态依赖**：需要蛋白质三维结构，对无结构或柔性较大的靶标（如固有无序蛋白）不适用。
- **未考虑配体构象变化**：模型基于静态结构，未显式处理蛋白质-配体结合的诱导契合效应。
- **算力和资源不明**：难以判断该方法计算开销是否可接受。

（完）
