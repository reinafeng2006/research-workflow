# Language policy and terminology

## One policy, two languages

The repository root contains the authoritative Chinese documentation; `en/` retains an English reference expressing the same rules. English is not independently calibrated and grants no additional authority. Project deliverables may use the language appropriate to that project.

Keep filenames, configuration keys, IDs, status values, and CSV headers in English. Translate headings, explanations, comments, template prompts, and free-text policy values, not machine identifiers. Keep stage IDs such as `Step 1` and the term `token`.

`../../translation-manifest.json` pairs relative paths and records SHA-256 hashes. Update both versions together when rules change, check semantic consistency, and refresh hashes. Hashes detect file changes; they do not prove equivalent meaning. If synchronization is incomplete, mark the English reference stale and identify the corresponding Chinese version. Resolve translation ambiguity against Chinese; substantive policy changes still require a human decision.

## Terms

| Chinese | English / stable identifier |
| --- | --- |
| 用户 | user: the person talking with the agent who keeps decision authority. In a single-person project the user is the principal; the two are the same |
| principal | principal: the final decision-maker. In team projects the user may name other approvers, but non-delegable decisions remain the principal's; see docs/teamwork.md |
| 批准人 | approver: a person who approves within the gate classes and scope the principal explicitly delegated |
| 任务单元 | work unit: the smallest unit of assignment, with one owner and mutually exclusive writable artifacts |
| 档位 | profile: `lite` / `standard` / `strict`, trimming the breadth of G1/G2 checklist items |
| 三类门槛 | G1 材料就绪 material ready / G2 独立核验完成 independently verified / G3 人类授权 human authorization |
| 运行期条件 | runtime condition: whether authorized work may continue, not judged at stage end |
| 智能体 | agent |
| 协调者 | coordinator |
| 研究者／产出者 | researcher / producer |
| 独立核验者 | verifier |
| 质疑者 | challenger |
| 方法专家 | methods_specialist: from v0.9.4 one kind of project specialist |
| 项目专长 | project specialist: configured per project and per stage, derived by the AI and approved by the user |
| 固定职能 | fixed function: coordinator, producer, independent verifier, challenger; the same in every project |
| 阶段契约 | stage contract |
| 协议定稿就绪 | protocol ready for implementation |
| 决策材料就绪 | decision readiness |
| 核验 | verification of evidence/artifacts against agreed criteria |
| 验证 | validation for a stated purpose; not automatic proof of a scientific conclusion |
| 有限测试 | pilot check / bounded test |
| 决策关键主张 | decision-critical claim |
| 有效证据复用 | valid evidence reuse |
| 取舍 | tradeoffs |
| 预批准备用方案 | preapproved fallback |
| 暂停／恢复 | pause / recovery |

Keep `pass`, `fail`, `not_verifiable`, `pending`, `draft`, `calibrated`, `pending_calibration`, and `proposed_not_authorized` unchanged. Gate identifiers `G1`, `G2`, `G3`, `runtime` and tier values `lite`, `standard`, `strict` are kept as they are and not translated. A human-authorized exception is not a `pass`. Distinguish estimated, measured, and unavailable resource usage.

## Evidence ledger fields

| Fields | Meaning |
| --- | --- |
| claim_id / claim | Claim identifier and text |
| source_title / source_url_or_path / source_version | Source title, address/path, and version |
| location_in_source / date_inspected | Precise source locator and actual inspection date |
| evidence_level / evidence_summary | Evidence level and summary |
| assumptions / limitations | Assumptions and limitations |
| decision_critical / decision_impact | Criticality and consequence for the decision |
| human_requested_verification | Whether the human requested verification |
| verification_status / missing_support | Verification status and missing support |
| alternatives / permitted_use | Alternatives and permitted uses |
| dependent_artifacts | Artifacts depending on the claim |

## Current synchronization scope

v0.9.6 provides the Chinese primary version and English reference for Steps 1–6, including docs, diagrams, configuration, templates and calibration records. From v0.9, gates are unified into three kinds with checklist items trimmed by tier, and the people and work-assignment layer, the division of labor, Step 1 divergence and appraisal, agent roles and project specialists, and the roundtable rules are added; stage documents are slimmed to stage-specific content, and runtime controls move to Shared controls section 7; v0.9.6 aligns every template to the same version. Configuration keys, IDs, status values, gate identifiers and tier values stay in English; project budgets and authority still require approval.
