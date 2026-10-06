---
title: Adaptive Conformal Prediction via Mixture-of-Experts Gating Similarity
title_zh: 基于专家混合门控相似度的自适应保形预测
authors: "Jingsen Kong, Wenlu Tang, Dezheng Kong, Linglong Kong, Guangren Yang, Bei Jiang"
date: 2026-01-26
pdf: "https://openreview.net/pdf?id=vCmnu4q8C3"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 用MoE门控向量作为软域分配，无需显式域标签即可适应潜在子群
tldr: 现有保形预测方法忽视数据异质性，覆盖率保证难以适应现代多模态数据中的潜在子群。该文提出MoE-CP框架，利用专家混合模型的门控概率向量作为软域分配，对校准残差进行相似度加权，从而在无需显式域标签的情况下生成自适应预测区间。理论与实验表明该方法能灵活、可扩展地贴合潜在子群结构。其贡献在于把MoE路由信号转化为分布感知的校准机制，为异质分布下的不确定性建模提供了新思路。
source: ICLR-2026-Accepted
selection_source: conference_retrieval
motivation: 现有保形预测忽视数据异质性与域知识，覆盖率保证难以贴合现代多模态数据的潜在子群结构。
method: 提出MoE-CP框架，将专家混合模型的门控概率向量作为软域分配，按门控向量相似度对校准残差加权。
result: 无需显式域标签即可生成自适应于潜在子群的预测区间，并给出相应理论保证，实验验证其灵活可扩展。
conclusion: 把MoE路由信号转化为分布感知的保形校准机制，为异质分布下的不确定性量化提供了通用思路。
---

## Abstract
Prediction intervals are essential for applying machine learning models in real applications, yet most conformal prediction (CP) methods provide coverage guarantees that overlook the heterogeneity and domain knowledge that characterize modern multimodal datasets. We introduce Mixture-of-Experts Conformal Prediction (MoE-CP), a flexible and scalable framework that uses the gating probability vectors of Mixture-of-Experts (MoE) models as soft domain assignments to guide similarity-weighted conformal calibration. MoE-CP weights calibration residuals according to the similarity between gating vectors of calibration and test points, producing prediction intervals that adapt to latent subpopulations without requiring explicit domain labels. We provide theoretical justification showing that MoE-CP preserves nominal marginal validity under common similarity measures and improves conditional adaptivity when the gating captures domain structure. Empirical results on synthetic and real-world datasets demonstrate that MoE-CP yields more domain-aware, interpretable, and often tighter intervals than existing conformal baselines while maintaining target coverage. MoE-CP offers a practical route to reliable uncertainty quantification in latent heterogeneous, multi-domain environments.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
用MoE门控向量作为软域分配，无需显式域标签即可适应潜在子群。

### 2. 核心内容
现有保形预测方法忽视数据异质性，覆盖率保证难以适应现代多模态数据中的潜在子群。该文提出MoE-CP框架，利用专家混合模型的门控概率向量作为软域分配，对校准残差进行相似度加权，从而在无需显式域标签的情况下生成自适应预测区间。理论与实验表明该方法能灵活、可扩展地贴合潜在子群结构。其贡献在于把MoE路由信号转化为分布感知的校准机制，为异质分布下的不确定性建模提供了新思路。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=vCmnu4q8C3](https://openreview.net/forum?id=vCmnu4q8C3)
