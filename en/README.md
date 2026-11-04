# Research workflow

English reference of the [authoritative Chinese README.md](../README.md). Both versions express the same calibrated rules; see [language policy](docs/language-policy.md) and [translation manifest](../translation-manifest.json). Use the mirrored configuration, docs and templates together.

A reusable workflow for research and study projects: six stages, three gates per stage (material ready, independently verified, human authorization), budget-bounded revision, and an explicit division of labor between people and AI. Supports individual and group research.

**Before starting you need to read only two documents: this one and the [Division of labor](docs/division-of-labor.md).** The latter sets out what the person and the AI are each responsible for, and prevails over any other document it conflicts with. Read the rest as needed.

**Version v0.9.6**; Steps 1–6 are calibrated, and each project's budgets, standards and authorizations still need approval per project. The repository root holds the authoritative Chinese version.

This repository provides specifications and record templates; it is not an executable orchestration service or a real-time resource monitor.

## How to start

1. On GitHub, select **Use this template** to create a new project repository, and open it in an agent environment that can read project files. Keep project outputs in the new repository, separate from the template.
2. Add existing materials, or give accessible paths/links. You do not need to fill in templates by hand.
3. Paste the prompt below. The agent reads the materials, decides which stage to enter, and proposes a first plan; substantive research starts only after you approve it.

```text
Initialize a research project following this project's
en/docs/division-of-labor.md, en/AGENTS.md and en/research-workflow.yaml,
and read the specifications for the applicable stage.

My research topic/question: [fill in]
What I have so far: [broad idea / candidate questions / settled question / existing protocol or results]
What I hope the project delivers: [several goals allowed, no ranking needed; unsure is fine]
Existing materials: [file paths or links; otherwise "none"]
Known delivery requirements, deadlines and constraints: [fill in; leave blank if unknown]
Hard budget limit: [fill in if any; otherwise ask the agent to propose one]

First read the existing materials and record the workflow commit used. Decide the
entry stage from existing work, filling only missing prerequisites without starting
over. First state which independent verification, resource accounting, pausing and
saving capabilities the current environment supports. Then propose the scope,
expected outputs, tier, budget and stop conditions for the first segment of work as
one decision package for my approval.

Before each segment of work, tell me: what you are doing, what it will produce,
which step comes next, and where it sits in the whole project. Ask one
multiple-choice question at a time, only about what is still unclear. Do no
substantive research before the initial plan is approved.
```

The agent reads files only when it has access and an explicit instruction; sending a repository link alone does not start the workflow. Private repositories require connecting an account or providing a local copy.

**Existing projects**: copy `research-workflow.yaml`, `docs/` and `templates/`, and merge the rules in `AGENTS.md` into your existing instructions rather than overwriting them. English projects use the corresponding files under `en/` and adjust the paths in the prompt. Record the commit actually used, not just the README version number.

## What the runtime environment must add

Documents can set rules but cannot enforce them. The following must come from the runtime environment:

| Control | Defined by the repository | Runtime support still needed |
| --- | --- | --- |
| Independent verification | Authors do not accept their own artifacts | An independent agent or reviewer; the same agent switching roles does not count |
| Resource accounting | Aggregate the cost of every role, retry, repair and review | Token/cost telemetry; without it, only labelled estimates |
| Real-time pausing | Stop rules for rates, budgets, lack of progress and so on | Continuous monitoring, timeouts and cancellation; documents cannot interrupt a running call |
| Parallel budgets | Reserve before launch to avoid duplicate dispatch and overcommitment | A coordinator dispatching serially, or a shared budget record with atomic operations |
| Saving and recovery | Save outputs, versions and cumulative usage | Persistent storage; whether a running computation can resume depends on the implementation |
| Periodic maintenance | Authorization, duration, cumulative budget and renewal rules | A scheduler; copying the repository does not start any maintenance |

When a capability is missing, the agent says so first, then proposes alternatives (smaller batches, serial execution, human checkpoints, independent review) for your approval; when risk cannot reasonably be bounded, the corresponding task does not start.

## Six stages

1. [Define and select a research question](docs/step-1.md) — ends with your approval of a specific question.
2. [Method comparison and protocol](docs/step-2.md) — approving the protocol does not authorize implementation.
3. [Implementation readiness and small-scale end-to-end validation](docs/step-3.md) — passing validation does not start formal execution.
4. [Formal execution and prespecified analysis](docs/step-4.md) — negative and uncertain results are reported as they are.
5. [Synthesis and finalizing the deliverable](docs/step-5.md) — finalization does not authorize external release.
6. [Required delivery, archiving and closure](docs/step-6.md) — actual submission needs explicit authorization of the exact version and action.

## File index

**Rules**

- [Division of labor](docs/division-of-labor.md) — read this first.
- [Gates, tiers and runtime conditions](docs/gates.md) — three gates, three tiers `lite` / `standard` / `strict`, checklist mapping.
- [Divergence and appraisal](docs/divergence-and-appraisal.md) — how Step 1 finds directions and compares candidates.
- [Agent roles and project specialists](docs/agents.md) — fixed functions, specialists derived per project, specialty library.
- [Team research](docs/teamwork.md) — person roles, authorization matrix, work units, handover.
- [Shared controls](docs/shared-controls.md) — authorization reuse, check records, pre-launch budget, role independence, runtime controls.
- `AGENTS.md` (agent operating instructions), `research-workflow.yaml` (structured index), [language policy and terms](docs/language-policy.md), [calibration record](docs/calibration-decisions.md).

**Templates** (`templates/`)

- General: project brief, stage contract, decision brief, decision log, verification report, upstream review, evidence ledger (CSV), authorization record, check registry, task launch, role assignments, work assignment.
- Step 1: direction log, appraisal matrix.
- By stage: Step 2 method comparison, pilot check, research protocol; Steps 3–6 one plan and one report/delivery package each.

Each project creates `project/brief.md`, `project/stages/`, `project/reviews/`, `project/artifacts/` and `project/decisions.md`, and records the template commit used.
