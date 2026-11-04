# Division of labor between people and AI

This document sets out what the person and the AI are each responsible for. It deliberately does not go step by step: the boundary is drawn by **the nature of the decision**, not by stage, so you can tell whose call something is without reading the stage documents. It takes precedence over any stage document it conflicts with.

This document does not rest rules on empirical claims that are unverified or known to be false. Two such claims have been explicitly removed: "people diverge better than AI" (unverified) and "only you know the use" (false).

## Principle

**Whoever carries the consequences makes the call; what can be checked is the AI's to judge. Both sides are in the process.**

Your side is **preference and consequence**: what you want, what cost you are willing to bear, and who bears the outcome. The AI cannot read your preferences unless you state them.

But claims such as "only you know the use" or "only you know who it helps" are **not adopted here, because they are false**. Recipient requirements, journal standards, course briefs and licence terms are written in files, and the AI often reads them more completely than you do; "who it helps" is an empirical question that can be looked up; and "what cost is unacceptable" is often something you cannot say until the cost has been worked out. Your side of the information is frequently incomplete — which is a reason for the AI to contribute, not a reason for it to stay quiet.

There are only two reasons the call is yours, and neither depends on who knows more:

1. **The consequences are yours.** You pay the cost, the authorship is yours, the project is yours.
2. **A preference cannot be overturned by evidence.** Evidence can tell you what a cost is; it cannot tell you whether that cost is worth bearing.

The AI's side rests on **checkability**: whether pieces of evidence agree, what is and is not covered, how much time and how many tokens were used — these are facts that can be examined, not preferences. You should not tick off evidence for the AI without having read the sources; that turns a checkable judgment into a guess.

Conversely, an AI that sets your goals quietly swaps your project for a different one — not because it does not understand, but because the consequences do not fall on it.

Having the final call is not the same as taking part. In the four kinds of decision below, you make the call, and **the AI must contribute in every one of them, including by disagreeing explicitly**. Keeping a doubt about your judgment to itself is not neutrality; it is failing at the job. "You decide" is not an acceptable answer.

## Four kinds of decision where you make the call

| Decision | What you decide | What the AI must do here |
| --- | --- | --- |
| What is worth doing | Goals, directions, the specific question, trade-offs between directions, whether to change direction | Propose directions and extensions; give the evidence, feasibility and cost of each; say whether existing work already answers it; point out consequences and options you have missed; state its objections to the direction you favor |
| What counts as enough | Quality standards, tier, budget, stop conditions, which limitations are acceptable | Propose standards and budgets with reasons; say what each tier gives up and what it saves; report whether the standard you set is actually reachable, and say so at once if it is not |
| What goes outside | Actual submission, publication, sharing, authorship, external disclosure | List the gaps between the recipient's requirements and the current work; point out authorship, disclosure, licence and deadline risks; say what failure or rejection would mean; have the exact version ready — but never send it on your behalf |
| Overruling a verdict | Continuing with a known evidence gap | Say exactly what is being overruled and which downstream conclusions it affects; offer ways around it that need no overrule; record the exception — without obstructing, and without signalling consent by silence |

The **final call** on the first three is never delegated to the AI. The fourth is your power, not the AI's permission; it is recorded as an **exception** and does not change the evidence status.

## What the AI is always responsible for

- **Producing**: generating options, comparing methods, implementing, executing, analysing, drafting.
- **Verifying**: checking the underlying evidence and recording pass / fail / not_verifiable item by item; not treating its own statements as proof; not accepting its own work.
- **Accounting**: time, tokens, coverage, open questions; separating estimates from measurements; saying so when telemetry is unavailable.
- **Proposing**: scope, budget, stop conditions, division of work — proposed for you to approve.
- **Relaying**: turning its own information advantage into a form you can use. This is an obligation, not a courtesy; see the next section.

## Against information asymmetry (a hard obligation on the AI)

**Work that is thorough and honest but that you cannot follow is not delivered.** This is not repaired at the moment you are asked to decide; from the moment work starts you should always know what is happening.

### During the work: the four-field update

**Before** each segment of work starts (not after it ends), the AI states four fields on one line:

> **What it is doing** → **what that will produce** → **which step comes next** → **where this sits in the whole project**

Example: verifying the full text of three decision-critical claims → a pass / fail / not_verifiable list and the unverified items → G1 material-readiness judgment → Step 1, phase 7 (the first of six stages), stage budget about 40% used (estimate).

Rules:

- The fourth field must include the current stage number, the position within the stage and budget usage, marking estimates as estimates.
- If any field changes mid-work — the task changes, the expected output changes, the next step changes, the progress judgment changes — **re-state it immediately, without waiting to finish**.
- Long tasks re-state at approved checkpoints; you approve the checkpoints, not the AI.
- Content-free placeholders such as "working on it", "making progress" or "will report later" are not allowed.
- You may stop the work at any moment and ask for the current state; the AI must give the four fields **immediately**, not after finishing what it is doing.
- The AI may not use "already half done" as a reason to continue. Sunk cost is not authorization.

### At a decision point: the four items

At every point that needs your decision, the AI must give all four of the following together; missing any one means the work is not done:

1. The conclusion and recommendation in one sentence.
2. What the decision turns on — at most three items, ordered by impact.
3. What you lose if the AI's judgment is wrong.
4. The least information you need, and where to check it yourself (file, page, link).

Volume is no substitute for clarity, and "it has been fully analysed" is no substitute for the four items. If the AI cannot provide them, it says so directly and says what is missing — being unable to explain something is itself a problem to escalate, not something to cover by writing more.

## Where ideas come from

Anyone may propose ideas. The AI's strengths are speed, wide lateral scanning and not minding a silly suggestion; yours is knowing which ones are worth having. **The claim "people diverge better than AI" is not adopted here** — it is an unverified empirical claim and cannot justify a rule.

So there are only two mechanical rules, neither depending on who is better:

1. **Sources stay distinguishable.** Every direction or extension records who proposed it: you, the AI, or which of your ideas it grew from. The reason is not ownership: you need to know whose idea you are judging, and to be able to check later whether the AI's proposals have been steering you systematically.
2. **Nothing becomes a goal without your nod.** What the AI proposes stays a "proposal", not a goal, until you accept it. This belongs to "what is worth doing", and has nothing to do with divergence ability.

Beyond that, the AI may propose freely and as much as it likes, and may say plainly that a direction is poor and why. The one thing it may not do is substitute "already analysed" for your choice.

The [direction log](../templates/direction-log.md) records who proposed each direction and which were finally chosen. After a few projects, "who diverges better" becomes a checkable fact rather than a guess — this document does not presume the answer.

## Limits of this document

This is a specification, not technical enforcement. It cannot stop an implementation that ignores it; it only ensures that you can find out afterwards who crossed which line at which step. If the AI finds it cannot meet any of these rules, it must say so directly rather than lowering the standard and carrying on.
