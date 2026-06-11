---
title: "DeepSynBa: Actionable Drug Combination Prediction with Complete Dose-Response Profiles"
title_zh: DeepSynBa：基于完整剂量-响应曲线的可操作性药物组合预测
authors: "Kuru, H. I., Zhang, H., Rattray, M., Ek, C. H., Cicek, A. E., Tastan, O., Milo, M."
date: 2026-06-11
pdf: "https://www.biorxiv.org/content/10.1101/2025.01.28.634673v2.full.pdf"
tags: ["query:cold-ddi"]
score: 6.0
evidence: 药物组合预测，属于药物相互作用的一种形式
tldr: "癌症组合疗法预测中现有模型仅输出单一协同得分，无法区分效价与效能。DeepSynBa通过预测完整剂量-反应矩阵并引入中间参数层，实现了对反应曲面的精细建模。在NCI-ALMANAC和O'Neil数据集上，DeepSynBa在多种测试场景下均超越现有方法，并能预测未测试组合的剂量-反应关系。该模型通过分离效能与效力，支持优化剂量选择以减少脱靶毒性，提升了预测的可操作性。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有模型预测聚合协同得分，忽略了剂量反应细节，导致预测不确定且不可操作。
method: 预测完整剂量-反应矩阵，通过中间参数层学习反应曲面参数。
result: "在NCI-ALMANAC和O'Neil数据集上，针对新药组合、细胞系等场景，均优于现有方法。"
conclusion: 分离效能与效力，指导优化剂量范围，推动药物组合研究。
---

## 摘要
许多癌症单一疗法临床疗效有限，使得联合疗法成为一种相关的治疗策略。潜在药物组合数量庞大且响应谱具有特异性，使得药物组合响应的预测变得复杂。现有计算模型通常训练用于预测单一聚合的协同评分，该评分总结了不同剂量组合下的药物响应，例如Bliss或Loewe评分。这种对药物响应曲面的过度简化导致预测不确定性高且可操作性有限，因为这些模型无法区分效价和效力。我们提出了DeepSynBa，一种可操作的模型，它预测药物对完整的剂量-响应矩阵，而非依赖聚合的协同评分。这是通过预测描述响应曲面的参数作为模型中间层来实现的。在NCI-ALMANAC和O'Neil数据集上评估，DeepSynBa在大多数评估场景中（包括在九种不同组织类型上测试新型药物组合、细胞系和药物）的剂量-响应矩阵预测任务中优于最先进方法。我们还展示了DeepSynBa生成可靠的协同评分预测。更重要的是，DeepSynBa能够预测未测试组合在不同剂量下的药物组合响应。中间的剂量-响应参数层能够将效力与效价分离，从而指导选择在实验筛选中优化效力同时限制脱靶毒性的剂量范围。预测能力和下游可操作性使DeepSynBa成为推动药物组合研究超越当前方法局限性的强大工具。

## Abstract
Many cancer monotherapies demonstrate limited clinical efficacy, making combination therapies a relevant treatment strategy. The extensive number of potential drug combinations and context-specific response profiles complicates the prediction of drug combination responses. Existing computational models are typically trained to predict a single aggregated synergy score, which summarises drug responses across different dosage combinations, such as Bliss or Loewe scores. This oversimplification of the drug-response surface leads to high prediction uncertainty and limited actionability, as these models fail to distinguish between potency and efficacy. We introduce DeepSynBa, an actionable model that predicts the complete dose-response matrix of drug pairs instead of relying on an aggregated synergy score. This is achieved by predicting parameters describing the response surface as an intermediate layer in the model. Evaluated on the NCI-ALMANAC and the O'Neil datasets, DeepSynBa outperforms the state-of-the-art methods in the dose-response matrix prediction task across most evaluation scenarios, including testing on novel drug combinations, cell lines, and drugs, across nine different tissue types. We also show that DeepSynBa yields reliable synergy score predictions. More importantly, DeepSynBa can predict drug combination responses across different dosages for untested combinations. The intermediate dose-response parameter layer enables the separation of efficacy from potency, informing the selection of dosage ranges that optimise efficacy while limiting off-target toxicity in experimental screens. The predictive capability and the downstream actionability make DeepSynBa a powerful tool for advancing drug combination research beyond the limitations of the current approaches.