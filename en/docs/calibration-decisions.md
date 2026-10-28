# Calibration record — 2026-10-27

These decisions were explicitly calibrated with the human. The detailed Step 1 specification is [step-1.md](step-1.md); the configuration indexes it. This record is design history, not approval for a particular research run.

| ID | Agreed decision |
| --- | --- |
| S1-01 | Support multiple starting stages; B enters goal clarification, C candidate refinement/comparison, A feasibility assessment preparation. Revisit earlier phases only for missing prerequisites or requested changes. |
| S1-02 | Goals are project-specific, more detailed than generic labels, and may coexist without ranking. Ask priorities only when a concrete decision needs them. |
| S1-03 | Suggest additional outcomes with reasons, but keep them optional until human acceptance. Track accepted, proposed, rejected, and deferred outcomes separately. |
| S1-04 | Conduct a bounded preliminary check of plausibility and value; explain uncertainty, alternatives, and tradeoffs. Human decides whether to proceed. |
| S1-05 | Agents propose a complexity-based budget and explain expected resolution before investigation. Human approval is required. |
| S1-06 | Budget combines time, tokens, and investigation scope. Separate estimates, measured actual usage, and unavailable telemetry. |
| S1-07 | If the budget is insufficient, explain unresolved work and options before any extension; no silent expansion. |
| S1-08 | Existing-research and data-availability claims need direct inspected sources. Methodological feasibility may include labeled inference with assumptions, uncertainty, and verification needs. |
| S1-09 | Abstract findings may orient the project but must be labeled. Decision-critical research claims need full-text verification. Unavailable full text requires uncertainty/alternative disclosure and human decision. |
| S1-10 | Flag claims whose change could alter the recommendation, explain their importance, and let the human add verification targets. |
| S1-11 | Recommend a path with alternatives and tradeoffs; disclose assumptions and uncertainty. Final choice belongs to the human. |
| S1-12 | Present unresolved disagreements with each position's evidence, assumptions, and recommendation impact. Human chooses whether to proceed or investigate further. Consensus is not mandatory. |
| S1-13 | Combined approval may authorize the next stage only if scope, budget, and expected outcomes are explicit. Otherwise ask separately. Direction approval is not unlimited permission. |
| S1-14 | Brainstorm both close and unconventional directions tied to accepted goals. Do not automatically expand scope. |
| S1-15 | Propose and justify a useful range of distinct directions within budget for human approval. No fixed number or redundant filler. |
| S1-16 | Human selects one or multiple directions before feasibility investigation. Mark initial feasibility as not assessed. |
| S1-17 | Assess selected options individually first. Suggest combinations with added value, complexity, and tradeoffs; obtain approval before scope expansion. |
| S1-18 | Step 1 ends with a human-approved specific research question. Detailed methodology belongs to Step 2. |
| S1-19 | Calibrate interactively, one question at a time. |

## Literature-workflow review: reference, not wholesale adoption

Reviewed the user's [literature workflow](https://github.com/reinafeng2006/Mechanism-Aware-Statistical-Arbitrage/tree/d0d6f19d439efe573d1c0b5f94ded790c3ede9d9/literature) as process evidence, not as authority over this project or verification of its papers.

Suggested reusable practices: decision-driven depth, claim provenance, reasoning labels, permitted-use boundaries, contradiction/dependency tracking, and bounded stopping/reopening. Suggested improvements: one authoritative current state, separate readiness/access/approval statuses, generic validators rather than fixed historical counts, more precise source locators, and stage-appropriate evidence detail. These are recommendations pending detailed literature/methodology calibration, except the abstract/full-text and criticality policies explicitly accepted above. Do not import domain-specific claims, statuses, or historical approval rules.

## Still open

Step 5 and subsequent stage structure; project-specific budgets and numerical revision/checkpoint values. Publishing this policy does not authorize a new investigation.

## Step 2 — approved calibration

The human approved the complete [Step 2 workflow](step-2.md) and its publication. This approves reusable policy, not a project run.

| ID | Agreed decision |
| --- | --- |
| S2-01 | Compare several approaches with a recommendation, assumptions, feasibility, and tradeoffs; human shortlists one or more before detailed design. |
| S2-02 | Explain what each approach can/cannot establish and the assumptions needed for each conclusion. |
| S2-03 | Propose small pilot checks when useful; specify uncertainty resolved, scope, budget, and limits; obtain approval before running. |
| S2-04 | Predefine positive, negative, and inconclusive meanings and recommendation consequences; human decides next steps. |
| S2-05 | Test shortlisted approaches independently and only on a small scale first; combinations require value/complexity/tradeoff explanation and approval before expansion. |
| S2-06 | Compare test results and recommend; human selects and approves detailed-design scope and budget before it starts. |
| S2-07 | Deliver an execution-ready protocol with data, procedures, assumption checks, evaluation and stopping rules; human approves before implementation. |
| S2-08 | Material unresolved choices block execution-ready status. Minor choices need explicit boundaries and human-approved classification. |
| S2-09 | If pilots undermine answerability, pause and propose targeted Step 1 return with evidence, failed assumptions, revisions, and tradeoffs; human approves changes. |
| S2-10 | Approve shared criteria and method-specific checks before tests; explain fit and comparability limits. |
| S2-11 | Preserve original criteria/results; explain amendments and interpretation effects; approve before application or additional testing; disclose post-result changes. |
| S2-12 | Separate verifier checks completeness/reproducibility; challenger checks support for conclusions; present unresolved concerns and dissent for human decision. |
| S2-13 | Approve project-specific pilot-reuse and independent-validation safeguards before finalizing them. |
| S2-14 | Approve fallback, pause, and upstream-review triggers and consequences. Log preapproved fallback use for next checkpoint; notify unexpected consequences immediately and pause before exceeding scope/budget. |
| S2-15 | Agents propose justified major milestones plus budget/progress checkpoints; human approves before starting. |
| S2-16 | Diagnose and repair stagnation within authority while informing human; agents propose repair rounds, time/token limits and observable progress criteria for approval; any stop condition pauses work for analysis/options. |
| S2-17 | Present decision summary first, then full traceable executable protocol. Include recommendation, assumptions, risk, unresolved choices and approval items. |
| S2-18 | Require document review, independent desktop walkthrough, and a separately proposed and approved minimal technical trial. |
| S2-19 | Recheck modified parts and dependencies; core-method/conclusion-boundary changes trigger whole review; new trials or budget expansion need approval. |
| S2-20 | If all candidates fail, diagnose methods/data/test insufficiency/answerability and offer options; human decides, no automatic standard reduction. |
| S2-21 | Minor issues may accompany submission only with impact, allowed bounds, owner and resolution time for approval; core-result or uncertain-impact risks are not automatically minor. |
| S2-22 | Continue calibration with one multiple-choice question at a time. |

## Step 3 — approved calibration and Step 2 boundary amendment

The human approved publication of [Step 3](step-3.md), both diagrams, and the boundary clarification in [Step 2](step-2.md). This supersedes generic earlier wording implying full implementation validation in Step 2. The policy is not authorization for a particular run.

| ID | Agreed decision |
| --- | --- |
| S3-01 | Step 3 prepares implementation and performs approved small-scale end-to-end validation; results go to human before formal execution. |
| S3-02 | Propose mixed synthetic/real materials, limits and reuse risks with scope/budget/pass criteria; never silently use reserved final-validation data. |
| S3-03 | Implementer self-check plus independent verifier maps protocol → implementation/operations → evidence; notify result-impacting issues, never silently amend protocol. |
| S3-04 | Default separate stages: Step 2 design decisions/protocol, Step 3 implementation/integration. Reuse valid evidence and pilot outputs, only recheck affected parts. |
| S3-05 | Step 2 approval may explicitly include Step 3 scope, budget and pass criteria if the human agrees. Stage transition alone never requires duplicate testing. |
| S3-06 | Evidence invalidation requires cause/impact record; minimally recheck only if explicitly authorized within budget, otherwise seek approval. |
| S3-07 | Clear implementation defects may be repaired within approved scope/budget with records. Protocol ambiguity or method/conclusion change pauses affected work for human decision. |
| S3-08 | Cover normal and decision-critical exceptional paths with approved rationale/budget/criteria; no exhaustive or redundant testing. |
| S3-09 | Project-specific reproducibility: deterministic consistency; approved stochastic/manual tolerances, repetition and records; reuse valid checks. |
| S3-10 | Recommend formal execution with scope, scale, budget, checkpoints, stop rules and unresolved issues; wait for approval after results. |
| S3-11 | Inherit Step 2 bounded repairs/fallback mechanism, but approve Step 3-specific limits and triggers; any stop condition pauses. |
| S3-12 | Representative-first batches with effective-progress checks; approved next batches continue normally; no output, repeated failure, abnormal costs or limits pause immediately. Logs/process survival are not progress. |
| S3-13 | Tiered rate monitoring: ordinary anomaly warns; sustained overspeed with poor progress, forecast overrun or hard-rate limit pauses. Approve baselines/windows/thresholds, distinguish startup/spikes; never inflate expectations. |
| S3-14 | Approve total and batch/agent budgets and triggers; aggregate parallel use without omission/double counting. Subtask anomalies pause corresponding work; total anomalies pause related parallel work. No silent budget increases. |
| S3-15 | Resource/rate/progress/repeated-failure pauses need cause, usage, saved work, repair proposal and remaining estimate plus human recovery approval. Single transient faults may retry only under bounded preapproval, original budget and retry count. |
| S3-16 | Approve save points and overhead at batch ends and costly milestones; record results/config/versions/usage; check integrity/applicability on recovery; rerun only missing/corrupt/invalid portions. |
| S3-17 | Deliver decision summary plus full validation records, traceability, reuse, usage, pass/fail status, risks and formal-execution proposal. |
| S3-18 | Disclose actual telemetry and interrupt granularity; propose smaller batches or supported runtime limits for blind spots; do not claim unavailable realtime protection. |

Historical checkpoint after Step 3: Steps 1–3 accepted; superseded by the Step 4 checkpoint below. No research execution has been authorized by these documentation updates. Runtime/token thresholds remain project-specific, not universal numeric defaults.

## Step 4 — approved calibration

User approved [Step 4](step-4.md), its diagram and gates for publication. This is reusable policy, not authorization for a specific formal run.

| ID | Agreed decision |
| --- | --- |
| S4-01 | Execute the approved protocol plus prespecified analyses; report results, uncertainty and deviations; new exploration/method changes need reasons, impact, scope/budget and prior approval, separate from original analysis. |
| S4-02 | Reuse Step 3 batching, monitoring and pause/recovery rules, but approve formal-scale batches, budgets and stop thresholds. Normal batches continue; no interim-result-driven standard changes. |
| S4-03 | Propose project-specific visible metrics, viewing times, use boundaries and actions for approval. Monitor operational quality/resources continuously; do not seal every result by default. |
| S4-04 | Low-impact accidental exposure continues under preapproved rules with log/checkpoint report. Possible method-selection/validation impact requires minimal remedy options for human decision; no automatic invalidation or reruns. |
| S4-05 | Negative/nonsignificant/inconclusive results are reported and original protocol completed subject to stop rules. Only preapproved bounded data/implementation diagnostics; no tuning for favorable results. |
| S4-06 | Preserve original results, mark errors and affected dependencies. Repair/rerun within explicit approved bounds, otherwise propose minimal plan. Broad impact may justify human-approved broad reruns; unaffected results remain. |
| S4-07 | Independent verifier fully checks key results; other results sampled under agent-proposed human-approved plan. Reuse valid evidence. Anomalies requiring expansion need impact, scope, rationale, budget and prior approval. |
| S4-08 | Approve protocol-derived critical-results list before execution. Additions require significance-to-conclusion explanation and supplementary scope/budget approval. Importance never follows outcome desirability. |
| S4-09 | Challenger checks support for current wording, uncertainty and competing explanations using authorized evidence only. New analyses require approval; comprehensive synthesis belongs to next stage. |
| S4-10 | Material unresolved correctness or interpretation concerns block affected results being marked verified. Other limits are recorded; human chooses further work or qualified continuation; no unresolved-to-pass conversion. |
| S4-11 | Deliver decision summary plus full traceable results, deviations, verification status, execution/resource records, unresolved concerns and next-stage scope/budget/outcomes proposal. Human decides progression. |

Current checkpoint: Steps 1–4 calibrated and published; Step 5 pending. No research runs authorized by this documentation update. Continue one multiple-choice question at a time. Numeric resource limits remain project-specific.
