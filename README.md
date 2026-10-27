# Research workflow

A reusable starter for research and study projects driven by multiple agents, fixed stage objectives, independent verification, and budget-aware upstream review.

**Status: v0.1 design draft.** This repository contains instructions and templates, not an executable orchestration service. Quality thresholds and resource budgets must be calibrated for each project. Token accounting depends on the host's telemetry.

## Start a new project

Create a new repository from this template using GitHub's **Use this template** button, then open that project's checkout in your agent environment. Keep project-specific work in the new repository so this starter stays reusable.

Paste this prompt:

> Use this repository's AGENTS.md and research-workflow.yaml to initialize my research project. My topic is [topic], my desired output is [output], and my deadline is [deadline]. Ask me the calibration questions in templates/project-brief.md, record the answers, and draft the first stage contract. Use separate producer and verifier agents when supported. Do not begin substantive research until the initial contract is agreed.

To adopt the workflow in an existing project, copy research-workflow.yaml and templates/ into it, and merge the relevant instructions from AGENTS.md with its existing instructions. Do not overwrite project instructions. Alternatively, provide an assistant with this repository URL and explicitly ask it to read the files; a URL alone does not load or execute the workflow.

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

Framing → evidence → method → execution → synthesis.

Within each stage: produce → self-check → independent verification → diagnose → revise → verify again. Advance only when all mandatory criteria pass and no critical or major defects remain. A rigorous negative or inconclusive result may pass.

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

Research domain, human approval checkpoints, challenger frequency, concrete budgets, and any preauthorized reserve remain to be agreed. Draft defaults do not imply prior user approval.
