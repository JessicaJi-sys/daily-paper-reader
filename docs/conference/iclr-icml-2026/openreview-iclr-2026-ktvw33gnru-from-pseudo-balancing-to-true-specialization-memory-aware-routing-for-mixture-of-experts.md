---
title: "From Pseudo-Balancing to True Specialization: Memory-Aware Routing for Mixture-of-Experts"
title_zh: 从伪均衡到真正专门化：混合专家的记忆感知路由
authors: "Peixuan Hou, Yunbo Hou, Bin Chen, LI He, Liang Wang, Jian Xu, Weiping Li, Bo Zheng, Guojie Song"
date: 2025-09-19
pdf: "https://openreview.net/pdf?id=KTVW33GNRU"
tags: ["query:ddi-moe"]
score: 6.0
evidence: 记忆感知路由促进真正的专家专门化
tldr: 针对MoE中专家负载均衡策略导致的伪均衡问题，即同一输入在不同训练步被随机路由而非匹配最优专家，本文提出记忆感知路由方法。该方法缓解了专家间知识重叠与冗余表示，促进token与专家的语义对齐。研究推动MoE从形式均衡走向真正的专家专门化，提升模型效率与表现。
source: ICLR-2026-Public
selection_source: conference_retrieval
motivation: 负载均衡策略导致伪均衡与专家知识重叠。
method: 提出记忆感知路由以实现token与专家的语义对齐。
result: 缓解专家冗余并促进真正的专家专门化。
conclusion: 为MoE路由从伪均衡走向真专门化提供方案。
---

## Abstract
Mixture-of-Experts(MoE) efficiently trains large models by using sparse activation to lower costs, selecting a few experts based on data characteristics. For MoE, an unbalanced expert load will lead to routing collapse or increased computational overhead. Existing methods commonly achieve an expert-centered balancing strategy to solve it, prioritizing equal utilization of experts over semantic alignment between tokens and experts.
However, this can lead to a pseudo-balance phenomenon: To ensure expert load balancing, the same input is randomly routed to different experts across training steps instead of the most matching one. It introduces two critical issues: (1) Severe knowledge overlap among experts, resulting in redundant representations and inefficient parameter utilization. (2) Difficulty in forming and stabilizing expert specialization. These issues limit the scalability of models, especially large language models(LLM). 
To address these limitations, we introduce Memory-Aware Routing (MAR), a training-phase approach that enhances existing load-balancing strategies. By equipping each expert with a memory buffer, our method explicitly models their long-term preferences, allowing historical experience to guide routing. This ensures that tokens are routed more consistently to compatible experts, mitigating the pseudo-balance problem while maintaining global load balance and fostering expert specialization.
Experimental results show that Memory-Aware Routing improves expert specialization by 35\% and downstream accuracy by 2\%-25\%, doubles parameter efficiency, and matches baseline performance with only half the experts (one-quarter of the parameters).

---

## 论文详细总结（自动生成）

### 1. 检索相关性
记忆感知路由促进真正的专家专门化。

### 2. 核心内容
针对MoE中专家负载均衡策略导致的伪均衡问题，即同一输入在不同训练步被随机路由而非匹配最优专家，本文提出记忆感知路由方法。该方法缓解了专家间知识重叠与冗余表示，促进token与专家的语义对齐。研究推动MoE从形式均衡走向真正的专家专门化，提升模型效率与表现。

### 3. 对应检索需求
How can mixture of experts models learn specialized knowledge integration strategies for different latent distribution regimes without manually defining expert semantics?

### 4. 来源与原文
- Source：ICLR-2026-Public
- OpenReview：[https://openreview.net/forum?id=KTVW33GNRU](https://openreview.net/forum?id=KTVW33GNRU)
