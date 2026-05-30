# AGENTS.md — 知识库维护手册

## 仓库目标

围绕"**面向专业域大模型智能体的决策安全沙箱**"这一研究方向，沉淀可长期复用的研究目标、技术路线、风险体系、关键概念与实施计划。读者既包括人类，也包括协助维护本库的 AI agent。

## `raw/` 的 source-of-truth 规则

- `raw/` 存放**原始素材的忠实副本**（研究内容原文、来源摘录），是事实的唯一来源。
- wiki 页面是对 `raw/` 的**结构化重组与提炼**，不得与 `raw/` 冲突；冲突时以 `raw/` 为准并在 wiki 标注。
- **禁止**把任何个人隐私信息（身份证号、电话、邮箱、住址、承诺书原文等）写入本库任何位置——本库为公开仓库。

## 页面类型及其职责

| 目录 | 职责 | 命名 |
|---|---|---|
| `wiki/overview/` | 一个主题 / 认知领域一页（大图景） | `kebab-topic.md` |
| `wiki/entities/` | 跨多页反复出现的稳定概念 / 实体一页 | `kebab-entity.md` |
| `wiki/analyses/` | 长期有效的答案、比较、综合、决策记录 | `YYYY-MM-DD-kebab.md` |
| `wiki/sources/` | 每个来源一页 | `YYYY-MM-DD-kebab.md` |

## 工作流

- **ingest（收录）**：新素材忠实存入 `raw/` → 建/更新对应 `sources/` 页 → 把稳定概念抽到 `entities/` → 必要时在 `overview/` 或 `analyses/` 综合 → 更新 `index.md` 与 `log.md`。
- **query（查询）**：先看 `index.md` 与 `overview/` 定位，再下钻 `entities/` / `analyses/`，必要时回溯 `sources/` 与 `raw/`。
- **lint（巡检）**：检查死链、孤页、与 `raw/` 的冲突、是否误入隐私信息、命名是否合规。

## 编辑规则

- 一处事实只在一个权威页维护，其他页用链接引用，避免复制粘贴漂移。
- 用相对链接互联（GitHub 可渲染），如 `[风险体系](wiki/entities/agent-decision-risk-taxonomy.md)`。
- 修改后必须更新 `log.md`，并在提交信息中说明改动。

## 何时新建页 vs 扩写旧页

- 出现一个**跨多页反复引用的稳定概念** → 新建 entity 页。
- 产生一个**长期有效的结论 / 计划 / 比较** → 新建 analysis 页。
- 只是给已有概念补细节 → 扩写旧页，不要新建。

## agent 修改后的输出要求

每次维护结束，简述：改了哪些页、为什么、是否新增/删除页、是否更新 `index.md` 与 `log.md`。
