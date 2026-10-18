# AI 量化个股诊断 MVP — SDD 项目档案

> **本仓库为 [ai-stock-diagnosis](https://github.com/jiayuanandhong-sys/ai-stock-diagnosis)（产品源码）的 SDD（Spec-Driven Development，规格驱动开发）完整项目档案**；Evals 工程见 [ai-stock-diagnosis-evals](https://github.com/jiayuanandhong-sys/ai-stock-diagnosis-evals)。本档案亦作为子目录 `sdd-stock-diagnosis/` 随主仓库同步分发。

按 **SDD 五阶段方法论**（Spec → Plan → Tasks → Implement → Verify）全程留痕开发该产品的全部活文档与验证证据：

| 文档 | 阶段 | 内容 |
|---|---|---|
| `spec.md` | ① Spec | 需求规格：3 REQ / 9 BR / 11 AC / 附表 A（18 项因子清单冻结版）/ CR 变更台账 |
| `plan.md` | ② Plan | 技术方案：12 项技术问题地图 + 4 个 ADR（架构决策记录）+ Spike 结论 |
| `tasks.md` | ③ Tasks | 任务分解：T-01~T-10 + 每任务 DoD + AC 覆盖矩阵 |
| `交付清单_Implement阶段.md` | ④ Implement | 实施阶段交付清单与遗留披露 |
| `GateV验收报告.md` | ⑤ Verify | 最终验收：AC-001~011 逐项独立实测记录（11/11 通过） |
| `spikes/` | ② Plan 前置 | 技术验证探针：spike1 数据可行性（新浪/东财/百度估值源实测 20/20）、spike2 报告渲染管线演示（图表 PNG + docx/HTML 演示报告） |
| `开发流程约定_SKILL.md` | 全程 | 开发纪律约定（环境锁定、依赖管理、验收证据规范） |

## 阅读顺序建议

1. `spec.md` —— 先看需求边界与验收标准（附表 A 是 18 因子口径的唯一权威定义）
2. `plan.md` —— 技术选型与 ADR（含"为什么不用数据库/为什么服务端渲染"等决策）
3. `tasks.md` —— 任务如何拆解、DoD 如何定义
4. `GateV验收报告.md` —— 最终如何逐条独立验证（对拍数据见主仓库 `evidence/` 目录）
5. `spikes/` —— 关键技术风险如何在开工前用最小成本证伪/证实

## 相关仓库

| 仓库 | 内容 |
|---|---|
| [ai-stock-diagnosis](https://github.com/jiayuanandhong-sys/ai-stock-diagnosis) | 产品源码（FastAPI + 18 因子引擎）+ 本档案 + evidence 验收证据链 |
| [ai-stock-diagnosis-evals](https://github.com/jiayuanandhong-sys/ai-stock-diagnosis-evals) | Evals 工程（PEG 检查器 / 41 案例合成 Golden Dataset / 五状态 Runner） |

## 已知限制

- `GateV验收报告.md` 与 `交付清单` 中引用的 `evidence/` 验收证据（T-01~T-10 运行日志与记录）位于主仓库，本档案不重复携带。
- `spikes/spike2/out/` 下的演示报告与图表为 Spike 阶段产物（数据截至 2026-06），与正式产品报告口径不完全一致，仅作技术验证留痕。
- 文档中的运行环境路径（Python venv 等）为开发机环境备忘，跨机器请以主仓库 README 的通用方式为准。
