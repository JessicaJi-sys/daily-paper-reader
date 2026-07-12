---
title: A control-validated pan-proteome deep-learning pipeline nominates GPR35 as a candidate target of the orphan bacterial metabolite ligiamycin A
title_zh: 一种经过对照验证的泛蛋白质组深度学习流程提名GPR35为孤儿细菌代谢物ligiamycin A的候选靶点
authors: "Martin, J."
date: 2026-07-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.01.735807v1.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 使用蛋白质语言模型和深度学习进行药物-靶标相互作用预测
tldr: 多数天然产物活性已知但靶点不明。本文提出控制验证的深度学习流程：采用图神经网络编码配体、ESM-2编码蛋白质，通过双向交叉注意力学习相互作用，结合偏差校正排名和分子对接，预测2022年发现的ligiamycin A靶点。原始模型显示候选主要是A类GPCR；用losartan校正频繁命中偏差后，孤儿受体GPR35排名最高。分子对接证实ligiamycin A与GPR35激动剂口袋结合（得分-8.1 kcal/mol，与已知激动剂zaprinast相当），而FFAR1被排除，组胺H2不明确。因此提出GPR35是优先实验验证靶点，并发布可重用计算工作流。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-01-735807-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1270, \"height\": 1187, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-01-735807-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1658, \"height\": 599, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-01-735807-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1271, \"height\": 803, \"label\": \"Figure\"}]"
motivation: 大多数天然产物有生物活性但缺少已知分子靶点，限制了其开发；需要一种可验证的计算方法生成靶点假设。
method: 构建全蛋白质组深度学习DTI模型，包括图神经网络配体编码器、ESM-2蛋白质编码器和双向交叉注意力，结合偏差校正排名与正负对照分子对接。
result: 流程应用于ligiamycin A，预测候选主要为A类GPCR；经偏差校正后孤儿受体GPR35得分最高，分子对接显示其与zaprinast得分相当（-8.1 vs -8.3 kcal/mol）。
conclusion: 提出GPR35作为ligiamycin A的优先实验验证靶点，该计算假说需进一步实验确认，工作流已开源可重用。
---

## 摘要
大多数具有文献记载生物活性的微生物天然产物缺乏已识别的分子靶点，这限制了其开发。我们提出了一种开放的、经过对照验证的计算流程，用于天然产物靶点假设的生成。该流程结合了泛蛋白质组深度学习药物-靶点相互作用模型（图神经网络配体编码器、ESM-2蛋白质语言模型编码器和双向交叉注意力）与偏差校正排名及对照锚定分子对接。将其应用于ligiamycin A（一种2022年描述的链霉菌/无色杆菌共培养产生的十氢化萘-氨基-马来酰亚胺，尚无报道的靶点），我们发现该化合物预测的相互作用主要集中于A类G蛋白偶联受体。使用已知靶点药物氯沙坦，我们识别并校正了原始模型中的频繁命中偏差；校正后，突出候选物均为A类G蛋白偶联受体，其中孤儿受体GPR35位居首位。针对三个候选物进行匹配阳性和阴性对照的基于结构的对接，特异性地证实了GPR35：在激动剂结合口袋中，ligiamycin A的得分与已知GPR35激动剂扎普司特相当（-8.1 vs -8.3 kcal/mol；非结合底限-5.5），而FFAR1被排除，组胺H2结果不明确。我们提出GPR35作为优先的、可实验验证的靶点，并将该工作流程作为可复用的工具发布。结果是一个需要实验验证的计算假设。

## Abstract
Most microbial natural products with documented bioactivity lack an identified molecular target, which limits their development. We present an open, control-validated computational pipeline for natural-product target hypothesis generation. It combines a pan-proteome deep-learning drug-target interaction (DTI) model (a graph neural-network ligand encoder, an ESM-2 protein language-model encoder, and bidirectional cross-attention) with bias-corrected ranking and control-anchored molecular docking. Applying it to ligiamycin A, a 2022-described Streptomyces/Achromobacter co-culture decalin-amino-maleimide with no reported target, we find that the predicted interactions of the compound are dominated by class-A G-protein-coupled receptors. Using a drug with a known target (losartan) we identify and correct a frequent-hitter bias in the raw model; after correction the standout candidates are uniformly class-A GPCRs, led by the orphan receptor GPR35. Structure-based docking with matched positive and negative controls across three candidates corroborates GPR35 specifically: ligiamycin A scores comparably to the known GPR35 agonist zaprinast at the agonist pocket (-8.1 vs -8.3 kcal/mol; non-binder floor -5.5), whereas FFAR1 is excluded and histamine H2 is inconclusive. We propose GPR35 as a prioritized, experimentally testable target and release the workflow as a reusable tool. The result is a computational hypothesis that requires experimental validation.