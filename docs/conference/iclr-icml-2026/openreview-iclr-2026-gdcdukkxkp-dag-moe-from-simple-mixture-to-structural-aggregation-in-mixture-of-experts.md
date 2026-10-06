---
title: "DAG-MoE: From Simple Mixture to Structural Aggregation in Mixture-of-Experts"
title_zh: DAG-MoE：从简单混合到专家混合中的结构化聚合
authors: "Jiarui Feng, Hanqing Zeng, Karish Grover, Ruizhong Qiu, Yinglong Xia, Qiang Zhang, Qifan Wang, Ren Chen, Dongqi Fu, Jiayi Liu, Zhuokai Zhao, Xiangjun Fan, Benyu Zhang, Yixin Chen"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=gdCdukkxKP"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 专家输出的结构化聚合扩展了专家组合空间，超越简单加权求和
tldr: 专家混合模型已成为解耦参数量与计算成本的主流方案，但细粒度专家带来路由开销与扩展瓶颈。该文转而探索专家输出混合这一新维度，先分析传统加权求和聚合的局限，再理论证明引入结构化聚合能扩展专家组合空间并提升灵活性。基于此提出DAG-MoE，用结构化聚合替代简单加权求和。其贡献在于为专家路由与聚合机制的设计提供了可迁移的结构化改进思路。
source: ICLR-2026-Rejected-Public
selection_source: conference_retrieval
motivation: 细粒度专家虽提升灵活性，却带来显著路由开销与扩展瓶颈，传统加权求和聚合存在局限。
method: 提出DAG-MoE，用结构化聚合替代标准加权求和，扩展专家组合空间并降低路由瓶颈。
result: 理论证明结构化聚合可扩大专家组合并提升扩展灵活性，实验验证其在MoE扩展上的优势。
conclusion: 为专家路由与输出聚合机制提供了可迁移的结构化设计思路。
---

## Abstract
Mixture-of-Experts (MoE) models have become a leading approach for decoupling parameter count from computational cost in large language models. Despite significant progress, effectively scaling MoE performance remains a challenge. Previous work shows that the use of fine-grained experts enlarges the space of expert combinations and can improve flexibility, but it also imposes substantial routing overhead, creating a new scalability bottleneck. In this paper, we explore a complementary axis for scaling --- expert-output mixture. We first analyze the limitations of the standard weighted-summation aggregation in conventional MoE architectures. We then theoretically demonstrate that introducing structural aggregation both expands the expert-combination space without altering the experts or router configuration and enables possible multi-step reasoning within a single MoE layer. To this end, we propose DAG-MoE, a sparse MoE framework that employs a lightweight module to automatically learn the optimal aggregation structure among the selected experts. We evaluate DAG-MoE under standard language modeling settings. Extensive experiments show that DAG-MoE consistently improves performance in both pretraining and fine-tuning, surpassing traditional MoE baselines.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
专家输出的结构化聚合扩展了专家组合空间，超越简单加权求和。

### 2. 核心内容
专家混合模型已成为解耦参数量与计算成本的主流方案，但细粒度专家带来路由开销与扩展瓶颈。该文转而探索专家输出混合这一新维度，先分析传统加权求和聚合的局限，再理论证明引入结构化聚合能扩展专家组合空间并提升灵活性。基于此提出DAG-MoE，用结构化聚合替代简单加权求和。其贡献在于为专家路由与聚合机制的设计提供了可迁移的结构化改进思路。

### 3. 对应检索需求
sample-level and drug-pair-level dynamic expert routing。

### 4. 来源与原文
- Source：ICLR-2026-Rejected-Public
- OpenReview：[https://openreview.net/forum?id=gdCdukkxKP](https://openreview.net/forum?id=gdCdukkxKP)
