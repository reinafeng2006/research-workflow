# Gates, tiers and runtime conditions

Status: new in v0.9, introduced by the human's direction decision of 2026-10-31 (three universal gates plus tiers by project scale). This document replaces how the 38 mandatory stage gates were **organized**; it removes none of their substantive requirements. The v0.8 item text and IDs remain in the stage documents, and checks that passed under v0.8 stay valid; reuse rules are in [Shared controls](shared-controls.md) section 4.

## 1. Separate three kinds of decision first

The v0.8 gate tables mixed three different kinds of decision in one table. That is the real cause of the item count and the interface complexity.

| Kind | Question asked | When judged | Judged by |
| --- | --- | --- | --- |
| Stage gate | Can this stage end? | End of stage | See the three gates below |
| Runtime condition | Can authorized work continue? | Each batch / checkpoint | Coordinator, under approved rules |
| Human authorization | Has a person approved it? | At each decision point | The principal or an authorized approver |

The third kind is both a gate and a record. Gate G3 checks only whether an authorization record exists and covers the exact version and scope; the authorization itself is a human act, and an agent cannot tick it on the person's behalf.

## 2. Three universal gates

Each stage has exactly three gate judgments: 18 across the six stages.

### G1 material ready

- **Object**: the exact version of the stage's deliverables.
- **Judged**: proposed by the coordinator after the producer's self-check.
- **Pass condition**: the deliverables exist in an exact version; every applicable checklist item has a conclusion; open questions, retained objections and the distinction between estimates and measurements are stated truthfully; every point awaiting decision meets the cross-stage checklist item "decision material usable" (section 7).
- **What failing means**: the material is not yet enough for an informed decision; it does not mean the research failed.
- **Key distinction**: material ready ≠ claims verified. Material can be ready while openly disclosing uncertainty; defective or misleading material cannot be marked ready.
- **Not a substitute**: an exhausted budget, agent consensus, length. Material that is truthful but unreadable to the decider does not pass G1.

### G2 independently verified

- **Object**: the stage's applicable checklist items.
- **Judged**: an independent verifier who did not take part in producing the artifact (a person or an agent, meeting the tier's independence requirement).
- **Pass condition**: each item recorded as `pass` / `fail` / `not_verifiable`, with check IDs and locators for the underlying evidence; every `fail` has an observable repair condition.
- **Blocking rule**: a `fail` affecting core correctness, evidential support or the stage's conclusion boundaries blocks the affected part; other issues record impact, handling bounds, owner and resolution time, and a person decides whether to accept them.
- **Not a substitute**: the producer's self-check, a successful run, restating the producer's claims, `not_verifiable` items.

### G3 human authorization

- **Object**: all of the stage's applicable authorization points.
- **Judged**: the principal, or an approver named in the authorization matrix (see [Team research](teamwork.md) section 2).
- **Pass condition**: every authorization point has a valid authorization record linked to the person's decision in their own words, the exact version, scope, budget, expected outputs and conditions; authorization pointing to the next stage states its scope, budget and expected outputs.
- **A stage may have several authorization points** (Step 2 has three). The interface still shows one gate: it passes when all applicable authorization points are covered. Several points may be bundled into one decision package and approved together; see [Shared controls](shared-controls.md) section 2.
- **Not a substitute**: silence, a timeout, approval of a direction, approval of the final text (finalization does not authorize external release). A human-approved exception stays an exception and is never re-labelled a G2 pass.

## 3. Three tiers

| Tier | Typical project | G1 / G2 checklist items | Independence | Evidence depth |
| --- | --- | --- | --- | --- |
| `lite` | Coursework, a one-week group exercise, internal exploration | 16 (of 25) | Another group member who did not produce the artifact may perform G2 | Decision-critical claims still need full-text verification |
| `standard` | Conference paper, internal lab report, external readers | 24 (of 25) | Independent per artifact; verifiers do not accept their own work | As above, plus a complete check registry |
| `strict` | Journal submission, external recipient, compliance or licence constraints | All 25 | Strictly per the [role assignments](../templates/role-assignments.yaml); the desk walkthrough is done by someone who did not design | As above, plus archive continuity and traceable check IDs throughout |

What `strict` adds is mostly not checklist items but independence requirements, coverage of decision-critical claim verification, and completeness of the check registry and archive.

**Tier rules**

1. The tier is chosen in the Step 1 stage contract, written in the `profile` field, approved by the principal and recorded in the decision log.
2. **A tier is a recorded human decision, not a hidden lowering of the standard.** Excluded checklist items are marked `not_applicable` with a reason based on approved scope; failure, missing evidence or lack of resources may not be re-labelled as not applicable.
3. Moving up a tier is always allowed. Moving down needs the principal's approval and a record of the affected conclusions that already passed: checks passed at the higher tier stay valid, but conclusions restated at the lower tier must note the change of basis.
4. **Tiers never trim G3.** All authorization points apply in every tier — human decision rights do not shrink with project size; tiers affect only the breadth of G1 and G2 checklist items.
5. **Tiers do not change the evidence standard for a single claim.** Full-text verification of decision-critical claims holds in all three tiers. `lite` reduces the breadth of checking, not the level of evidence.

## 4. Mapping 38 → 34

Four items are merged: three handoff gates were the same authorization recorded once by each adjacent stage, and Step 6 "independent verification complete" is the G2 gate itself rather than an item under it.

| Original gate | Stage | Now | Lowest tier |
| --- | --- | --- | --- |
| Decision readiness | 1 | G1 | lite |
| Human selection and authorization | 1 | G3 | all tiers |
| Comparison ready | 2 | G1 | lite |
| Small tests authorized | 2 | G3 | all tiers (when the action occurs) |
| Detailed design authorized | 2 | G3 | all tiers |
| Protocol ready | 2 | G2 | lite |
| Implementation authorized | 2 | G3 | all tiers |
| ~~Step 3 authorized~~ | 3 | merged into "Implementation authorized" | — |
| Implementation conforms | 3 | G2 | lite |
| Appropriate coverage | 3 | G2 | standard |
| Batch may continue | 3 | **runtime condition** | — |
| Reproducibility | 3 | G2 | standard |
| Decision package ready | 3 | G1 | standard |
| Formal execution authorized | 3 | G3 | all tiers |
| ~~Formal execution authorized~~ | 4 | merged into the Step 3 gate of the same name | — |
| Execution/analysis conform | 4 | G2 | lite |
| Appropriate review | 4 | G2 | lite |
| Interpretation bounded | 4 | G2 | lite |
| Accurate unresolved status | 4 | G1 | lite |
| Next stage authorized | 4 | G3 | all tiers |
| ~~Start authorized~~ | 5 | merged into Step 4 "Next stage authorized" | — |
| Evidence/status traceable | 5 | G2 | lite |
| Synthesis and wording supported | 5 | G2 | lite |
| Delivery suitable | 5 | G2 | standard |
| Revision authority clear | 5 | G3 | all tiers |
| Issues classified accurately | 5 | G1 | standard |
| Finalization package ready | 5 | G1 | lite |
| Finalization/publication separate | 5 | G3 | all tiers |
| Required delivery explicit | 6 | G1 | lite |
| Plan and completion criterion approved | 6 | G3 | all tiers |
| Valid outputs reused | 6 | G2 | strict |
| Mismatches handled by impact | 6 | G2 | standard |
| Necessary archive suitable | 6 | G2 | standard |
| ~~Independent verification complete~~ | 6 | is G2 itself | — |
| Unresolved issues retained | 6 | G1 | lite |
| Submission explicitly authorized | 6 | G3 | all tiers |
| Resources and duration controlled | 6 | **runtime condition** | — |
| Optional follow-up does not block closure | 6 | G1 | standard |

Check: 38 original items − 4 merged = 34 substantive requirements = 22 checklist items (G1 nine, G2 thirteen) + 10 authorization points + 2 runtime conditions.

**Both authorization-point counts hold, with different meanings.** The 10 above are mapped from v0.8 items; the stage documents, listing actual decision points, have **12**. The difference is Step 1: v0.8's "human selection and authorization" bundled three decisions — the tier and feasibility contract, the specific question, and the next-stage authorization for Step 2. v0.9 lists them separately because they happen at different times (before investigation, after appraisal, optionally together with the question). The number of checklist items is unaffected.

## 5. Two runtime conditions

| Condition | Applies to | Satisfied when |
| --- | --- | --- |
| Batch may continue | Each batch in Steps 3 and 4 | The batch met its pass criteria, made effective progress, triggered no stop condition, and further work remains authorized |
| Resources and duration controlled | Step 6 preparation, archiving, approved maintenance | Overall and sub-budgets valid, maintenance stops at expiry, renewal approved first, cumulative usage never reset |

Runtime conditions are judged per batch or checkpoint, not at stage end. A general rate alert only adds a notification; it does not waive G1 or G2. Logs and live processes are not progress. Detailed rules for batches, rates, pauses, retries, saving and recovery are in [Shared controls](shared-controls.md) section 7.

## 6. How it is recorded

The structure of `acceptance_criteria_and_check_methods` in the [stage contract](../templates/stage-contract.yaml) is unchanged; each criterion gains two fields:

- `gate`: `G1` / `G2` / `G3` / `runtime`
- `tier`: `lite` / `standard` / `strict`

The meanings of `applicability` (`applicable` / `not_applicable` / `undetermined`) and `verification_verdict` (`pending` / `pass` / `fail` / `not_verifiable`) are unchanged, and [Shared controls](shared-controls.md) section 3 still applies: `undetermined` is not a pass, and `not_applicable` requires `applicability_basis_and_approval`.

This document is a specification, not a runtime controller. Passing the three gates does not mean a research conclusion holds.

## 7. Checklist items added after v0.9

These three items are not among v0.8's 38, so they are not in the section 4 mapping. "Decision material usable" comes from the [Division of labor](division-of-labor.md), applies in every stage's G1 and counts as one substantive requirement; the other two come from [Divergence and appraisal](divergence-and-appraisal.md) and belong to Step 1 only.

| Checklist item | Condition | Gate | Lowest tier |
| --- | --- | --- | --- |
| Decision material usable (cross-stage) | Every point awaiting decision carries the four items: one-sentence conclusion and recommendation; what the decision turns on (at most three, ordered by impact); what the decider loses if the AI is wrong; the least necessary information and where to check it. Volume is no substitute for clarity; points that cannot be explained have been escalated, not covered by more text. | G1 | lite |
| Divergence coverage accounted for (Step 1) | Every one of the eight operators and five extension types is accounted for: directions produced, tried without result, or not tried with a reason; directions name who proposed them; dropped directions keep their reason. Counting directions does not satisfy it. | G1 | lite |
| Appraisal comparable and scores traceable (Step 1) | All candidates use the same argument base and scoring dimensions; every score used in ranking points back to the base and carries an evidence level; verdicts follow the published rules and state their sensitivity. | G2 | lite |

With these counted: 37 substantive requirements = 25 checklist items (G1 eleven, G2 fourteen) + 10 authorization points + 2 runtime conditions; tier breadth is 16 / 24 / 25 items.

The four-field update before each segment of work (what it is doing → what that will produce → which step comes next → where this sits in the whole project) is a **process obligation**, not a checklist item: gates check artifacts at the end of a stage, while the update happens during the work and cannot be supplied afterwards. Its rules are in the [Division of labor](division-of-labor.md) and [Shared controls](shared-controls.md) section 5.
