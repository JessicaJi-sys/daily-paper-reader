---
title: "MolMAE: A Surface-Centric Multimodal Masked Autoencoder for Molecular Representation Learning"
title_zh: MolMAE：一种以表面为中心的多模态掩码自编码器用于分子表示学习
authors: "Li, J."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.11.737987v1.full.pdf"
tags: ["query:cold-ddi"]
score: 7.0
evidence: 以分子表面为中心的多模态表示学习，可用于跨域药物表示
tldr: 分子性质主要由分子表面决定，但现有分子表示学习模型多依赖SMILES、二维图或三维原子坐标，忽略了表面信息。本文提出MolMAE，一种表面引导的多模态掩码自编码器，同时处理分子表面点云、三维分子图和SMILES片段与官能团token，通过官能团对齐的掩码自编码联合重建表面几何、物理化学场、拓扑和结构信息。在约261K类药生物活性分子上预训练后，MolMAE在ESOL等分子性质预测任务上取得强性能，表明表面引导预训练可有效补充传统分子表示。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1687, \"height\": 887}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1701, \"height\": 719}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1617, \"height\": 1873}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1699, \"height\": 1754}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1306, \"height\": 2299}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1383, \"height\": 1147}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1692, \"height\": 1533}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1676, \"height\": 923}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1286, \"height\": 499}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1590, \"height\": 501}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1660, \"height\": 465}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-11-737987-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 616, \"height\": 282}]"
motivation: 现有分子表示学习忽视分子表面，但分子性质由表面几何和物理化学模式决定。
method: 提出MolMAE，以表面点云、3D图、SMILES片段和官能团token为输入，通过官能团对齐的掩码自编码联合重建表面几何、静电势等。
result: 在约261K类药分子上预训练，在ESOL基准和多项性质预测任务上取得强性能。
conclusion: 分子表面引导预训练可补充传统图、序列和坐标表示，尤其适用于受表面几何影响的性质预测。
---

## 摘要
分子表示学习已成为现代计算药物发现的核心组成部分。现有的分子基础模型主要依赖于SMILES字符串、二维分子图或三维原子坐标。然而，许多分子性质最终由分子表面决定，分子间识别、溶剂化、静电互补性和配体-蛋白质相互作用都发生在分子表面。在这项工作中，我们提出了MolMAE，一种表面引导的多模态掩码自编码器用于分子表示学习。MolMAE将分子表面点云、三维分子图以及SMILES衍生的片段和官能团标记作为互补的输入模态，并通过官能团对齐的掩码自编码学习统一的、多模态的分子嵌入。在预训练期间，化学上对应的局部区域在表面、图、片段和官能团视图上被联合掩码，迫使模型从剩余上下文中重建缺失的几何、物理化学、结构和语义信息。虽然分子表面重建是主要的预训练目标，但图、片段和官能团级别的重建任务提供了互补的监督，鼓励模型捕捉分子拓扑结构、键合模式、立体化学、局部化学环境和子结构组织。除了重建表面几何外，MolMAE还重建表面相关的物理化学场，包括静电势和福井相关描述符，使模型能够学习具有化学意义的表面表示。在约261K个铅类生物活性分子上预训练后，MolMAE在脚手架分割下的ESOL基准测试中取得了强劲的性能，并在多个分子性质预测任务中表现出竞争力。这些结果表明，分子表面引导的预训练可以补充传统的基于图、序列和原子坐标的分子表示，特别是对于受暴露表面几何和表面相关物理化学模式影响的性质预测任务。

## 速览
**TLDR**：分子性质由表面决定，但现有表示学习忽视表面。MolMAE以表面点云、3D图和SMILES片段为多模态输入，通过联合掩码重建几何、物理化学场和结构信息。预训练于26万分子，在ESOL等任务上表现优异。该方法为分子表面感知的表示学习提供了新范式。 \
**Motivation**：现有分子表示学习忽略决定性质的分子表面，缺乏对表面几何和物理化学场的捕获。 \
**Method**：提出MolMAE，利用表面点云、3D图和片段令牌多模态输入，通过官能团对齐的掩码自编码联合重建表面、图、片段和官能团。 \
**Result**：在26万分子上预训练，ESOL骨架划分任务性能强，多个性质预测任务有竞争力。 \
**Conclusion**：分子表面引导预训练能补充传统表示，尤其适用于表面相关性质预测。

---

## Abstract
Molecular representation learning has become a central component of modern computational drug discovery. Existing molecular foundation models mainly rely on SMILES strings, two-dimensional molecular graphs, or three-dimensional atomic coordinates. However, many molecular properties are ultimately governed by the molecular surface, where intermolecular recognition, solvation, electrostatic complementarity, and ligand-protein interactions occur. In this work, we propose MolMAE, a surface-guided multimodal masked autoencoder for molecular representation learning. MolMAE takes molecular surface point clouds, three-dimensional molecular graphs, and SMILES-derived fragment and functional-group tokens as complementary input modalities, and learns a unified multimodal molecular embedding through functional-group-aligned masked autoencoding. During pretraining, chemically corresponding local regions are jointly masked across surface, graph, fragment, and functional-group views, forcing the model to reconstruct missing geometric, physicochemical, structural, and semantic information from the remaining context. While molecular surface reconstruction serves as the primary pretraining objective, graph-, fragment-, and functional-group-level reconstruction tasks provide complementary supervision that encourages the model to capture molecular topology, bonding patterns, stereochemistry, local chemical environments, and substructure organization. In addition to reconstructing surface geometry, MolMAE reconstructs surface-associated physicochemical fields, including electrostatic potential and Fukui-related descriptors, enabling the model to learn chemically meaningful surface representations. Pretrained on approximately 261K lead-like bioactive molecules, MolMAE achieves strong performance on the ESOL benchmark under scaffold splitting and competitive performance across multiple molecular property prediction tasks. These results suggest that molecular surface-guided pretraining can complement conventional graph-, sequence-, and atom-coordinate-based molecular representations, especially for property prediction tasks influenced by exposed surface geometry and surface-associated physicochemical patterns.