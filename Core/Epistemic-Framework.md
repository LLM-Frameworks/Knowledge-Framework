# Epistemic Framework

**Core rule**  
The framework only works if the four tags are defined by binary, checkable criteria and every new claim is forced through them at capture time.

## 1. Mandatory Tags

Every atomic claim receives **exactly one** tag at the moment it is written:

- **[Certain]**  
  Primary source or direct observation is named **and** the exact supporting passage/data is linked or quoted. Third-party checkable. No inference required. The source must have been re-opened and the quote confirmed in the current session — memory of a source is [Likely] at best.

- **[Likely]**  
  Multiple independent secondary sources converge **or** a short, explicit inference chain from [Certain] premises is stated and auditable.

- **[Theory]**  
  Coherent speculation consistent with existing higher-tier material. The missing evidence is explicitly named.

- **[Guessing]**  
  No identifiable source, no inference chain, or only a single weak/anonymous source.  
  **Default** for anything that fails the tests above.  
  **[Unknown]** (legacy / Claim Scout tracker language) maps to **[Guessing]** — do not use both.

### Separate flag (not a tier)

- **[Conflict]** — Two or more sources or claims disagree and the disagreement is material. Not a fifth confidence tier. Use alongside a tier tag when needed (e.g. [Likely] [Conflict]).

Untagged claims are treated as [Guessing].

## 2. Receipts Rule (“Show me the receipts”)

A receipt = **source + warrant**.

- Naming an author, expert, scripture, paper, or dataset is only the first half.
- The text must also show **why** that source actually supports the specific claim under the rules of its domain.

Absence of the warrant keeps the tag at [Likely] or lower.  
Mere citation without warrant is name-dropping, not evidence.

## 3. Capture Discipline

1. Write the atomic claim.
2. Attach the tag **immediately** (even if only [Guessing]).
3. Prefer inline placement for precision.

When a whole proposition rests on mixed evidence, state the proposition once, then list the tagged components underneath if needed.

## 4. Authority

Only the human Steward may **raise, lower, or change** a tag on standing material — after personally verifying the receipt, or consciously accepting a lower bar when evidence is thin.

AIs may propose tags (including proposed changes) in drafts and sidecars.  
AIs may never apply, raise, lower, or finalize a tag on standing material.

Automated topic-candidate lines (see `CORE.md`) may carry a **proposed** tag at most [Likely]; that proposal is not a Steward decision until the Steward acts.
