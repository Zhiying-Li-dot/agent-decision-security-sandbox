# Optima-Bench（工程底座）

> 首个面向电商**卖家侧**大模型智能体的**行为**评测基准。本课题的工程底座与决策安全沙箱原型。

## 是什么

Optima-Bench 评估 AI Agent **操作**工具的能力（调对工具、按对顺序、传对参数），而非回答问题的能力。评分基于**工具调用序列 + 状态变更**，模型无关（任何 OpenAI / Anthropic 兼容端点或自研 Agent Runtime 均可评测）。

## 关键规模与能力

- **581 条用例 / 31 技能域 / 243 条工具命令 / 16 个 Mock CLI**：覆盖商品、订单、库存、广告、BI、Shopify、物流、社媒研究、KOL 外联、浏览器自动化等。
- **拦截式 Mock 执行器**：智能体在 bash 里调用 CLI → Mock Handler 拦截、更新内存状态、返回 JSON 并记录 `call_trace` → 评估器对比 trace 与最终状态 vs **golden state**。
- **6 维诊断指标**：Skill Routing F1 / Command Correctness / State Outcome / Progress Rate / Efficiency / Checklist。
- **用户视角主指标**：Task Success Rate（raw/effective）、pass^k 可靠性、**Harmlessness（安全性）**。
- **3 个难度等级**：L1（单步）/ L2（多步推理）/ L3（复合工作流）。
- 已完成多款主流大模型基线评测；配 93 项单测；MIT 协议，自有开源成果。

## 为什么是本课题的原型

Optima-Bench 的拦截式 Mock 执行器，本质上**就是一个在工具调用前拦截、评估并控制是否落地的沙箱**：

| Optima-Bench（评测） | 决策安全沙箱（防御） |
|---|---|
| 拦截工具调用 → 更新 Mock 状态 | 拦截工具调用 → 研判是否放行 |
| 对比 golden-state 评分 | [影子执行](decision-security-sandbox.md)预测危害 |
| Harmlessness 指标 | [风险体系](agent-decision-risk-taxonomy.md)分级 |
| `call_trace` 行为序列 | 态势感知特征 |

因此本课题从 Optima-Bench 改造，而非从零搭建——显著降低研发风险、缩短周期。

## 来源
- 仓库事实见 [来源页](../sources/2026-05-30-optima-bench.md)。
