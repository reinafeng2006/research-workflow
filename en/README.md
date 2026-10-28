# Research workflow

English reference of the [authoritative Chinese README.md](../README.md). Both versions express the same calibrated rules; see [language policy](docs/language-policy.md) and [translation manifest](../translation-manifest.json). Use the mirrored configuration, docs, and templates together.


A reusable starter for research and study projects driven by multiple agents, fixed stage objectives, independent verification, and budget-aware upstream review.

**Status: v0.8 — Steps 1–6 calibrated; project controls require approval.** This repository contains instructions and templates, not an executable orchestration service. Quality thresholds and resource budgets must be calibrated for each project. Token accounting depends on the host's telemetry.

## Minimal startup

1. On GitHub, select **Use this template** to create a new project repository, then open it in an agent environment that can read project files. Keep project outputs in the new repository, separate from this reusable starter.
2. Add existing materials or provide accessible file paths/links. You do not need to fill every template yourself or recalibrate all six stages.
3. Paste the prompt below. Agents first read the inputs, identify the entry stage and propose the first bounded work plan; substantive research starts only after your approval.

### Copyable startup prompt

```text
Initialize my research project using this project's AGENTS.md,
research-workflow.yaml and docs/shared-controls.md, then read the
specification for the applicable stage.

Research topic/question: [fill in]
Current inputs: [broad idea / candidate questions / defined question /
existing protocol or results]
Desired project value: [multiple goals are welcome, without ranking;
uncertainty is fine]
Existing materials: [file paths or links; write none if unavailable]
Known delivery requirements, deadline and constraints: [unknowns may be blank]
Hard budget limits: [if known; otherwise propose a budget]

Read existing materials first and record the workflow commit used.
Select the entry stage from existing work, filling only missing prerequisites.
Explain the environment's support for independent verification, resource
accounting, pausing and persistence before planning execution.
Create the project brief and propose the first work scope, expected outputs,
quality gates, roles, budget and stop conditions as one decision package
for my approval.

Ask only unanswered questions, one multiple-choice question at a time,
allowing custom or combined answers. Reuse valid authorization and evidence.
Do not begin substantive research before the initial plan is approved.
```

### What you provide and what agents read and organize

| Item | Your input | Agents' work |
| --- | --- | --- |
| Topic and starting point | What you want to study and what already exists | Identify the entry stage and missing prerequisites |
| Goals | Desired value; multiple unranked goals or initial uncertainty are welcome | Clarify success criteria and propose optional outcomes for your choice |
| Materials and access | Files/links and necessary access permissions | Read existing briefs, protocols, results, decisions and verification records; organize versions and reusable evidence |
| Delivery and constraints | Known recipient requirements, deadlines and data/tool limitations | Map requirements to design and acceptance criteria; retain unknowns as unresolved |
| Budget | Known hard limits, or a request for a proposal | Propose time, tokens, investigation scope and rationale for approval |
| Project records | No need to fill every template yourself | Create briefs, contracts, authorization, check, resource and decision records as needed |

Agents should first read `AGENTS.md`, `research-workflow.yaml` and `docs/shared-controls.md`, then the current stage's specification and relevant templates. They should reuse existing project records before asking unanswered questions. Automatic reading requires access and an explicit startup instruction; sending a repository URL alone neither loads files nor runs the workflow. If a private repository is inaccessible, connect an account or provide a local copy.

For an existing project, copy `research-workflow.yaml`, `docs/` and `templates/`, and merge relevant `AGENTS.md` rules with existing instructions rather than overwriting them. English-language projects may use the corresponding configuration, documents and templates under `en/`; adjust the prompt paths accordingly. Record the actual commit used, not just the README version label.

### Runtime limitations

The repository provides policy and record templates. It does not automatically create agents, enforce budgets or launch background tasks.

| Control | Repository policy | Required runtime support |
| --- | --- | --- |
| Independent verification | Authors cannot independently accept their own artifacts | A separate agent or other independent reviewer; switching roles within one agent is not independent verification |
| Resource accounting | Include every role, retry, repair and review | Token/cost telemetry; without it, explicitly labeled estimates only |
| Real-time pausing | Rate, budget and no-progress stop rules | Continuous monitoring, timeouts and cancellation; documents cannot forcibly interrupt an active call |
| Concurrent budgets and deduplication | Reserve before dispatch; avoid duplicate work and overcommitment | Coordinator-serialized reservations and dispatch, or an atomic shared budget record |
| Persistence and recovery | Save outputs, versions and cumulative usage; rerun only invalidated portions | Persistent file storage; resuming an in-flight computation depends on its implementation |
| Scheduled maintenance | Explicit authorization, expiry, cumulative budgets and renewal rules | A scheduler; copying this repository starts no monitoring or maintenance |

If capabilities are missing, agents must disclose the limits and propose small batches, serial execution, human checkpoints or alternative independent review for your approval. Estimates are not measurements and policy is not technical enforcement; do not launch a task whose resource risk cannot be reasonably bounded. Reuse existing authority only within its recorded bounds and conditions; uncovered changes remain your decision. Finalization or closure does not automatically authorize actual submission/publication.

## Roles

| Role | Job | Why it exists |
| --- | --- | --- |
| Coordinator | Contracts, delegation, dependencies, budgets, and stage transitions | Keeps work aligned and iterations bounded |
| Researcher | Evidence, analysis, deliverables, self-checks, and repairs | Owns substantive production |
| Verifier | Independent checks against frozen acceptance criteria | Separates production from acceptance |
| Challenger | Counterexamples, assumptions, alternative explanations | Detects conceptual weaknesses beyond checklist compliance |
| Methods specialist | Domain, statistical, mathematical, or computational methods | Adds technical depth when needed |

Detailed responsibilities, beliefs, reactions, and limits are in [research-workflow.yaml](research-workflow.yaml).

## Stage cycle

Step 1: define and select a specific research question → Step 2: detailed methodology → Step 3: implementation preparation and bounded end-to-end validation → Step 4: formal execution and prespecified analyses → Step 5: research synthesis and delivery finalization → Step 6: required delivery, archive and approved project closure; optional follow-up is separately authorized.

See the [Step 1 workflow and diagram](docs/step-1.md) , [Step 2 workflow and gates](docs/step-2.md), [Step 3 workflow and resource controls](docs/step-3.md), [Step 4 execution and result review](docs/step-4.md), and [calibration record](docs/calibration-decisions.md). Broad ideas, candidate questions, and calibrated questions enter different phases of the same sequence.

Within each stage: produce → self-check → independent verification → diagnose → revise → verify again. Separate decision-readiness checks from scientific verification and human approval. Unresolved evidence or disagreement may be presented honestly for human decision; approval never converts it into verified evidence. A rigorous negative or inconclusive result may pass.

At a resource checkpoint or stagnation trigger, diagnose local execution problems, upstream defects, or underestimated workload. Reopen the smallest affected upstream stage when warranted, preserve prior versions, and revalidate dependent outputs. Never silently lower the quality gate.

The initial proposals are three revision cycles, two consecutive cycles without progress, and a budget review at 80%. These are escalation triggers, not substitutes for project-specific runtime and token budgets.

## Files and records

- `research-workflow.yaml`: source of truth for roles and workflow policy.
- `AGENTS.md`: operating instructions for assistants using this repository.
- `templates/project-brief.md`: calibration questions and project definition.
- `templates/stage-contract.yaml`: objectives, evidence checks, dependencies, budgets.
- `templates/verification-report.md`: criterion-by-criterion acceptance record.
- `templates/upstream-review.md`: diagnosis and recovery proposal.
- `templates/evidence-ledger.csv`: traceable claims and inspected sources.
- `templates/decision-log.md`: decisions, exceptions, and policy revisions.

For each project, create `project/brief.md`, `project/stages/`, `project/reviews/`, `project/artifacts/`, and `project/decisions.md` from these templates. Record the starter commit used so later policy updates can be adopted deliberately.

## Calibration still open

Step 1 goal handling, entry routing, budgets, evidence policy, decision authority, and next-stage authorization are calibrated. Concrete budgets remain project-specific and require approval. The numeric iteration/checkpoint defaults remain proposals. Step 2 comparison, limited tests, independent review, protocol gates, checkpoints, fallback and repair rules are calibrated. Step 3 batching, reuse, resource monitoring and pause/recovery rules are calibrated. Step 4 protocol-bound execution, tiered review, interpretation boundaries and unresolved-issue handling are calibrated. Project-specific controls still require approval.

## Step 2 templates

- [Method comparison](templates/method-comparison.md)
- [Bounded pilot or technical trial](templates/pilot-check.md)
- [Decision summary and execution-ready protocol](templates/research-protocol.md)

A material unresolved design choice blocks protocol-ready status. Transparent uncertainty in a Step 1 decision brief does not waive this Step 2 requirement.

## Step 3 templates and reuse

Use [Step 3 plan](templates/step-3-plan.yaml) and [validation report](templates/step-3-report.md). Step 2 finalizes the protocol; Step 3 checks implementation. Reuse valid evidence and pilot artifacts; only new gaps or invalidated portions need checks. These documents specify monitoring requirements; they do not implement a realtime resource controller.

## Step 4 templates

Use [formal execution and review plan](templates/step-4-plan.yaml) and [results package](templates/step-4-results.md). Execution completion, per-result verification and authorization to proceed are distinct. Reuse valid evidence; do not repeat checks merely because the stage changed.

## Step 5 synthesis and delivery

See [Step 5 workflow and gates](docs/step-5.md), [plan](templates/step-5-plan.yaml) and [delivery package](templates/step-5-delivery.md). Step 4 verifies results; Step 5 reviews new synthesis and wording. Reuse valid evidence, classify issues by impact, and obtain human finalization approval. Finalization does not authorize external publication. Step 5 is calibrated; Project-specific controls still require approval.

## Step 6 required delivery and closure

See [Step 6 workflow and gates](docs/step-6.md), [plan](templates/step-6-plan.yaml), and [handoff](templates/step-6-handoff.md). Recipient requirements guide necessary delivery/archive and the human-approved completion criterion. Optional follow-up never blocks closure. Actual submission requires explicit exact-version/action authority; record prepared, authorized, submitted, recipient confirmed, closed and maintenance-started states separately.

Read [shared controls](docs/shared-controls.md) alongside stage rules. Use the authorization, check-registry, task-launch and role-assignment templates. Existing authority is reusable only within its recorded bounds; human decisions remain authoritative.
