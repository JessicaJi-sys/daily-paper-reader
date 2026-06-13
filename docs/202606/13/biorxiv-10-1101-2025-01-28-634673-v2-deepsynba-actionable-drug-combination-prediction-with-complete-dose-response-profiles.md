---
title: "DeepSynBa: Actionable Drug Combination Prediction with Complete Dose-Response Profiles"
title_zh: DeepSynBa：基于完整剂量-反应曲线的可行药物组合预测
authors: "Kuru, H. I., Zhang, H., Rattray, M., Ek, C. H., Cicek, A. E., Tastan, O., Milo, M."
date: 2026-06-11
pdf: "https://www.biorxiv.org/content/10.1101/2025.01.28.634673v2.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 预测药物组合剂量反应曲线
tldr: "现有癌症组合疗法预测模型通常只能输出单一聚合协同分数，无法区分效能与 potency，导致高不确定性和有限可操作性。DeepSynBa通过预测完整剂量反应矩阵并引入中间参数层，能够分离效能与 potency。在NCI-ALMANAC和O'Neil数据集上，DeepSynBa在预测新组合、细胞系和药物时表现优于现有方法。该模型不仅可靠预测协同分数，还能指导剂量选择以优化疗效并降低毒性，为药物组合研究提供了强大工具。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有模型预测单一聚合协同分数，忽略剂量响应表面的完整信息，导致预测不确定性高且缺乏可操作性。
method: DeepSynBa预测完整剂量反应矩阵，通过中间参数层描述反应表面，分离效能与 potency。
result: "在NCI-ALMANAC和O'Neil数据集上，DeepSynBa在多种评估场景中优于现有方法，能可靠预测协同分数并指导剂量选择。"
conclusion: DeepSynBa结合预测能力与下游可操作性，克服了现有方法的局限性，推进了药物组合研究。
---

## 摘要
许多癌症单一疗法表现出有限的临床疗效，使得联合疗法成为一种相关的治疗策略。大量潜在的药物组合和特定背景的反应谱使药物组合反应的预测变得复杂。现有计算模型通常被训练以预测单一的聚合协同得分，该得分总结了不同剂量组合下的药物反应，例如Bliss或Loewe评分。这种对药物反应表面的过度简化导致高预测不确定性和有限的可操作性，因为这些模型无法区分效价和效力。我们提出了DeepSynBa，一种可操作的模型，它预测药物对的完整剂量-反应矩阵，而不是依赖于聚合的协同得分。这是通过预测描述反应表面的参数作为模型中间层来实现的。在NCI-ALMANAC和O'Neil数据集上评估，DeepSynBa在大多数评估场景（包括对新药物组合、细胞系和药物以及九种不同组织类型的测试）中的剂量-反应矩阵预测任务上优于最先进的方法。我们还表明DeepSynBa能产生可靠的协同得分预测。更重要的是，DeepSynBa可以预测未经测试组合在不同剂量下的药物组合反应。中间的剂量-反应参数层能够区分效力与效价，从而指导选择能够在实验筛选中优化效力同时限制脱靶毒性的剂量范围。预测能力和下游可操作性使DeepSynBa成为推进药物组合研究超越当前方法局限性的强大工具。

## Abstract
Many cancer monotherapies demonstrate limited clinical efficacy, making combination therapies a relevant treatment strategy. The extensive number of potential drug combinations and context-specific response profiles complicates the prediction of drug combination responses. Existing computational models are typically trained to predict a single aggregated synergy score, which summarises drug responses across different dosage combinations, such as Bliss or Loewe scores. This oversimplification of the drug-response surface leads to high prediction uncertainty and limited actionability, as these models fail to distinguish between potency and efficacy. We introduce DeepSynBa, an actionable model that predicts the complete dose-response matrix of drug pairs instead of relying on an aggregated synergy score. This is achieved by predicting parameters describing the response surface as an intermediate layer in the model. Evaluated on the NCI-ALMANAC and the O'Neil datasets, DeepSynBa outperforms the state-of-the-art methods in the dose-response matrix prediction task across most evaluation scenarios, including testing on novel drug combinations, cell lines, and drugs, across nine different tissue types. We also show that DeepSynBa yields reliable synergy score predictions. More importantly, DeepSynBa can predict drug combination responses across different dosages for untested combinations. The intermediate dose-response parameter layer enables the separation of efficacy from potency, informing the selection of dosage ranges that optimise efficacy while limiting off-target toxicity in experimental screens. The predictive capability and the downstream actionability make DeepSynBa a powerful tool for advancing drug combination research beyond the limitations of the current approaches.