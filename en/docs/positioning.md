# Product positioning and competitors

English reference of the [authoritative Chinese positioning.md](../../docs/positioning.md).

Status: decided by the user on 2026-11-04; see [calibration record](calibration-decisions.md) S18. This document is the basis for positioning, not a workflow rule. Everything under "possible differentiators" is a hypothesis still to be tested.

Evidence levels follow Step 1: **verified** (full text or original documents read directly), **abstract-level**, **inferred**, **unknown**.

## 1. Decisions

| Item | Content | Basis |
| --- | --- | --- |
| Project purpose | A product people actually use | User decision |
| First users | Undergraduate and master's students who must choose a research topic and lack domain expertise | User decision |
| Positioning | Upstream of the hypothesis, plus a human decision layer: turn a vague idea into a specific question that is worth doing and that the person can choose for themselves; downstream execution goes to existing pipelines such as NeuriCo | User adopted the AI's recommendation; basis in sections 2 and 3 |
| Steps 2–6 | Frozen, not deleted | See calibration record S18-03 |
| Next step | Run a concierge comparison test first, then decide whether to build the website | See [pilot/](../../pilot/README.md) |

## 2. Competitors

All five paper titles were checked on arXiv. Unless noted, the statements below were checked against the full text.

| Work | What it does | Relation to this workflow | Evidence level |
| --- | --- | --- | --- |
| IdeaSynth (arXiv 2410.04025, CHI 2025) | Breaks ideas into facets (problem, method, evaluation, and so on) on a canvas, with variants, combinations and literature-grounded feedback | Closest to Step 1. **Deliberately gives no evaluation scores** and offers actionable suggestions instead, because LLMs evaluate ideas inconsistently and human experts often disagree on novelty. Participants were PhD students and postdocs (lab study N=20, deployment study N=7) | Verified |
| Same work, user reactions | In the deployment study, 4 of 7 participants had concerns about the trustworthiness of LLM-generated content; one of them (D2) said explicitly they did not trust an LLM to evaluate novelty | Whether our scores and evidence levels help or burden novices must be tested | Verified; sample far too small to generalize |
| IRIS (arXiv 2504.16728) | Interactive ideation with Monte Carlo Tree Search (MCTS) expansion and LLM review as feedback | The authors report signs similar to "reward hacking" in ideation (fancy terminology and so on), mitigated by the researcher checking the feedback. They state that this relies on the assumption of "sufficient domain expertise of the researcher", which our first users do not have | Verified |
| ResearchAgent (arXiv 2404.07738) | Iterative idea generation over a literature graph, scored by LLM reviewing agents against criteria | Evaluation dimensions include feasibility | Verified |
| Chain of Ideas (arXiv 2410.13185) | Organizes idea development along chains of literature | Evaluation dimensions include feasibility | Verified |
| SciMON (arXiv 2305.14259) | Generates scientific inspiration optimized for novelty | No feasibility evaluation found by full-text search | Inferred (search found no match) |

**Common ground**: all of these systems target researchers who already have some domain knowledge; none targets novices without domain expertise choosing a topic. This rests on these five papers only, not the whole field (inferred).

## 3. Relation to NeuriCo

Basis: NeuriCo repository documents at commit 88d98e8 (`docs/HITL_AUTORESEARCH.md`, `docs/ARCHITECTURE_AND_ROADMAP.md`). The documents were read but the system was not run (documents verified; features not tested).

- NeuriCo already **enforces** at runtime much of what we only specify: an authority table for the human, manager, worker and runtime; workers cannot advance their own phase; a sealed scorer; checkpoints and recovery.
- Its "independent ranked" mode isolates proposers from each other, the opposite of our full roundtable, which makes it a useful contrast.
- Its open research questions 4 (how to structure outputs for human decisions and present multiple directions with trade-offs) and 5 (exploration diversity versus reliability) are exactly where Step 1 focuses.
- Conclusion: downstream execution need not be rebuilt, and Step 1's output could be its input. Whether the two can actually connect, and whether the NeuriCo team is interested, is **unknown**; contacting them is an outward action for the user to decide.

## 4. Possible differentiators (all untested)

1. Clarify goals before diverging on directions.
2. Traceable scores, used only to support human decisions, never as an automatic search reward.
3. Designed for novices without domain expertise.
4. Every claim carries an evidence level.
5. Output can be handed to pipelines such as NeuriCo.

Item 2 is the opposite of IdeaSynth's choice and carries the most risk: novices may not understand the scores, may distrust them, or may trust them too much. The pilot's measures of understanding and trust exist for this item.

## 5. Not yet checked

- Only five papers and one repository were checked; commercial products (such as AI topic-selection tools for students) were not searched systematically.
- The content of "Qirun's proposal", mentioned in the external assessment, is unknown.
- There is no data on what first users currently use to choose topics; the pilot's background questions ask.
