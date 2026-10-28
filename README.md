# 研究工作流

用于研究与学习项目的可复用多智能体工作流：固定阶段目标、独立核验、质量门槛，以及受预算约束的修正和前序阶段复查。

**版本：v0.7；Step 1–6 已校准，具体项目规则仍须批准。** 本次新增已批准的 Step 6 规则，保持中英文同步。仓库提供说明和模板，不是可执行的编排服务或实时资源监控器。

## 语言与版本

主目录为中文权威版本；[英文参考版](en/README.md)保留同一套规则。文件名、配置键、ID 和状态值保持英文。英文版不独立修改规则；同步关系见 [语言政策与术语](docs/language-policy.md) 和 `translation-manifest.json`。工作流说明语言不限制项目产出的语言。

## 开始新项目

在 GitHub 点击 **Use this template** 创建新项目仓库，再在智能体环境中打开该项目。项目成果保存在新仓库，避免与通用模板混杂。

启动提示词：

> 按本仓库 AGENTS.md 和 research-workflow.yaml 初始化研究项目。主题是 [主题]，目标产出是 [产出]，截止时间是 [日期]。先读取已有材料，再按 templates/project-brief.md 一次问一个尚未回答的选择题，记录答案并起草阶段契约。环境支持时使用独立的产出者与核验者。初始契约获批前，不开展实质研究。

已有项目可复制 `research-workflow.yaml`、`docs/` 和 `templates/`，并将 AGENTS.md 的相关规则合并到已有指令中，不覆盖项目原有指令。也可把仓库链接交给智能体并明确要求读取；链接本身不会自动加载或执行流程。英文项目可使用 `en/` 下的对应参考文件。

## 角色

| 角色 | 责任 | 存在理由 |
| --- | --- | --- |
| 协调者（Coordinator） | 契约、分工、依赖、预算及阶段转换 | 保持工作一致，限制无效循环 |
| 研究者／产出者（Researcher / Producer） | 证据、分析、交付物、自查和修正 | 负责实质产出 |
| 独立核验者（Verifier） | 按固定标准独立核查 | 将产出与验收分离 |
| 质疑者（Challenger） | 检查假设、反例和竞争解释 | 发现清单以外的概念问题 |
| 方法专家（Methods specialist） | 领域、统计、数学或计算方法 | 按需提供技术深度 |

详细责任、原则和反应见 [配置](research-workflow.yaml)。

## 阶段与规则

1. [Step 1：定义并选择研究问题](docs/step-1.md)：不同输入进入同一流程的不同阶段。
2. [Step 2：方法比较与协议定稿](docs/step-2.md)：形成可进入实施的协议。
3. [Step 3：实施准备与小规模端到端验证](docs/step-3.md)：复用有效证据，只验证新增或失效部分。
4. [Step 4：正式执行与预先规定的分析](docs/step-4.md)：分层复核结果及解释边界。
5. [Step 5：研究综合与交付定稿](docs/step-5.md)：按项目综合与交付，分级处理问题，定稿不自动授权发布。
6. [Step 6：必要交付、归档与收尾](docs/step-6.md)：满足接收方要求，按获批标准收尾，可选后续不阻碍完成。

每阶段采用产出 → 自查 → 独立核验 → 诊断 → 修正 → 复核的有界循环。决策就绪、科学证据核验与人类授权分别记录。严谨的负面或不确定结果也可能满足研究目标；批准继续不会将未决问题变为已通过。

达到资源或停滞触发条件时，区分执行问题、前序假设缺陷和工作量低估；只提出必要的前序修正，保留版本并重验受影响部分。不因预算不足降低标准，不因换阶段重复有效测试。

初始的三轮修正、连续两轮无进展、80% 预算检查点仍只是提案。具体限额和规则须按项目批准。

## 文件与模板

- `research-workflow.yaml`：结构化角色和阶段政策索引。
- `AGENTS.md`：智能体操作指令。
- [校准记录](docs/calibration-decisions.md)：已批准设计决定与待定项。
- [项目说明](templates/project-brief.md)、[阶段契约](templates/stage-contract.yaml)、[核验报告](templates/verification-report.md)、[前序复查](templates/upstream-review.md)、[决策记录](templates/decision-log.md)。
- [方法比较](templates/method-comparison.md)、[有限测试](templates/pilot-check.md)、[研究协议](templates/research-protocol.md)。
- [Step 3 计划](templates/step-3-plan.yaml)及[验证记录](templates/step-3-report.md)。
- [Step 4 计划](templates/step-4-plan.yaml)及[结果包](templates/step-4-results.md)。
- `templates/evidence-ledger.csv`：稳定英文列名的证据台账；字段含义见语言政策。

每个项目从模板建立 `project/brief.md`、`project/stages/`、`project/reviews/`、`project/artifacts/` 和 `project/decisions.md`，记录采用的模板提交版本。Step 1–6 规则已校准，项目预算仍须批准；具体交付与收尾标准按项目批准。

使用 [Step 5 计划](templates/step-5-plan.yaml) 和 [交付包](templates/step-5-delivery.md)。Step 4 核验结果，Step 5 审查新增综合与表述；有效证据直接复用。

使用 [Step 6 计划](templates/step-6-plan.yaml) 和 [交接包](templates/step-6-handoff.md)。实际提交必须明确授权准确版本与动作；准备、授权、提交、接收确认、收尾和维护启动分别记录。

各阶段同时遵循[共享控制](docs/shared-controls.md)，使用授权记录、统一检查记录、任务启动和角色分工模板。已有授权仅在记录的边界内复用，人类保留决策权。
