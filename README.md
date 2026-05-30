# 智能体应用态势、风险体系与决策安全沙箱

> 研究知识库 · **Agent Situation · Risk Taxonomy · Decision Security Sandbox**

把智能体（Agent）安全做成"**宏观治理 + 微观保障**"的一体化能力。智能体在大模型"生成内容"之上进一步具备"**行为能力**"——可自主调用工具、操作真实系统，风险更多、威胁更大；而传统软件测试与静态分析已无法应对其在开放环境中自主决策带来的不可预测风险。

## 三位一体（三条研究线 ↔ 三份交付报告）

| 研究线 | 做什么 | 交付 |
|---|---|---|
| **① 应用态势研判** | 跟踪国内外智能体技术应用发展态势，建重点应用清单与暴露面 | 报告②：应用发展分析 |
| **② 风险分类分级** | 按内生风险 / 外部攻击 / 应用衍生风险，分类分级建风险体系框架 | 报告③：风险分类分级 |
| **③ 决策安全沙箱** | 多层次沙箱 + "感知—规划—决策—执行"全链路可解释监控、风险溯源、影子执行、主动干预、人机混合决策回路动态测评 | 报告①：沙箱关键技术 |

核心范式：**"仿真推演 — 风险评估 — 主动免疫"一体化**，替代传统静态分析；对高危不可逆决策先**影子执行**预测危害，再**主动干预**。

## 工程底座

以已开源的行为评测基准 **[Optima-Bench](wiki/entities/optima-bench.md)** 为底座：其拦截式 Mock 执行器即"沙箱 / 影子执行"原型，行为轨迹支撑全链路可解释监控，pass^k 与 6 维指标支撑人机混合决策回路的**动态测评**——把"事后行为测评"升级为"运行时仿真—评估—干预"。

## 导航

- **总览**：[三位一体总览](wiki/overview/decision-security-sandbox.md)
- **三条研究线**
  - [① 智能体应用态势研判](wiki/entities/agent-application-situation.md)
  - [② 决策风险分类分级体系](wiki/entities/agent-decision-risk-taxonomy.md)
  - [③ 决策安全沙箱机制](wiki/entities/decision-security-sandbox.md)
- **工程底座**：[Optima-Bench](wiki/entities/optima-bench.md)
- **分析**：[研究计划与考核指标（12 个月 / 三份报告）](wiki/analyses/2026-05-30-research-plan-and-kpis.md)
- **来源**：[长安 #25 任务选题](wiki/sources/2026-05-30-changan-task-25.md) · [Optima-Bench](wiki/sources/2026-05-30-optima-bench.md)
- **维护**：[AGENTS.md](AGENTS.md) · [索引](index.md) · [变更日志](log.md)

## 说明

研究性知识库，仅含技术内容，**不含任何个人隐私信息，也不含课题设置企业的私有材料（联系人、任务书原文等）**。相关研究支撑 2026 年"网络安全学院学生创新资助计划"四期长安通信 #25 选题。

作者：Zhiying Li（李志颖）· © 2026 · 仅供学术交流
