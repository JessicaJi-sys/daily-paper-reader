---
title: "Rewiring Experts on the Fly: Continuous Rerouting for Better Online Adaptation in Mixture-of-Expert models"
title_zh: 即时重连专家：面向混合专家模型在线适应的持续重路由
authors: "Guinan Su, Yanwu Yang, Li Shen, Lu Yin, Shiwei Liu, Jonas Geiping"
date: 2025-09-16
pdf: "https://openreview.net/pdf?id=v5qb8BG18G"
tags: ["query:ddi-moe"]
score: 7.0
evidence: 分布偏移下MoE专家的动态重路由
tldr: 该文针对混合专家模型在部署时因分布偏移导致路由决策次优的问题，指出已有测试时适应方法多针对稠密模型且依赖外部数据。作者提出一种无需数据与监督的在线测试时框架，仅依据输入上下文持续动态调整专家选择。该方法在文本生成任务中改善了在线适应表现，为MoE在分布偏移下的动态路由提供了通用且实用的机制。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: MoE在部署时因分布偏移产生次优路由，现有适应方法多针对稠密模型且依赖外部数据。
method: 提出无数据、无监督的在线测试时框架，依据输入上下文持续优化专家选择。
result: 在文本生成任务中持续重路由提升了MoE的在线适应能力。
conclusion: 为分布偏移下MoE的动态专家路由提供了通用且可迁移的机制。
---

## Abstract
Mixture-of-Experts (MoE) models achieve efficient scaling through sparse expert activation, but often suffer from suboptimal routing decisions due to distribution shifts in deployment. While existing test-time adaptation methods could potentially address these issues, they primarily focus on dense models and require access to external data, limiting their practical applicability to MoE architectures. However, we find that, instead of relying on reference data, we can optimize MoE expert selection on-the-fly based only on input context. As such, we propose a data-free, online test-time framework that continuously adapts MoE routing decisions during text generation without external supervision or data. Our method cycles between two phases: During the prefill stage, and later in regular intervals, we optimize the routing decisions of the model using self-supervision based on the already generated sequence. Then, we generate text as normal, maintaining the
modified router until the next adaption. We implement this through lightweight additive vectors that only update router logits in selected layers, maintaining computational efficiency while preventing over-adaptation. The experimental results show consistent performance gains on challenging reasoning tasks while maintaining robustness to context shifts. For example, our method achieves a 5.5\% improvement on HumanEval with OLMoE. Furthermore, owing to its plug-and-play property, our method naturally complements existing test-time scaling techniques, e.g., achieving 6\% average gains when incorporated with self-consistency on DeepSeek-V2-Lite.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
分布偏移下MoE专家的动态重路由。

### 2. 核心内容
该文针对混合专家模型在部署时因分布偏移导致路由决策次优的问题，指出已有测试时适应方法多针对稠密模型且依赖外部数据。作者提出一种无需数据与监督的在线测试时框架，仅依据输入上下文持续动态调整专家选择。该方法在文本生成任务中改善了在线适应表现，为MoE在分布偏移下的动态路由提供了通用且实用的机制。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=v5qb8BG18G](https://openreview.net/forum?id=v5qb8BG18G)
