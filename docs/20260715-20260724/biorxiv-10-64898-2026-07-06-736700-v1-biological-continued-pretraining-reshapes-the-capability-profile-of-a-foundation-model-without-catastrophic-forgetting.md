---
title: Biological Continued Pretraining Reshapes the Capability Profile of a Foundation Model Without Catastrophic Forgetting
title_zh: 生物持续预训练重塑基础模型的能力轮廓而不导致灾难性遗忘
authors: "Wang, L."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.06.736700v1.full.pdf"
tags: ["query:mgp"]
score: 7.0
evidence: 生物序列持续预训练
tldr: "通常认为领域持续预训练会降低通用模型能力，但本文无新增训练，直接分析Gemma-4-26B-A4B三阶段检查点发现：生物CPT在8.7B token后，MMLU提升13分，MBPP pass@1从0.33升至0.63，BixBench MCC从0.23升至0.92，且CoW推理缩短41%无回溯；随后SFT反而使所有指标回退至基座水平。这表明生物序列重塑而非占用模型能力，CPT与SFT应互为补充。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 795, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1534, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 964, \"height\": 880, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1040, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1784, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736700-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1506, \"height\": 287, \"label\": \"Table\"}]"
motivation: 验证领域持续预训练是否必然导致灾难性遗忘，挑战“无免费午餐”直觉。
method: 无训练分析同一26B MoE模型在指令微调、生物CPT、后续SFT三阶段检查点的通用、代码、生物医学能力。
result: 生物CPT提升MMLU+13、MBPP翻倍、BixBench MCC达0.92；后续SFT使所有指标降回近基座水平。
conclusion: CPT与SFT互补，生物序列作为结构化数据重塑能力剖面，而非削弱通用能力。
---

## 摘要
人们普遍认为，在狭窄的分布外语料库（如原始生物序列）上进行持续预训练（CPT）必然会牺牲通用模型的广泛能力——即“对齐税”或灾难性遗忘的直觉。我们直接对此进行了测试，无需任何新训练，通过重新分析一个26B参数混合专家模型（Gemma-4-26B-A4B）同一谱系中的三个检查点：指令微调的基础模型、该模型经过生物CPT（87亿个DNA、蛋白质和生物医学文本标记）后的版本，以及随后经过监督微调（SFT）的版本。在三个独立的能力轴——通用知识/推理（MMLU、ARC、HellaSwag）、代码生成（MBPP）和生物医学知识（BixBench）上，我们发现生物CPT并未降低模型性能；反而提升了它：MMLU提高13分，MBPP pass@1几乎翻倍（0.33→0.63），BixBench判别力急剧上升（MCC 0.23→0.92）。唯一测得的回归是真实性（TruthfulQA下降8.8分），这是一个微小且可解释的领域漂移。一个干净的词汇扩展消融实验（每项通用指标<0.4分）证实了这些增益归因于CPT，而非分词器变化。关键在于，后续的SFT将模型拉回：所有三个轴都下降到接近基础水平，揭示了一种一致的劳动分工——CPT重新组织并提升共享的能力基础；SFT则将其兑现到目标任务上。我们认为，这重新定义了生物序列并非与基础模型的能力竞争，而是一种结构化的科学数据，重塑了其能力轮廓，并且CPT和SFT应被视为互补而非可互换的阶段。所有检查点、评估代码和每个样本的输出均已公开。

亮点
• 对同一26B MoE谱系进行免训练重新分析，将生物持续预训练（CPT）的效果与分词器变化和微调区分开来。
• 生物CPT不会导致灾难性遗忘；它提升了通用知识（MMLU +13分）和代码生成（MBPP pass@1从0.33到0.63）。
• CPT还使思维链推理缩短41%，且几乎无回溯，同时保持准确性——这是准确性指标无法捕捉的效果。
• 在四个轴上重复出现一致的CPT提升/SFT缩窄的劳动分工，将生物序列重新定义为重塑模型能力轮廓的结构化科学数据。

更广阔的视角
将通用AI模型适应于专业领域——此处是DNA和蛋白质的语言——通常被认为需要付出代价：教会它生物学就会忘记如何推理其他一切。这种“没有免费午餐”的直觉塑造了从业者如何分配计算资源，以及他们是否尝试领域适应。我们直接测试了这一假设，无需进行任何新训练，通过比较同一模型在生物训练前后的三个快照。结果推翻了这一直觉：将原始生物序列输入模型使其在通用知识、编写代码方面变得更好，甚至改变了它的推理方式——产生更短、更果断的思维链而不损失准确性。这些增益出现在序列预训练阶段，并在任务特定的微调期间部分被返还，揭示了这两个阶段发挥着互补而非可互换的作用。这为以数据为中心的AI提出了一个更广泛的原则：结构化的科学数据——今天的生物序列，进而扩展至代码、数学和化学——不仅仅是需要吸收的知识，而是重塑基础模型能力的杠杆。

## Abstract
It is widely assumed that continued pretraining (CPT) on a narrow, out-of-distribution corpus such as raw biological sequence must trade away a general-purpose models broad competence -- the "alignment tax" or catastrophic-forgetting intuition. We test this directly, without any new training, by re-analyzing three checkpoints from a single lineage of a 26B-parameter Mixture-of-Experts model (Gemma-4-26B-A4B): the instruction-tuned base, the same model after biological CPT (8.7B tokens of DNA, protein, and biomedical text), and after subsequent supervised fine-tuning (SFT). Across three independent capability axes -- general knowledge/reasoning (MMLU, ARC, HellaSwag), code generation (MBPP), and biomedical knowledge (BixBench) -- we find that biological CPT does not degrade the model; it lifts it: MMLU +13 points, MBPP pass@1 nearly doubles (0.33 [-&gt;]0.63), and BixBench discrimination rises sharply (MCC 0.23 [-&gt;] 0.92). The single measured regression is truthfulness (TruthfulQA 8.8 points), a small and interpretable domain drift. A clean vocabulary-expansion ablation (< 0.4 pt on every general metric) confirms the gains are attributable to CPT, not tokenizer changes. Crucially, subsequent SFT narrows the model back: all three axes fall to near-base levels, revealing a consistent division of labor -- CPT re-organizes and lifts the shared capability substrate; SFT cashes it out onto target tasks. We argue this reframes biological sequence not as a competitor for a foundation models capacity but as a form of structured scientific data that reshapes its capability profile, and that CPT and SFT should be budgeted as complementary rather than substitutable stages. All checkpoints, evaluation code, and per-example outputs are public.

HighlightsO_LIA training-free re-analysis of one 26B MoE lineage isolates the effect of biological continued pretraining (CPT) from tokenizer changes and from fine-tuning.
C_LIO_LIBiological CPT does not cause catastrophic forgetting; it raises general knowledge (MMLU +13 pts) and code generation (MBPP pass@1 0.33[-&gt;] 0.63).
C_LIO_LICPT also makes chain-of-thought reasoning 41% shorter and near-backtrack-free while pre-serving accuracy -- an effect invisible to accuracy metrics.
C_LIO_LIA consistent CPT-lifts / SFT-narrows division of labor recurs across four axes, reframing biological sequence as structured scientific data that reshapes a models capability profile.
C_LI

The Bigger PictureAdapting a general-purpose AI model to a specialized domain -- here, the language of DNA and proteins -- is usually assumed to come at a cost: teach it biology and it forgets how to reason about everything else. This "no free lunch" intuition shapes how practitioners budget compute and whether they attempt domain adaptation at all. We test the assumption directly, and without running any new training, by comparing three snapshots of the same model taken before and after biological training. The result overturns the intuition: feeding the model raw biological sequence made it better at general knowledge, at writing code, and even changed how it reasons -- producing shorter, more decisive chains of thought without losing accuracy. The gains appear during the sequence-pretraining stage and are partly given back during task-specific fine-tuning, revealing that the two stages play complementary rather than interchangeable roles. This suggests a broader principle for data-centric AI: structured scientific data -- biological sequence today, and by extension code, mathematics, and chemistry -- is not merely knowledge to be absorbed but a lever that reshapes what a foundation model can do.