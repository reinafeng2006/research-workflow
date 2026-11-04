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

Project-specific budgets, numerical revision/checkpoint values, recipient completion criteria and optional follow-up authorization. Publishing this policy does not authorize a new investigation.

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


## Step 5 — approved calibration

The human approved the [Step 5](step-5.md) workflow, gates and bilingual publication as reusable policy, not a project run or external research-publication authorization.

| ID | Agreed decision |
| --- | --- |
| S5-01 | Propose project-specific synthesis and delivery scope, budget, outcomes and tradeoffs for human approval before starting; reuse valid evidence, no automatic new analysis. |
| S5-02 | Classify gaps by impact: record ordinary limitations and continue; potential core-conclusion/use changes pause affected work with impact, qualification, additional-analysis or upstream options and budgets for human decision. |
| S5-03 | Recommend framework-first or direct drafting based on complexity, disagreement and use; explain costs/tradeoffs for stage-plan approval. |
| S5-04 | Review accuracy, traceability, interpretation boundaries and audience suitability; approve scope, budget and rationale first; review new synthesis/wording and affected content only, reusing valid evidence. |
| S5-05 | Revisions preserving meaning, evidence strength and applicability may proceed within approved scope/budget with records; material conclusion, qualification or use changes pause affected portions with reasons/options/budget for human decision. |
| S5-06 | Approve project-specific version checkpoints, continuous-revision bounds and reasons, budgets, revision rounds, effective progress and stops; any stop condition pauses work with unresolved issues and next options. |
| S5-07 | Core correctness, evidence-support or use issues block affected finalization; other issues need impact, bounds, owner and deadline for human acceptance; qualifications/omissions require human decision and retain unresolved status. |
| S5-08 | Submit decision summary and full package with conclusions, evidence limits, reviews, open issues, approvals, deliverables, conclusion-evidence map, review/revision and resource records; human approves exact final version without automatic publication authority. |
| S5-09 | Approve full workflow, pause diagram and gates. Separate Step 4 result verification from Step 5 synthesis/delivery; preserve unresolved status across stages and never repeat valid checks. |
| S5-10 | Synchronize Chinese/English documentation, diagrams, templates and calibration records; Step 6 scope remains pending; continue one multiple-choice question at a time. |

## Step 6 — approved calibration

See [Step 6](step-6.md). The later delivery-first clarification governs; early optional work combinations are not prerequisites for required delivery.

| ID | Agreed decision |
| --- | --- |
| S6-01 | Prioritize project/recipient-based required delivery, necessary archive and approved closure before optional follow-up; this supersedes the earlier equal-priority ordering of the three work types. |
| S6-02 | Propose scope, budget, outcomes, reasons and tradeoffs for human selection/approval; reuse known requirements, valid outputs and records without automatic analysis or duplicate checks. |
| S6-03 | Propose archive depth, scope, budget and criteria based on reuse/resumption needs, storage cost and restrictions for approval; no default validation reruns. |
| S6-04 | Propose prepublication checks, depth, budget and decision items based on channel, audience and restrictions; reuse valid records, no research reverification; actual submission/publication needs explicit authority. |
| S6-05 | Record nonmaterial formatting/layout/file changes within preapproval; new analysis or changes to conclusions, qualifications, authorship or disclosure pause affected work with minimal plan, impact, options and budget; approved upstream return may target Step 5 or earlier. |
| S6-06 | Propose materials-ready, submission-success, recipient-confirmation or another explicit completion criterion and reasons for approval; retain unachieved states, no automatic relaxation, optional follow-up never blocks closure. |
| S6-07 | After closure offer bounded follow-up value/cost/tradeoff suggestions; separately approve selected scope/budget/outcomes, no automatic goals/execution or required-delivery budget diversion. |
| S6-08 | Compare none/on-demand/bounded periodic maintenance; approve scope, triggers, frequency, duration, budget and stops; no monitoring, execution or modification before explicit approval. |
| S6-09 | Record preapproved nonmaterial maintenance; potential conclusion/evidence-validity/authorship/disclosure impact pauses work with impact, minimal remedy and budget for decision; preserve originals, no automatic reruns, retraction or republication. |
| S6-10 | Approve total plus work-type subbudgets, effective-progress criteria and stops; any stop pauses and reports; periodic maintenance preserves cumulative usage, stops at expiry and requires prior renewal, without per-run budget resets. |
| S6-11 | Executor self-check plus independent verifier under approved project-specific scope/depth/assignments/reasons/budget; check archive continuity, delivery/authority accuracy and maintenance boundaries; new or affected content only. |
| S6-12 | Material delivery/archive-usability/authority/maintenance issues block affected completion; other issues need impact/bounds/owner/deadline for acceptance; passed unaffected portions may be confirmed separately, retaining open status. |
| S6-13 | Summary/full handoff includes completion/acceptance, issues, exact versions, archive index, authority/actual receipts, reviews, resources and resumption; separately record prepared, authorized, submitted/published, recipient confirmed, closed and maintenance actually started. |
| S6-14 | Human approved revised main workflow, resource/stop diagram and gates for bilingual docs/templates/calibration records; saving policy grants no project submission or scheduled-maintenance authority. |


Current checkpoint: Steps 1–6 calibrated and saved. Project budgets, numeric limits, recipient completion criteria and optional follow-up authority still require project-specific approval. Earlier Step 6-pending statements are historical and superseded here. Documentation publication authorizes no research run, submission or scheduled maintenance.

## v0.8 — 2026-10-27

Human-approved cross-stage corrections: (1) Step 3 warnings cannot bypass batch gates; (2) capture delivery constraints early; (3) separate applicability, verdict, readiness and authority; (4) reuse exact matching stage authorization. Implement a single check registry, authorization records, serialized pre-dispatch budget admission and artifact-level role combination boundaries. No new research or automatic publication authority. See shared-controls.md and the fictional walkthrough.

## v0.9 — 2026-10-31

Restructuring directions approved by the user: (1) team research at the depth of a "work-assignment system"; (2) gates simplified by combining "three universal gates" with "tiers by project scale".

| ID | Agreed decision |
| --- | --- |
| S9-01 | Gates are unified into three kinds — G1 material ready, G2 independently verified, G3 human authorization — three per stage, 18 per project. Stage gates, runtime conditions and human authorization are recorded as separate kinds of decision rather than mixed in one gate table. |
| S9-02 | The substance of all 38 original mandatory items is kept, demoted to checklist items under the gates. Four are merged: three handoff authorizations were recorded once by each adjacent stage (Step 2 implementation authorized / Step 3 authorized; Step 3 and Step 4 formal execution authorized; Step 4 next stage authorized / Step 5 start authorized), and Step 6 "independent verification complete" is G2 itself. 34 substantive requirements remain. |
| S9-03 | "Batch may continue" and "resources and duration controlled" are reclassified as runtime conditions, judged per batch or checkpoint rather than at stage end. 34 substantive requirements = 22 checklist items (G1 nine, G2 thirteen) + 10 authorization points + 2 runtime conditions. |
| S9-03a | Authorization points have two counts: 10 mapped from v0.8 items; 12 when the stage documents list actual decision points. The difference is that Step 1 "human selection and authorization" splits into the tier and feasibility contract, the specific question and the next-stage authorization, because they happen at different times. Checklist counts are unaffected. |
| S9-04 | New project tiers `lite` / `standard` / `strict`, with checklist breadth of 13 / 21 / 22 items. The tier is chosen in the `profile` field of the Step 1 stage contract, approved by the principal and recorded in the decision log. |
| S9-05 | A tier is a recorded human decision, not a hidden lowering of the standard. Excluded checklist items are `not_applicable` with a reason based on approved scope; failure, missing evidence or lack of resources may not be relabelled as not applicable. |
| S9-06 | Tiers do not trim G3 authorization points and do not change the full-text verification requirement for decision-critical claims. `lite` reduces breadth of checking, not the level of evidence. `strict` mainly adds independence requirements, verification coverage and archive completeness. |
| S9-07 | Moving up a tier is always allowed; moving down needs the principal's approval and a record of affected conclusions that already passed. Checks passed at a higher tier stay valid. |
| S9-08 | A people layer is added — `principal` (final decision-maker), `approver`, `collaborator`, `reviewer`, `observer` — separate from agent roles. In a single-person project the user is the principal. |
| S9-09 | Non-delegable decisions: research goals and direction, substantive changes to method or conclusion boundaries, changes to quality standards, unauthorized scope or budget expansion, lowering the tier, actual external submission. |
| S9-10 | G2 and G3 for the same artifact are not performed by the same person. In groups of two or fewer, a principal who also owns a unit may self-approve G3, with the overlap recorded and G2 still performed by another person or an agent that did not produce it; recorded as an exception, not a pass. |
| S9-11 | A work unit is the smallest unit of assignment: one owner, mutually exclusive writable artifacts, acceptance criteria pointing to specific checklist items, budget admission before start, no start before dependencies are ready, and blocks reported immediately. People's time is treated as a constrained resource in the same way. |
| S9-12 | Handover does not transfer G2 responsibility; if the new owner took part in production, another verifier is assigned. When someone leaves, the principal reassigns unfinished units; checks already passed stay valid. |
| S9-13 | Contribution records are generated from work units' `owner` and `material_contributors` and are traceable; author order is the principal's decision, and agents may not infer or fill it in. A full contribution taxonomy is left for a later version. |
| S9-14 | Disagreements between people keep each side's evidence, assumptions and effect on the recommendation for the principal to decide; majority vote does not replace evidence. Formal arbitration rules are not part of v0.9. |
| S9-15 | Terms: user and principal are the same in a single-person project; in team projects the user may name other approvers, while non-delegable decisions remain the principal's. Gate identifiers and tier values are not translated. |
| S9-16 | The restructuring proceeds in batches, with the English mirror synchronized in a later batch; until then `en/` is explicitly marked stale and may not be treated as the current rules. |

This restructuring replaces how the old gate tables were **organized**, not any of their substantive requirements. The v0.8 item text and IDs remain in the stage documents, and checks passed under v0.8 stay valid. Open: several people sharing the principal role, formal arbitration rules, a contribution taxonomy.

## v0.9.1 — 2026-11-03: division of labor first

The user asked for a division-of-labor document independent of stage details, with the other documents then rebuilt around it. Reason: an overly complex structure creates information asymmetry between people and AI; a person who cannot follow what the AI produced cannot decide well, and people need to take part in every step.

| ID | Agreed decision |
| --- | --- |
| S10-01 | New docs/division-of-labor.md, which prevails over any stage document or configuration it conflicts with. The boundary is drawn by the nature of the decision, not by stage. |
| S10-02 | Principle: whoever carries the consequences makes the call; what can be checked is the AI's to judge; both sides are in the process. There are only two reasons the call is the person's: the consequences are theirs, and a preference cannot be overturned by evidence. |
| S10-03 | "Only the person knows the use" and "only the person knows who it helps" are not adopted: they are false. Recipient requirements, journal standards, course briefs and licence terms are written in files the AI often reads more completely; the person's side of the information is often incomplete, which is why the AI must contribute. |
| S10-04 | "People diverge better than AI" is not adopted: an unverified empirical claim cannot justify a rule. Anyone may propose ideas; the only requirements are that sources stay distinguishable and that nothing becomes a goal without the person's nod. The direction log will make the question checkable. |
| S10-05 | The four kinds of decision where the person makes the call: what is worth doing, what counts as enough, what goes outside, overruling a verdict. The AI must contribute in each, including disagreeing explicitly; "you decide" is not acceptable, and keeping a doubt to itself is a failure of duty. |
| S10-06 | The four-field update: before each segment of work, state what is being done, what it will produce, which step comes next and where it sits in the whole project; re-state immediately if any field changes; give it at once when the person stops the work; sunk cost is not authorization. It is a process obligation, not a gate checklist item. |
| S10-07 | The four items at a decision point: one-sentence conclusion and recommendation, what it turns on (at most three), the loss if the judgment is wrong, and the least necessary information with where to check it. A new cross-stage G1 checklist item "decision material usable" (lite) is added; truthful material the decider cannot follow does not pass G1. |
| S10-08 | Counts are updated: 35 substantive requirements = 23 checklist items (G1 ten, G2 thirteen) + 10 authorization points + 2 runtime conditions; tier breadth 14 / 22 / 23. |
| S10-09 | AGENTS.md changes from a stage-by-stage restatement to a pointer file: read the division of labor first, keep only the line most easily crossed for each stage, and leave the details in the stage documents. A check confirmed that every removed restatement has a corresponding rule in the stage documents. |
| S10-10 | The README states that only two documents need reading before starting: the README and the division of labor; the rest as needed. |

## v0.9.2 — 2026-11-03: Step 1 divergence and appraisal

The user chose: appraisal as "argument base plus scores used only for ranking"; divergence as "operators plus five extension types" combined.

| ID | Agreed decision |
| --- | --- |
| S11-01 | New docs/divergence-and-appraisal.md and templates direction-log.md and appraisal-matrix.md. Originally proposed as two specifications; merged into one because the user had said the repository was too complex. |
| S11-02 | Two divergence axes: eight lateral operators look for different directions from the current idea; five vertical extension types grow the next question from a chosen direction. Both are working checklists and do not claim to exhaust the space of directions. |
| S11-03 | Coverage is not counted but accounted for, operator by operator and extension type by type: directions produced, tried without result, or not tried with a reason. |
| S11-04 | Substantive difference: at least one of subject, outcome measure, contrast or the decision it can inform differs. Proposed by the AI and confirmed by the user; duplicate directions are merged, not deleted. |
| S11-05 | Every direction names its proposer (the user, the AI, or the direction it derives from); dropped directions keep their reasons. |
| S11-06 | The argument base A1–A8 is required for every candidate; an item that cannot be answered says "unknown" and what is missing. |
| S11-07 | Seven scoring dimensions with 0–5 anchors. Every score must point back to base items and carry an evidence level; missing either makes it invalid and excluded from ranking. All candidates use the same dimensions. |
| S11-08 | No weighted total: any weighting is an unverified claim. Ranking follows the published decision rules, with the mean for reference only. Decision thresholds are proposals; changes are recorded and every candidate is re-judged. |
| S11-09 | Every appraisal states its sensitivity: what the verdict becomes when the one to three most sensitive scores or assumptions change. |
| S11-10 | The decision brief's six-column free-text appraisal table is replaced by a reference to the appraisal matrix. |
| S11-11 | Whether divergence coverage and score traceability become G1/G2 checklist items is left to the user; gate counts do not change until then. |
| S11-12 | User decision: "divergence coverage accounted for" joins Step 1 G1 and "appraisal comparable and scores traceable" joins Step 1 G2, in all three tiers. Supersedes S11-11. Counts become 37 substantive requirements = 25 checklist items (G1 eleven, G2 fourteen) + 10 authorization points + 2 runtime conditions; tier breadth 16 / 24 / 25. |

## v0.9.3 — 2026-11-04: slimming the stage documents

After assessing the whole workflow, the user decided to slim the six stage documents to "output and boundaries, stage-specific rules, checklist items, and the points where the person makes the call", with general rules referenced rather than restated. Research safeguards and the 37 gate requirements are unchanged.

| ID | Agreed decision |
| --- | --- |
| S12-01 | The six stage documents go from 1041 to 645 lines; diagrams from 359 to 107 lines, each showing only that stage's main line rather than redrawing the generic approve/revise loop. |
| S12-02 | The rules for batches, rates, pauses, retries, saving and recovery, formerly in Step 3, are in fact runtime controls shared by Steps 3, 4 and 6; the original text moves to shared-controls.md section 7 with the rules unchanged, and Steps 3, 4 and 6 reference it. |
| S12-03 | Per-stage role tables are removed; role requirements belonging to one stage only (such as the Step 1 methods specialist not designing early, the Step 2 desk walkthrough, the three Step 5 reviews) are written into that stage's specific rules. |
| S12-04 | Verification method: all 639 sentences of the old documents were scored for coverage in the new set, and every low-coverage sentence was judged by hand; the 7 stage-specific rules found missing were restored (four in Step 1, two in Step 2, one in Step 4, plus two phrasings in Step 6). 32 research safeguards and 7 runtime rules were also checked by exact search; all present. |
| S12-05 | The cut was smaller than estimated beforehand (450–550 lines for stage documents and about 1700 overall estimated; 645 and 2142 actual). Reason: keyword counting overstated the repetition — the Step 3 runtime rules were a source, not a duplicate, most of Step 6 is stage-specific, and several rules were restored after checking. |

## v0.9.4 — 2026-11-04: agent roles and project specialists

The user proposed that agents be distinguished by what they are good at, but noted that every project needs different specialties.

| ID | Agreed decision |
| --- | --- |
| S13-01 | Agents are distinguished by specialty (what they look at, what they may read, what they deliver), not personality. New docs/agents.md. |
| S13-02 | Two layers: fixed functions (coordinator, producer, independent verifier, challenger) are the same in every project, for structural reasons; project specialists are configured per project and per stage, replacing the vague "methods specialist (as needed)". The config key methods_specialist is kept for compatibility. |
| S13-03 | Specialists are mainly derived from the parts of the research question and the appraisal matrix's sensitivity, with their source stated, then checked item by item against the specialty library for gaps. The library is a working checklist and does not claim completeness. |
| S13-04 | The specialist list is proposed by the AI and approved by the user as part of the Step 1 "tier and feasibility contract" authorization point; per-stage adjustments are approved in each stage's start authorization. No authorization point is added and gate counts are unchanged. 2–4 per stage is a proposal. |
| S13-05 | The challenger gains a duty: find angles no specialist covers, to offset the risk that assigning specialists by sensitivity only watches known risks. |
| S13-06 | Personality is an optional presentation layer that does not change specialty; the interface must say whether several mates are one model, and "several mates agree" is not evidence. |
| S13-07 | The whole design is marked as an unverified default; the direction log records which specialist proposed each direction for later comparison. Whether to adopt a roundtable is left for a later decision. |
| S13-08 | User decision: the specialty library is restructured on two axes, "discipline lens × research function"; a concrete specialist = discipline × function. The old library compressed "domain" into one row and assumed quantitative empirical research. |
| S13-09 | The discipline axis does not invent its own classification; it adopts the FORD classification in chapter 3 of the OECD Frascati Manual 2015. Verification status is abstract-level (from search results): 6 broad fields, 42 sub-fields and a content-based approach seen in summaries; broad field names not checked against the source, because this environment's network policy blocked uis.unesco.org and unstats.un.org. Must be checked before adoption. |
| S13-10 | Discipline lenses per stage: one home discipline plus one or two near or far disciplines; near and far ones are used specifically for divergence and may be assigned to divergence operators. |
| S13-11 | The function axis is grouped by type of research (all research, quantitative empirical, qualitative, theoretical and formal, sources and texts, building and engineering), correcting the quantitative bias; still a working checklist that does not claim completeness. |
| S13-12 | What an AI says from a discipline's point of view is not evidence and still needs direct sources under the Step 1 evidence rules; how well a model simulates a discipline is unverified. |
| S13-13 | FORD verification result: the United Nations Statistics Division classification registry confirms the source (Manual 2015 chapter 3, ISBN 978-92-6423880-0), the structure of 6 broad fields and 42 sub-fields, the content-based approach, and one broad field, "engineering and technology". The other five broad fields and the 42 sub-field names remain unverified: the registry does not list them, the UNESCO links are dead, and the OECD site refuses automated access. Supplements S13-09. |

## v0.9.5 — 2026-11-04: roundtable

| ID | Agreed decision |
| --- | --- |
| S14-01 | "Independent first, then roundtable" adopted, for now only for Step 1 divergence. The independent phase is lateral: each specialist diverges in an isolated call with its assigned operators; the roundtable phase is vertical: building on each other, merging duplicates, growing along extension types. |
| S14-02 | The verifier does not sit at the table (G2 independence); the user may interject, add directions or veto at any time; the roundtable does not choose directions for the user and does not force consensus. |
| S14-03 | The interface must say whether the mates are one model; agreement among mates is not evidence and does not mean the user agrees. |
| S14-04 | The user writing directions before the table is optional; "people speaking first reduces AI anchoring" is unverified and not a rule. |
| S14-05 | Rounds and budget are approved with the Step 1 divergence budget and stop when reached; the four-field update applies every round. |
| S14-06 | The whole is an unverified default; the direction log gains a "produced in" column (independent phase / roundtable / user) for later comparison. |
| S14-07 | The user switched to a **full roundtable**, superseding S14-01's "independent first, then roundtable". After the AI restated the convergence risk, three countermeasures make convergence visible: speaking order rotates every round; every mate proposes at least one direction per round with its assigned operators; the challenger checks each round with the four substantive-difference criteria and reports convergence. S14-02 to S14-05 are unchanged; the direction log's "produced in" column becomes "roundtable round N / you", superseding the wording in S14-06. |
| S14-08 | The user explained the reason for a full roundtable: everyone should think along the same line, and the starting point is necessarily the user's question. Written into the specification: the roundtable starts from the user's question and accepted goals, all mates share one starting point; align on the question and goals, diverge on directions; when a mate's reading of the question differs from the user's, it raises it for the user to clarify and may not rewrite the question. Separate divergence may produce false diversity when mates each misread the question, which the earlier trade-off had not listed. Supersedes S14-04's wording that the user writing directions first is optional: the question coming from the user is structural, while writing additional directions remains optional. |

## English mirror synchronized — 2026-11-04

| ID | Agreed decision |
| --- | --- |
| S15-01 | `en/` is synchronized with the Chinese v0.9.5: 8 new and 19 updated files, translated against the final Chinese text; the calibration record appends only the v0.9 and later sections, leaving earlier history as it was. Supersedes the "en/ is stale" state of S9-16. |
| S15-02 | Three outdated Chinese passages found during synchronization were corrected at the source: the division of labor still called the direction log "to be built"; the language policy's "current synchronization scope" still described v0.7; the README still said the English version was v0.8. |

## v0.9.6 — 2026-11-04: all files aligned to one version

Before checking whether the workflow can run, the user asked for all files to be on the same version. An inventory found 18 files untouched since the v0.8 synchronization, several of them inconsistent with the v0.9 rules.

| ID | Agreed decision |
| --- | --- |
| S16-01 | The current version number is unified as v0.9.6: the README, configuration and translation manifest said v0.9 while the content had reached v0.9.5. Historical mentions such as "v0.8's 38 gates" are unchanged. |
| S16-02 | Critical gap: the cross-stage G1 checklist item "decision material usable" requires the four items at every decision point, but only the two Step 1 templates had a place for them, so Steps 2–6 could not record them and therefore could not pass. The four items now open the method comparison, pilot check, research protocol, Step 3 validation record, Step 4 results package, Step 5 delivery package, Step 6 handoff package and upstream review. |
| S16-03 | The Step 3–6 plan templates gain the tier, a record block for the stage's checklist items and authorization points, runtime conditions, and project-specialist and work-assignment references; the Step 3 and 4 plans note that runtime rules are in shared controls section 7; the Step 6 plan references the submission action's own work unit. |
| S16-04 | Each check in the check registry gains `checklist_item`, `gate` and `tier`; the verification report table gains "gate" and "lowest tier" columns and notes that the verifier did not take part in production; the task launch record gains the four-field update and the work unit; the decision log gains a "type" column, with lite-tier self-approval overlaps recorded as exceptions. |
| S16-05 | The duplicated `assessed_by` and `assessed_at` keys in the check registry are removed, the same kind of defect as the earlier duplicate keys in the authorization record template. |
| S16-06 | The v0.8 walkthrough is marked "historical record, superseded, to be redone" without rewriting its content; a walkthrough of the current rules belongs to the later verification step, which is not yet approved. |

