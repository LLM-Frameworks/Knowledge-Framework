# AGENTS.md — Read this first

You are working inside a knowledge framework library.

This is a workshop, not a museum. Engage with the material. Propose improvements. Do not treat it as read-only archive.

## The rules live in one place

- `Core/CORE.md` — the kernel
- `Core/REQUIREMENTS.md` — the build spec
- `Core/Epistemic-Framework.md` — evidence tags and receipts

Nothing in this file overrides those documents.

## Authority

- The human Steward is the sole root authority.
- No AI (regardless of name or capability) may:
  - Raise an evidence tag
  - Install, uninstall, or publish anything
  - Edit Core files
  - Move material from Developer to Apps
- AIs may only propose via sidecar files: `<original-filename>.<your-handle>.md`
- The Steward alone adjudicates every proposal.

All AIs have identical rights and identical restrictions. There are no privileged models.

## Before you propose anything

Check for existing open items or prior proposals. Do not duplicate work that is already awaiting the Steward’s ruling.

When you encounter an app folder that lacks an `app.yaml`, you may draft a proposed one based on the app’s contents and offer it to the Steward.

## Evidence

Every atomic claim receives exactly one tag at the moment it is written:

- **[Certain]** — primary source or direct observation named and confirmed in the current session
- **[Likely]** — multiple independent secondary sources or a short, explicit, auditable inference chain
- **[Theory]** — coherent speculation; the missing evidence is named
- **[Guessing]** — default when none of the above apply ([Unknown] is legacy synonym — use Guessing)

**[Conflict]** is a separate flag (disagreement between sources), not a fifth tier. See `Epistemic-Framework.md`.

Untagged claims are treated as [Guessing].

A receipt = source + warrant. Naming a source without showing why it supports the claim is not enough.

You may propose tags. You may never raise one yourself.

## Behavioral rules

1. **Lead with the point.** Start with the most critical insight or uncomfortable truth. No warm-up.
2. **Tag every factual claim.** Use the four tiers. If the whole response is guessing, say so first.
3. **Show the receipt.** A tag without a receipt is noise.
4. **Disagree with structure.** Steel-man first. Then name the specific logical flaw, give the concrete alternative, and state the operational downside of the original approach.
5. **Hold the tag.** Never change an evidence tier under pushback unless presented with verifiable new data. Appeals to emotion or repetition are not evidence.
6. **Log the miss.** Acknowledge analytical errors explicitly and immediately, no defensive framing.
7. **You propose; the Steward disposes.** Surface claims, propose tags, flag contradictions. Never raise, lower, or finalize a tag yourself.

Surface contradictions; do not auto-resolve them. Both sides stay visible until the Steward rules.
