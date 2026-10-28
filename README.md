# Research workflow

A reusable starter for research and study projects driven by multiple agents, fixed stage objectives, independent verification, and budget-aware upstream review.

**Status: v0.5 — Steps 1–4 calibrated; Step 5 and later pending.** This repository contains instructions and templates, not an executable orchestration service. Quality thresholds and resource budgets must be calibrated for each project. Token accounting depends on the host's telemetry.

## Start a new project

Create a new repository from this template using GitHub's **Use this template** button, then open that project's checkout in your agent environment. Keep project-specific work in the new repository so this starter stays reusable.

Paste this prompt:

> Use this repository's AGENTS.md and research-workflow.yaml to initialize my research project. My topic is [topic], my desired output is [output], and my deadline is [deadline]. Ask me the unanswered calibration questions in templates/project-brief.md as multiple-choice questions one at a time, record the answers, and draft the first stage contract. Use separate producer and verifier agents when supported. Do not begin substantive research until the initial contract is agreed.

To adopt the workflow in an existing project, copy research-workflow.yaml, docs/, and templates/ into it, and merge the relevant instructions from AGENTS.md with its existing instructions. Do not overwrite project instructions. Alternatively, provide an assistant with this repository URL and explicitly ask it to read the files; a URL alone does not load or execute the workflow.

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

Step 1: define and select a specific research question → Step 2: detailed methodology → Step 3: implementation preparation and bounded end-to-end validation → Step 4: formal execution and prespecified analyses → Step 5 onward to be calibrated.

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

Step 1 goal handling, entry routing, budgets, evidence policy, decision authority, and next-stage authorization are calibrated. Concrete budgets remain project-specific and require approval. The numeric iteration/checkpoint defaults remain proposals. Step 2 comparison, limited tests, independent review, protocol gates, checkpoints, fallback and repair rules are calibrated. Step 3 batching, reuse, resource monitoring and pause/recovery rules are calibrated. Step 4 protocol-bound execution, tiered review, interpretation boundaries and unresolved-issue handling are calibrated. Step 5 and later remain open.

## Step 2 templates

- [Method comparison](templates/method-comparison.md)
- [Bounded pilot or technical trial](templates/pilot-check.md)
- [Decision summary and execution-ready protocol](templates/research-protocol.md)

A material unresolved design choice blocks protocol-ready status. Transparent uncertainty in a Step 1 decision brief does not waive this Step 2 requirement.

## Step 3 templates and reuse

Use [Step 3 plan](templates/step-3-plan.yaml) and [validation report](templates/step-3-report.md). Step 2 finalizes the protocol; Step 3 checks implementation. Reuse valid evidence and pilot artifacts; only new gaps or invalidated portions need checks. These documents specify monitoring requirements; they do not implement a realtime resource controller.

## Step 4 templates

Use [formal execution and review plan](templates/step-4-plan.yaml) and [results package](templates/step-4-results.md). Execution completion, per-result verification and authorization to proceed are distinct. Reuse valid evidence; do not repeat checks merely because the stage changed.
