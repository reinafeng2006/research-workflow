# Agent roles and project specialists

Status: new in v0.9.4. **This is an unverified default design**: the claim that dividing work by project specialty yields more valuable directions than generic roles has not been tested on a real project; see section 6. Who makes the call between people and AI is governed by the [Division of labor](division-of-labor.md).

## 1. Two layers

Agents are distinguished by **specialty** — what they look at, what they may read, what they deliver — not by personality. Specialty changes the content of ideas; personality mostly changes how they are phrased.

### Fixed functions: the same in every project

| Function | What it does | Why it is fixed |
| --- | --- | --- |
| Coordinator | Contracts, division of work, dependencies, budget, stage transitions; the four-field update | Keeps the whole consistent |
| Producer | Generates options, implements, executes, analyses, drafts, and self-checks | Owns substantive output |
| Independent verifier | Checks the underlying evidence and records pass / fail / not_verifiable item by item | Gate G2 requires that it took no part in producing what it verifies |
| Challenger | Checks assumptions, counterexamples and competing explanations; **looks for angles no specialist covers**; checks for convergence every roundtable round | A dedicated opposing voice cannot depend on a project happening to include that viewpoint; **always present, never enabled on demand** |

This layer does not vary by project because its reasons are structural, independent of the field. Independence rules are in [Shared controls](shared-controls.md) section 6.

**What counts as an "independent instance"**: a separate call or a separate agent that receives only the artifact under verification and the underlying evidence, and cannot see how it was produced (the conversation, drafts, the producer's reasoning). The same conversation under a different role name does not count. Where the environment cannot provide this, G2 can only be recorded as a human-approved exception, never as a pass.

### Project specialists: configured per project and per stage

These replace the vague "methods specialist (as needed)". They may differ by project and by stage: Step 1 may need a domain lens, Step 2 a methods and statistics lens, Step 5 a target-audience lens.

## 2. Two axes: discipline lens × research function

A concrete specialist = **discipline lens × research function**, combined as needed. For example "psychometrics" (psychology × measurement), "econometric identification" (economics × research design), "textual criticism" (literature × sources and texts).

- The **discipline lens** supplies that discipline's own knowledge, conventions and recognized difficulties. The same word "measurement" means psychometric validity in psychology, instrument calibration in physics, and identification in economics.
- The **research function** supplies the kind of work every discipline has to do, and ensures nothing is missed.

### Discipline lens

- **Home discipline**: existing work, field conventions and recognized difficulties.
- **Near and far disciplines**: used specifically for divergence. The most valuable extension questions often come from borrowing a framework from a neighbouring discipline; during divergence they can be assigned operators, asking "how would this discipline look at the problem?" (see [Divergence and appraisal](divergence-and-appraisal.md) section 1).

**This document does not invent its own list of disciplines.** It adopts the Fields of Research and Development (FORD) classification in chapter 3 of the OECD Frascati Manual 2015. The classification is content-based, with 6 broad fields and 42 sub-fields. Go through it field by field to decide where the home discipline sits and where the near and far ones are.

> Verification status (2026-11-04):
> - **Verified**: the source is OECD (2015), Frascati Manual 2015, chapter 3 (ISBN 978-92-6423880-0); level 1 "broad field" has 6 items and level 2 "sub-field" has 42; the approach is primarily content-based; one broad field is "engineering and technology". Source: the [United Nations Statistics Division classification registry](https://unstats.un.org/unsd/classifications/Family/Detail/1039), an official registry restating the manual, not the manual itself.
> - **Not verified**: the other five broad fields and the names of the 42 sub-fields. The registry does not list them, the relevant UNESCO pages no longer exist, and the OECD site refuses automated access. They are commonly given as natural sciences, engineering and technology, medical and health sciences, agricultural sciences, social sciences, and humanities and the arts, but they are not treated as confirmed until checked against the manual.

### Research function

Grouped by type of research, so that not all research is assumed to be quantitative and empirical. This is a working checklist for finding gaps and **does not claim to be complete**; a derived specialist that is not on it is perfectly acceptable.

| Applies to | Function | Main concerns | Typical stages |
| --- | --- | --- | --- |
| All research | Literature and novelty | Whether the question has been answered; the nearest neighbouring work | 1 |
| All research | Research design | The overall construction of the study or argument: controls, bias, comparability, or the structure of the argument | 1, 2 |
| All research | Ethics and permissions | Subjects, informed consent, compliance, rights to use materials, potential harm | 1, 2, 6 |
| All research | Audience and use | Who will use the answer, how, and how they might misread it | 1, 5 |
| All research | Delivery and recipient | Format, channel, deadline, acceptance requirements | 5, 6 |
| Quantitative empirical | Measurement | How the outcome is measured; validity and reliability | 1, 2 |
| Quantitative empirical | Statistics and inference | Sample, effect size, multiple comparisons, uncertainty | 2, 4 |
| Quantitative empirical | Data and access | Sources, licences, availability, quality, held-out data | 1, 2, 3 |
| Qualitative | Interviews, observation and coding | Sampling logic, coding scheme, saturation, credibility | 2, 4 |
| Qualitative | Positionality and reflexivity | How the researcher's position shapes the material and its reading | 2, 5 |
| Theoretical and formal | Definitions, proofs and counterexamples | Whether concepts are well defined, proofs complete, edge cases covered | 2, 4 |
| Theoretical and formal | Model construction | Whether assumptions are necessary; how conclusions depend on them | 1, 2 |
| Sources and texts | Source criticism and editions | Reliability of sources, differences between versions, completeness of archives | 1, 2, 4 |
| Sources and texts | Interpretation | Whether a reading is supported by the text; competing readings | 4, 5 |
| Building and engineering | Implementation and reproducibility | Code, environment, compute and cost, whether others can reproduce it | 3, 4 |
| Building and engineering | Benchmarks and evaluation | Whether comparisons are fair; whether the evaluation measures what it means to | 2, 4 |

## 3. How specialists are chosen

1. **Derive.** The AI derives specialists from two sources and states which one each came from. The two sources are available at different times: the parts of the research question exist from the start and are used for divergence specialists; sensitivity exists only once the appraisal matrix has been scored and is used for the specialists who watch sensitive points during verification.
   - The parts of the research question: subject, outcome measure, contrast, boundaries, the decision it should inform. For example, "outcome measure" calls for a measurement lens, "the decision it should inform" for a user's lens.
   - The sensitivity of the [appraisal matrix](../templates/appraisal-matrix.md): assign specialists to the few scores or assumptions the recommendation depends on most. Specialists are spent where the project is most uncertain, not spread evenly.
2. **Check each axis for gaps.** Discipline axis: go through the FORD broad fields one by one to identify the home, near and far disciplines. Function axis: first decide which types of research the project involves, then go through "all research" and the functions for those types one by one. Mark each "needed", "not needed", or "not needed, because…".
3. **You approve the list, in two steps.** In Step 1: divergence specialists are approved before phase 2 with the "divergence scope, budget and specialists" authorization point; specialists watching sensitive points are approved after phase 6 and before phase 7 at the "sensitivity specialists" authorization point. Later adjustments are approved in each stage's start authorization.
4. **Number**: 2–4 specialists per stage, of which at most one home-discipline lens and one or two near or far lenses. This is a proposal, adjusted per project.

## 4. Each specialist states four things

| Item | Example: psychometrics (psychology × measurement) |
| --- | --- |
| Looks at | Validity and reliability of the scale; whether the measure is equivalent across all participants |
| May read | Protocol, scale documentation, analysis plan; no interim results it is not authorized to see |
| Delivers | A list of measurement risks for each candidate direction or design, pointing back to base items in the appraisal matrix |
| Must not | Set thresholds for you; accept a measurement plan it helped design |

General constraints:

- A specialist that took part in producing an artifact may not independently accept it — the independence rules apply to specialists too.
- Specialists change neither the evidence rules nor who makes the call. **What an AI says from a discipline's point of view is not evidence**: judgments such as "from an economics point of view…" still need direct sources under the [Step 1](step-1.md) evidence rules. How well one model can simulate a discipline's point of view is unverified.
- In the direction log, directions proposed by the AI name **which specialist** proposed them, for later comparison.

## 5. Personality is an optional presentation layer

Names, avatars and tone of voice may be added on top of a specialty for the interface. Rules:

- Personality does not change the four things a specialist states.
- The interface must say whether the mates are the same model. One model playing several roles is not several independent viewpoints, and "several mates agree" is not evidence.
- Whether personality increases the diversity of ideas, or users' willingness to take part in discussion, is **unverified**.

## 6. Unverified parts

- Whether dividing work by specialty yields more directions you want to keep than generic roles do.
- Whether assigning specialists by sensitivity makes the AI watch only known risks and miss unknown ones. The challenger's duty to find uncovered angles is the countermeasure for this risk, and is itself unverified.
- Whether 2–4 per stage is the right number.
- How well one model can simulate a discipline's point of view; whether near and far discipline lenses actually produce usable new directions.

The direction log records which specialist proposed each direction and whether it was finally chosen. After a few projects this can be compared; until then, this document is followed as a default design, not treated as a proven conclusion.
