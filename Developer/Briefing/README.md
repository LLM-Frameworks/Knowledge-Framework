# Briefing

Produces daily or on-demand briefings from a Steward-owned list of people and topics.  
Output can feed blog drafts, social comments, debate material, and other downstream tools.

## How it works

1. Steward maintains `Settings/people-topics.md`.
2. Any capable AI runs the briefing (manual or scheduled).
3. Manual runs stay in conversation. Automated runs write:
   ```
   Settings/briefing.<date>.<model>.md
   ```
4. AIs may propose changes to the list; only the Steward applies them.
5. Other apps read the dated briefing files when they exist.

## Status

Nominated — in Developer until audited and approved for Apps/.
