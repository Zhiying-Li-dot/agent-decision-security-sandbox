# 来源：Optima-Bench 开源仓库

- **类型**：开源代码仓库 / 行为评测基准
- **协议**：MIT
- **收录日期**：2026-05-30
- **定位**：首个面向电商卖家侧大模型智能体的行为评测基准；本课题工程底座。

## 仓库事实摘录

- **规模**：581 条测试用例 / 31 个技能域 / 243 条工具命令 / 16 个 Mock CLI。
- **评测对象**：模型无关——OpenAI / Anthropic 兼容端点或自研 Agent Runtime 均可。
- **工作原理**：指令 → Agent → bash 调 CLI → Mock Handler 拦截、更新内存状态、返回 JSON 并记 `call_trace` → 评估器对比 trace + 最终状态 vs golden state → 输出双轨报告。
- **诊断指标（M1–M6）**：Skill Routing F1 / Command Correctness（AST）/ State Outcome / Progress Rate / Efficiency / Checklist（LLM Judge）。
- **主指标**：Task Success Rate（raw / effective）/ Attempt Rate / pass^k / **Harmlessness Rate**。
- **难度**：L1 单步 / L2 多步推理 / L3 复合工作流。
- **工程**：93 项单测；支持断点续跑、多 trial（pass^k）、LLM Judge。

## 为什么用 Mock 而非真实店铺

状态变更*就是*标准答案——与业界一致（SWE-bench 用 Docker 仓库，WebArena 用 Docker 网站）。这也使其拦截式执行器天然适合改造为[决策安全沙箱](../entities/decision-security-sandbox.md)的影子执行环境。

## 实体页
- [Optima-Bench（工程底座）](../entities/optima-bench.md)
