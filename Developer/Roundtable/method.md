# Roundtable — method

Multi-seat collaboration on **one** assignment. Public-safe. No privileged AI.

Can run as a light multi-seat table **or** as a court-style proceeding (below). Same Moderator, same stake rules.

## Permanent seat

**Moderator** — stake keeper only. Does not win the argument for a domain side.

- Restates defeat/success condition
- Calls drift (nuance that never returns to the stake)
- Enforces epistemic tags, seat labels, and **phase** discipline
- Declares end of phase and stop conditions
- Does not invent extra rounds — only Steward authorizes rounds beyond the default sequence

Default session pattern: the model that co-authors the task card with the Steward often takes Moderator for that run (Steward confirms).

## Cast

Task-defined. **Handle = model id** (`grok`, `claude`, `muse`, …). Role ≠ model.

| Pattern | Seats |
|---------|--------|
| Adversarial | Advocate · Red team · Moderator |
| Delivery | Money · Engineer · QC · Moderator |
| Org | HR · Money · Ops · Moderator |
| Court-style | Same as above; phases control *when* they speak |

Each seat speaks only from its lens. Quiet goal-changes are not allowed.

## How each AI knows its job

Seat assignment is on the **task card**, not implied by model name.

Each participant receives:

1. Shared block — goal, defeat/success condition, constraints, full cast list, **current phase**, output rules
2. Seat block — `You are: [seat]`, lens, forbiddens
3. Context — what the phase allows (see below)

## Court-style phases (default sequence)

### Phase 1 — Discovery (in writing)

- Each seat files **written** evidence, reasoning, and warrants — no oral back-and-forth yet.
- Prefer parallel filings (no seat sees another’s Discovery until the phase closes), unless the Steward orders shared Discovery.
- Moderator checks: labeled, tagged, on-stake; rejects unsigned dumps and untagged factual claims.
- Output path: `runs/<task-slug>/discovery/<seat>.md` (or one `discovery.md` with clear seat headers).

### Phase 2 — Presentation

- Each seat states its case from its Discovery filing (and only from what was filed, plus task card).
- Still mapped to the defeat/success condition.
- Moderator keeps order and timebox if the Steward set one.

### Phase 3 — Rebuttal

- Seats answer opposing Presentation points.
- New evidence only if the Moderator allows a narrow add (or Steward so orders); default is argue from the Discovery record.

### Further rounds

- **Not automatic.** After Rebuttal, Moderator summarizes stake positions and stop-condition status.
- **Additional rounds only if the Steward authorizes** (e.g. second rebuttal, focused question, or limited new Discovery on one issue).
- Authorization is explicit: “one more rebuttal on X” / “reopen Discovery for Y only.”

## Stop conditions (any one)

1. Convergence on the stake outcome  
2. Clean deadlock (disagreement named; warrants visible; nothing new moves the stake)  
3. Formal revision of defeat/success condition + re-baseline  
4. Steward interrupt  
5. Repeated drift without return to stake → Moderator forces summary and pause  

Progress rule within a phase: each filing or turn must affirm, deny, or revise the defeat/success condition, or answer a direct challenge to a prior warrant.

## Output

Labeled by seat and phase. Tagged claims. Proposal/fuel only — Steward promotes or rejects.

```text
Developer/Roundtable/runs/<task-slug>/
  task.md
  discovery/          # Phase 1 filings
  presentation.md     # Phase 2 (or per-seat files)
  rebuttal.md         # Phase 3
  transcript.md       # optional running log
  artifact.md         # joint product if any
  moderator.md        # phase calls, drift, stop checks
```

## Forbidden

- Unlabeled consensus that hides disagreement
- Moderator acting as a domain advocate
- Skipping Discovery when the task card says court-style
- Auto-starting extra rounds without Steward word
- Auto-publish to References or Apps
- Treating model brand as a seat
