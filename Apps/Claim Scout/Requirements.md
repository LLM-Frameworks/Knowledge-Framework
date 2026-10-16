# Claim Scout — Requirements

**Version:** 0.4  
**Status:** Approved by Steward (2026-10-15). In force for this tree.  
**Note:** Personal pilot details belong in Settings/, not in shipped requirements.

Each requirement has an ID, plain wording, and a test.

---

## R1 — Simple to use (headline requirement)

A veteran with no prior knowledge of the system can upload records and get a useful first output in a single session, guided only by the tool itself. No manual, no tutorial, no prior reading.

- **Test:** hand the system to someone who has never seen it. If they stall, the system failed — not the user.

## R2 — Guided first, power on demand

The guided intake (`walk me through it`) is the default path. Power commands exist for experienced users but are never required to get value.

- **Test:** every capability reachable by a power command is also reachable through the guided path.

## R3 — Plain language, always

No VA jargon, legal term, or acronym appears in output without a plain-English definition on first use in that output.

- **Test:** a non-veteran reader understands every output without looking anything up.

## R4 — No dead ends

Every output states three things: what was found, the single most useful next step, and what is missing. The user never has to ask "okay, so what now?"

## R5 — Missing records are named, never skipped

If records are absent, the output says which ones and why they matter — then proceeds with what exists. Silence about gaps is a defect.

## R6 — Tracker stays portable

Tracker.md remains a standalone, human-readable file that any person or any AI can use without the rest of the system. No feature may make the Tracker depend on tooling outside the file.

## R7 — Command economy

New capabilities must not add new commands unless they remove real ambiguity. Prefer fewer, clearer commands over more features. If two commands confuse users, merge them.

## R8 — Simplicity never overrides the firewall

Simple to use, never simple-minded. No-source-no-fact, the evidence tiers, the Finding vs. Attribution rule, and the Citation Confidence rule hold regardless of how simple the interface gets. If a simplification would weaken a guardrail, the simplification loses.

## R9 — Uncertainty is stated, not buried

Low confidence, conflicts, and unknowns appear in the output in plain words, at the point where they matter — not in a footnote, not omitted for cleanliness.

## R10 — Tracker governance takes effect only on Steward approval

Tracker rules, review protocol, and signed-entry conventions are inert until the Steward explicitly approves them.

## R11 — Recruit on pain, not politeness

User testing recruits veterans who already feel the problem — not polite favors.

## R12 — One tracker, not two

Claim Scout asks for the veteran's existing claim tracker at the start of a run and writes there. It never spawns a parallel tracker. When none exists, Tracker.md is generated on first run from the schema in START_HERE.md — never shipped or reused.

## R13 — VA decisions are opinions, not facts

A VA rating decision — including denial rationale and examiner opinion — is treated as an assertion to be tested, never as a finding of fact.
