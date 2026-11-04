# Divergence and appraisal (Step 1)

Status: new in v0.9.2, used in [Step 1](step-1.md) phases 2–4 (divergence: generating, selecting and refining directions) and phase 6 (appraising candidates). The [Division of labor](division-of-labor.md) governs who does what: anyone may propose ideas, sources stay distinguishable, and nothing becomes a goal without your nod.

The operators, extension types, scoring dimensions and decision thresholds here are **working checklists and proposals**, not validated theory. This document does not claim they exhaust the possible directions, nor that the thresholds are calibrated.

## 1. Divergence: two axes

The two axes differ in their **starting point**: lateral starts from your current idea and looks for other directions; vertical starts from a direction already chosen and looks for its next question.

### Lateral: eight operators

Using "does step-by-step prompting raise accuracy on maths items?" as the example:

| Operator | Question | Example |
| --- | --- | --- |
| Change the subject | Does it hold for another population, system or material? | From frontier models to small models |
| Change the outcome | What if you measure something else? | From accuracy to the distribution of error types |
| Change the contrast | What if you compare with something else? | Step-by-step vs worked examples, not step-by-step vs direct answers |
| Change the scale | A different time span, size or granularity? | From per-item accuracy to ranking on a whole exam |
| Change the level of mechanism | From "does it work" to "why does it work", or back? | Which step in the chain is doing the work |
| Invert an assumption | Turn the default premise around? | When does step-by-step prompting hurt? |
| Move the boundary | Widen or narrow the scope and exclusions? | Drop the "no items with figures" restriction |
| Change the use and audience | For the same phenomenon, who would use the answer? | From an evaluation team to maths teachers |

### Vertical: five extension types

| Extension | Question |
| --- | --- |
| Upstream (mechanism) | Why does this happen? |
| Downstream (consequence) | So what? Who would act differently? |
| Boundary (failure) | Under what conditions does it stop holding? |
| Generalization | Does it hold for other subjects or settings? |
| Method redo | Can a stronger design answer the same question again? |

The axes overlap ("generalization" resembles "change the subject"). Record the starting point clearly; there is no need to force the distinction.

Operators say which way to change; what to change it into often comes from another discipline. An approved near or far discipline lens (see [Agent roles and project specialists](agents.md) section 2) can be assigned to an operator, asking "how would this discipline look at the problem?"

## 2. Coverage: account for each item, do not count

There is no target number of directions. What is required is that **every operator and every extension type is accounted for**: which directions it produced; tried without producing a useful direction; or not tried, and why it does not apply.

"Tried without result" is recorded too, because it is information: that part of the space may already be occupied, or the question may be insensitive along that axis. Check the two axes separately.

## 3. Substantive difference

Two directions are substantively different if and only if at least one of the following differs: the subject of study, the outcome measure, the contrast, or the decision the answer can inform. Rewording or a small adjustment of scope does not count.

The AI proposes the judgment and you confirm it. Directions judged duplicates are merged, not deleted, with a record of which one they were merged into.

## 4. Provenance and record

Every direction is recorded in the [direction log](../templates/direction-log.md):

- **Proposer**: you, the AI, or derived from another direction (for example "derived from D3"). What the AI proposes stays a "proposal" until you accept it.
- **Which axis, and which operator or extension type**.
- **Status**: candidate, selected, deferred, dropped.
- **The reason for dropping or deferring**. Dropped directions are not deleted, so the next session does not regenerate the same thing and a wrongly dropped direction can be recovered.

After a few projects, the log can also answer "who proposed which directions, and which were finally chosen" — without presuming the answer.

## 5. Appraisal: the argument base first, scores only for ranking

All candidates use the [appraisal matrix](../templates/appraisal-matrix.md), answering **the same questions on the same dimensions**.

### 5.1 Argument base (required)

| ID | Question |
| --- | --- |
| A1 | If it succeeds, what is the most it can establish? |
| A2 | What can it not establish? What is the most common over-reading? |
| A3 | Which assumptions does it depend on? List at most the three most important. |
| A4 | What happens if those assumptions fail? |
| A5 | Competing explanations: what else could produce the same result? |
| A6 | Drop condition: what would make you abandon this direction? **Written beforehand, not added afterwards.** |
| A7 | Has existing work already answered it? With sources and evidence level. |
| A8 | Relation to the accepted goals. |

Where the base cannot answer an item, write "unknown" and what is missing; do not leave it blank or fill it with generalities.

### 5.2 Scores

Seven dimensions scored 0–5: significance, novelty, answerability, data and access, method readiness, budget fit, ethics and risk.

**Anchors** (2 and 4 fall in between):

- 0: definitely not feasible
- 1: a known hard obstacle
- 3: no known obstacle, but not verified
- 5: supported by direct evidence

**Every score must carry two things; missing either makes it invalid, and it takes no part in ranking**:

1. **A pointer to the base**: which base items the score rests on (for example "answerability 4 ← A1, A3").
2. **An evidence level**: verified, abstract-level, inferred, unknown.

**Comparability**: all candidates use the same dimensions and anchors. If a dimension does not apply to a candidate, state why; do not score only some candidates.

**No weighted total.** Any weighting is a claim nobody has verified, and it hides the trade-offs inside one number. Ranking follows the rules below; the mean is for reference only.

### 5.3 Decision rules

Check in order; stop at the first that applies:

| Condition | Verdict | Meaning |
| --- | --- | --- |
| Answerability or data and access < 2 | De-risk first | Propose an approved small feasibility check; do not go straight to design |
| Ethics and risk < 2 | Settle ethics and permissions first | Clarify consent, use boundaries and potential harm before investing |
| Significance + novelty < 4 | Reframe the question | Go back to divergence; change the angle, not the budget |
| Budget fit < 2 | Narrow the scope or rebudget | |
| Every dimension ≥ 3 and mean ≥ 3.6 | Ready to take for approval | Hand it to you to decide |
| None of the above | Defer and list what is open | No hard block, but not solid enough yet |

These thresholds are proposals. You may change them; changes go in the decision log, and every candidate is re-judged under the changed thresholds, not just one.

### 5.4 Sensitivity

For the one to three scores or assumptions that most affect the recommendation, state: **if it were two points lower, or the assumption failed, what would the verdict become?** When a candidate's verdict flips at a touch, say so when handing it to you.

## 6. Who does what

**AI**: generates directions along both axes and records their source; proposes substantive-difference judgments; fills in the base, scores, points every score back to the base with an evidence level; works out the sensitivity; states its objections to the direction you favor.

**You**: propose your own ideas; confirm substantive-difference judgments; accept or reject the AI's directions; choose the directions to pursue; change decision thresholds; decide whether to combine.

When something is handed to you for decision, the AI gives the four items under the [Division of labor](division-of-labor.md): one-sentence conclusion and recommendation, what it turns on, what you lose if it is wrong, and the least necessary information with where to check it.

## 7. Relation to the gates

Two requirements can block Step 1 readiness, in all three tiers:

- **Divergence coverage accounted for** (sections 2–4) is a G1 checklist item: if the coverage table has a blank row, G1 does not pass.
- **Appraisal comparable and scores traceable** (section 5) is a G2 checklist item: if any score used in ranking does not point back to the base or lacks an evidence level, G2 does not pass.

Counts are in [Gates, tiers and runtime conditions](gates.md) section 7.

## 8. Roundtable

Status: new in v0.9.5, **an unverified default design**. Used for now only in Step 1 divergence (phases 2–4).

The user chose a **full roundtable**: the approved [project specialists](agents.md) think about directions together in one discussion from the start, building on each other.

**The roundtable starts from your question.** Before round one, every mate at the table shares the same starting point: the topic, candidate question or settled question you brought, together with the goals and boundaries already accepted in the project brief. This follows from how Step 1 is entered, not from a hypothesis about who should speak first. The benefit is that everyone is aligned on the same question — when mates diverge separately, each may misread the question, and the output looks diverse when it is really a mismatch in understanding.

**Align on the question and the goals; diverge on directions.** When a mate reads the question differently from you, it raises this for you to clarify and may not rewrite the question; rewriting the question is a "what is worth doing" decision, and it is yours.

Known risk: in one conversation, later speakers tend to follow earlier ones, the directions converge, and the convergence looks natural and is hard to notice. The three countermeasures below do not change the full-roundtable form; they make convergence visible:

1. **Speaking order rotates every round**, so no mate always sets the tone.
2. **Every mate proposes at least one direction per round using its assigned operators**, so the lateral coverage of section 1 is not steered away by the discussion. Near and far discipline lenses are assigned operators too.
3. **The challenger checks for convergence every round**: using the four criteria of section 3, it judges whether new directions are substantively different from existing ones. When most new directions in a round are not substantively different, it reports "this round converged" and the mates switch operators.

During the discussion, mates challenge each other, merge duplicates by section 3, and grow next questions along the five extension types. Each direction records "proposed by which mate, in which round, derived from which direction". The challenger also looks for angles no specialist covers. Once the coverage table is complete, you choose the directions (G3).

Rules:

- **The verifier does not sit at the table.** Gate G2 requires that it took no part in producing what it verifies.
- You may interject, add directions or veto any of them at any time. The roundtable does not choose directions for you and does not force consensus. Besides the question itself, you may write down directions you already have before round one (optional).
- The interface must say whether the mates are the same model. **Agreement among mates is not evidence, and does not mean you agree.**
- Rounds and budget are approved together with the divergence budget before Step 1 brainstorming; when reached, the roundtable stops and moves to your choice.
- The four-field update applies as usual: before each round, say what it is doing, what it will produce, which step comes next, and where this sits in the whole project.

Unverified: whether the three countermeasures are enough to prevent convergence; whether a full roundtable yields more directions you want to keep than separate divergence does; the token cost per round. The "produced in" column of the direction log and the challenger's convergence reports are there for later comparison.
