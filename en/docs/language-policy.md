# Language policy and terminology

## One policy, two languages

The repository root contains the authoritative Chinese documentation; `en/` retains an English reference expressing the same rules. English is not independently calibrated and grants no additional authority. Project deliverables may use the language appropriate to that project.

Keep filenames, configuration keys, IDs, status values, and CSV headers in English. Translate headings, explanations, comments, template prompts, and free-text policy values, not machine identifiers. Keep stage IDs such as `Step 1` and the term `token`.

`../../translation-manifest.json` pairs relative paths and records SHA-256 hashes. Update both versions together when rules change, check semantic consistency, and refresh hashes. Hashes detect file changes; they do not prove equivalent meaning. If synchronization is incomplete, mark the English reference stale and identify the corresponding Chinese version. Resolve translation ambiguity against Chinese; substantive policy changes still require a human decision.

## Terms

| Chinese | English / stable identifier |
| --- | --- |
| 智能体 | agent |
| 协调者 | coordinator |
| 研究者／产出者 | researcher / producer |
| 独立核验者 | verifier |
| 质疑者 | challenger |
| 方法专家 | methods_specialist |
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

Keep `pass`, `fail`, `not_verifiable`, `pending`, `draft`, `calibrated`, `pending_calibration`, and `proposed_not_authorized` unchanged. A human-authorized exception is not a `pass`. Distinguish estimated, measured, and unavailable resource usage.

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

## Synchronization scope

Documentation, Steps 1–4, calibration records, configuration, and templates have Chinese primary and English reference versions. Stale stage-status prose and duplicated wording were corrected. Step 5 is still pending. Configuration keys, IDs, status values, proposed numeric defaults, approval/budget boundaries, and evidence-reuse rules are unchanged.
