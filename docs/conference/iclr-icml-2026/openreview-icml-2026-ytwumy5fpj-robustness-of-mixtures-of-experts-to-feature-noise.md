---
title: Robustness of Mixtures of Experts to Feature Noise
title_zh: 专家混合模型对特征噪声的鲁棒性
authors: "Dong Sun, Rahul Nittala, Rebekka Burkholz"
date: 2026-04-30
pdf: "https://openreview.net/pdf/f66ba4597fbfb910b01b25015a91c90f67c7af0e.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 稀疏专家激活作为噪声滤波器提升泛化的理论
tldr: 针对专家混合模型为何优于稠密网络、尤其在特征噪声与潜在模块化结构下机理不明的问题，本文在等参数设定下进行理论与实证研究。分析表明稀疏专家激活充当噪声滤波器，相较稠密估计器，MoE在特征噪声下具有更低的泛化误差、更强的抗扰动能力与更快的收敛速度。合成数据与真实语言任务的实验一致印证了上述理论。该工作从理论层面解释MoE的鲁棒性优势，支持其在分布偏移场景下的泛化应用。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: MoE为何优于稠密网络尚不清晰，尤其在特征噪声与潜在模块化结构下的机理未被充分理解。
method: 在等参数设定下理论分析稀疏专家激活，将MoE与稠密估计器在特征噪声下的泛化误差进行对比。
result: 证明稀疏激活充当噪声滤波器，MoE泛化误差更低、抗扰动更强、收敛更快，合成与语言实验印证。
conclusion: 从理论层面解释MoE的鲁棒性优势，支持其在分布偏移与噪声场景下的泛化应用。
---

## Abstract
Despite their practical success, it remains unclear why Mixture of Experts (MoE) models can outperform dense networks beyond sheer parameter scaling. We study an iso-parameter regime where inputs exhibit latent modular structure but are corrupted by feature noise, a proxy for noisy internal activations. We show that sparse expert activation acts as a noise filter: compared to a dense estimator, MoEs achieve lower generalization error under feature noise, improved robustness to perturbations, and faster convergence speed. Empirical results on synthetic data and real-world language tasks corroborate the theoretical insights, demonstrating consistent robustness and efficiency gains from sparse modular computation.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
稀疏专家激活作为噪声滤波器提升泛化的理论。

### 2. 核心内容
针对专家混合模型为何优于稠密网络、尤其在特征噪声与潜在模块化结构下机理不明的问题，本文在等参数设定下进行理论与实证研究。分析表明稀疏专家激活充当噪声滤波器，相较稠密估计器，MoE在特征噪声下具有更低的泛化误差、更强的抗扰动能力与更快的收敛速度。合成数据与真实语言任务的实验一致印证了上述理论。该工作从理论层面解释MoE的鲁棒性优势，支持其在分布偏移场景下的泛化应用。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=Ytwumy5fpJ](https://openreview.net/forum?id=Ytwumy5fpJ)
