---
title: "DAG-MoE: From Simple Mixture to Structural Aggregation in Mixture-of-Experts"
title_zh: DAG-MoE：从简单混合到混合专家中的结构化聚合
authors: "Jiarui Feng, Hanqing Zeng, Karish Grover, Ruizhong Qiu, Yinglong Xia, Qiang Zhang, Qifan Wang, Ren Chen, Dongqi Fu, Jiayi Liu, Zhuokai Zhao, Xiangjun Fan, Benyu Zhang, Yixin Chen"
date: 2026-04-30
pdf: "https://openreview.net/pdf/a680c8ec181dca96b830038c5484dfd13c29e3a6.pdf"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 混合专家中专家输出的结构化聚合
tldr: 细粒度专家虽扩大专家组合空间并提升灵活性，却带来路由开销瓶颈，MoE 的有效扩展面临挑战。本文从专家输出聚合入手，提出用结构化聚合替代标准加权求和。理论分析表明，结构化聚合在不改动专家与路由器的前提下扩大专家组合空间，并支持单层内多步推理。其贡献在于为 MoE 扩展提供聚合维度的新方向，可能增强专家组合的表达能力。
source: ICML-2026-Accepted
selection_source: conference_retrieval
motivation: 细粒度专家虽扩大专家组合空间，却带来路由开销瓶颈，MoE 的有效扩展面临挑战。
method: 提出从专家输出聚合入手，用结构化聚合替代标准加权求和，在不改动专家与路由器的前提下扩展组合空间。
result: 理论证明结构化聚合可扩大专家组合空间，并支持单层内的多步推理。
conclusion: 为 MoE 扩展提供聚合维度的新方向，可能增强专家组合的表达能力。
---

## Abstract
Mixture-of-Experts (MoE) models have become a leading approach for decoupling parameter count from computational cost in large language models, yet effectively scaling MoE performance remains a challenge. Prior work shows that fine-grained experts enlarge the space of expert combinations and improve flexibility, but they also impose substantial routing overhead, creating a new scalability bottleneck. In this paper, we explore a complementary axis for scaling—how expert outputs are aggregated. We theoretically show that replacing the standard weighted-summation aggregation with structural aggregation expands the expert-combination space without altering the experts or router, and enables possible multi-step reasoning within a single MoE layer. To this end, we propose DAG-MoE, a sparse MoE framework that employs a lightweight module to automatically learn the optimal aggregation structure among the selected experts. Extensive experiments under standard language modeling settings show that DAG-MoE consistently improves performance in both pretraining and fine-tuning, surpassing traditional MoE baselines.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
混合专家中专家输出的结构化聚合。

### 2. 核心内容
细粒度专家虽扩大专家组合空间并提升灵活性，却带来路由开销瓶颈，MoE 的有效扩展面临挑战。本文从专家输出聚合入手，提出用结构化聚合替代标准加权求和。理论分析表明，结构化聚合在不改动专家与路由器的前提下扩大专家组合空间，并支持单层内多步推理。其贡献在于为 MoE 扩展提供聚合维度的新方向，可能增强专家组合的表达能力。

### 3. 对应检索需求
mixture-of-experts architecture for drug pair modeling。

### 4. 来源与原文
- Source：ICML-2026-Accepted
- OpenReview：[https://openreview.net/forum?id=yv1iRquxF9](https://openreview.net/forum?id=yv1iRquxF9)
