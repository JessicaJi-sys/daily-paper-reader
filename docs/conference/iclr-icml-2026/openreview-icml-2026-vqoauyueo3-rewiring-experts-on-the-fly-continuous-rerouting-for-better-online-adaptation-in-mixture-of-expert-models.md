---
title: "Rewiring Experts on the Fly: Continuous Rerouting for Better Online Adaptation in Mixture-of-Expert Models"
title_zh: 即时重连专家：面向混合专家模型在线适应的持续重路由
authors: "Guinan Su, Yanwu Yang, Li Shen, Lu Yin, Shiwei Liu, Jonas Geiping"
date: 2026-04-30
pdf: "https://openreview.net/pdf/5ef3f1852abe33996089a6849728c61f6cf6f207.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 面向部署分布漂移的MoE专家在线动态重路由
tldr: 混合专家模型在部署时因分布漂移常出现次优路由，而现有测试时适应方法多针对稠密模型且依赖外部数据。作者提出一种无数据在线框架，仅依据输入上下文在生成过程中持续重路由专家。实验表明该方法无需外部监督即可动态优化专家选择，为MoE在分布漂移下的动态路由适应提供了实用方案。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: MoE在部署时因分布漂移导致路由次优，现有测试时适应方法多面向稠密模型。
method: 提出无数据在线框架，仅凭输入上下文在生成中持续重路由专家。
result: 无需外部数据与监督即可动态优化专家选择，提升在线适应。
conclusion: 为MoE在分布漂移下的动态路由提供轻量在线适应方案。
---

## Abstract
Mixture-of-Experts (MoE) models achieve efficient scaling through sparse expert activation, but often suffer from suboptimal routing decisions due to distribution shifts in deployment. While existing test-time adaptation methods could potentially address these issues, they primarily focus on dense models and require access to external data, limiting their practical applicability to MoE architectures. However, we find that, instead of relying on reference data, we can optimize MoE expert selection on-the-fly based only on input context. As such, we propose *a data-free, online test-time framework* that continuously adapts MoE routing decisions during text generation without external supervision or data. Our method cycles between two phases: During the prefill stage, and later in regular intervals, we optimize the routing decisions of the model using self-supervision based on the already generated sequence. Then, we generate text as normal, maintaining the modified router until the next adaption. We implement this through lightweight additive vectors that only update router logits in selected layers, maintaining computational efficiency while preventing over-adaptation. The results show consistent performance gains on challenging reasoning tasks while maintaining robustness to context shifts. For example, our method achieves a 5.5\% improvement on HumanEval with OLMoE. Furthermore, owing to its plug-and-play property, our method complements existing test-time scaling techniques, e.g., achieving 6\% average gains when incorporated with self-consistency on DeepSeek-V2-Lite.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
面向部署分布漂移的MoE专家在线动态重路由。

### 2. 核心内容
混合专家模型在部署时因分布漂移常出现次优路由，而现有测试时适应方法多针对稠密模型且依赖外部数据。作者提出一种无数据在线框架，仅依据输入上下文在生成过程中持续重路由专家。实验表明该方法无需外部监督即可动态优化专家选择，为MoE在分布漂移下的动态路由适应提供了实用方案。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=vqOaUyUeO3](https://openreview.net/forum?id=vqOaUyUeO3)
