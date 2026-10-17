# Roundtable — method

Multi-seat collaboration on **one** assignment. Public-safe. No privileged AI.

## Permanent seat

**Moderator** — stake keeper only. Does not win the argument for a domain side.

- Restates defeat/success condition
- Calls drift (nuance that never returns to the stake)
- Enforces epistemic tags and seat labels
- Declares stop conditions

## Cast

Task-defined. Examples:

| Pattern | Seats |
|---------|--------|
| Adversarial | Advocate · Red team · Moderator |
| Delivery | Money · Engineer · QC · Moderator |
| Org | HR · Money · Ops · Moderator |

Each seat speaks only from its lens. Cross-talk allowed; quiet goal-changes are not.

## How each AI knows its job

Seat assignment is on the **task card**, not implied by model name.

Each participant receives:

1. Shared block — goal, defeat/success condition, constraints, full cast list, output rules
2. Seat block — `You are: [seat]`, lens, forbiddens
3. Context — transcript slice and/or current artifact

## Rounds

Unbounded. Progress rule: each turn must affirm, deny, or revise the defeat/success condition, or answer a direct challenge to a prior warrant.

**Stop when any one holds:**

1. Convergence on the stake outcome
2. Clean deadlock (disagreement named; warrants visible; nothing new moves the stake)
3. Formal revision of defeat/success condition + re-baseline
4. Steward interrupt
5. Moderator has called repeated drift without return to stake → force summary and pause

## Output

Labeled by seat. Tagged claims. Proposal/fuel only — Steward promotes or rejects.

Suggested layout for a run:

```text
Developer/Roundtable/runs/<task-slug>/
  task.md
  transcript.md
  artifact.md
```

## Forbidden

- Unlabeled consensus that hides disagreement
- Moderator acting as a domain advocate
- Auto-publish to References or Apps
- Treating model brand as a seat
