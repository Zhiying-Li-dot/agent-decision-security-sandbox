# 面向专业域大模型智能体的决策安全沙箱

> 研究知识库 · **Decision Security Sandbox for Professional-Domain LLM Agents**
> 态势感知（Situational Awareness）· 风险体系（Risk Taxonomy）· 运行时拦截（Runtime Interception）

把大模型智能体（LLM Agent）的安全防护，从"模型对齐层"下沉到"**决策—执行层**"。

当智能体从"对话问答"走向"自主调用工具操作真实业务系统"，真正的危害不再是它"说错话"，而是它**真的执行了**越权访问、不可逆破坏（批量删商品 / 误改价）、数据泄露、经济损失（错误下单 / 广告超投），或在提示注入 / 工具投毒下发生目标漂移。现有智能体安全研究多停留在让模型"拒答"的内容护栏层，缺乏面向"工具操作决策"这一真正危害发生环节的**运行时安全机制**与配套的态势感知、风险刻画体系。

## 核心思路

> **风险体系（静态） × 态势感知（动态） × 影子执行（预测） = 决策安全沙箱**

以已开源的行为评测基准 **Optima-Bench** 的"拦截式 Mock 执行器"为工程原型，将其从"事后评测"升级为"运行时防御"——在工具调用真正落地前对高危决策做安全研判与拦截 / 降级，并对不可逆决策先做影子执行预演危害。

## 导航

- **总览**：[决策安全沙箱总览](wiki/overview/decision-security-sandbox.md)
- **关键概念**
  - [决策风险体系（六类风险）](wiki/entities/agent-decision-risk-taxonomy.md)
  - [决策安全沙箱机制](wiki/entities/decision-security-sandbox.md)
  - [Optima-Bench（工程底座）](wiki/entities/optima-bench.md)
- **分析**：[研究计划与考核指标（12 个月）](wiki/analyses/2026-05-30-research-plan-and-kpis.md)
- **来源**：[长安 #25 任务选题](wiki/sources/2026-05-30-changan-task-25.md) · [Optima-Bench](wiki/sources/2026-05-30-optima-bench.md)
- **维护手册**：[AGENTS.md](AGENTS.md) · [索引](index.md) · [变更日志](log.md)

## 说明

本仓库是**研究性知识库**，仅含技术内容（研究目标、技术路线、风险体系、实施计划），**不含任何个人隐私信息**。相关研究支撑 2026 年"网络安全学院学生创新资助计划"四期长安通信 #25 选题的研究方案。

作者：Zhiying Li（李志颖）· © 2026 · 仅供学术交流
