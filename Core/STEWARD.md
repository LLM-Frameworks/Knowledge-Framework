# STEWARD.md — Layout and multi-AI rules

This file is the single source of truth for **folder purpose** and **multi-AI rules**.  
App lifecycle states and graduation are defined only in `CORE.md` — this file does not redefine them.  
No AI may edit, move, or contradict this file. Only the Steward updates it.

## Folder purposes

- **Core/** — the OS: kernel rules, requirements, evidence standards, intake protocols (`INTAKE.md`), and templates.
- **Developer/** — apps and modules still being worked on. The only place unfinished apps live.
- **Apps/** — finished, installed apps only. Nothing lands here until the Steward declares it finished.
- **References/** — settled public theses and supporting material.
- **Settings/** (inside Core/) — instance-specific or personal configuration. Not for public GitHub.
- Every app may have its own **Settings/** for instance-specific files (gitignored).

## App lifecycle

See `CORE.md` (canonical). Summary: work in Developer/ → Steward audit → explicit approval → GitHub and/or Apps/.  
Requirements (must-pass) and nice-to-haves live with each project. The personal audit checklist lives in Core/Settings/.

## Multi-AI rules

1. **All AI output is provisional.** AIs propose via sidecar files (`<file>.<handle>.md`) or tagged proposals. They never write directly to live Core, Developer, or Apps except under standing authorizations in `CORE.md`.
2. **No per-AI folders.** Model-owned directories are forbidden. Use model tags in the filename instead.
3. **Agreement is a ranking signal only.** Convergence among AIs may promote an item for review. It still requires the Steward’s explicit word (except gated candidate appends).
4. **Hard isolation of state.** No AI may keep private memory, goals, or preferences about the library across sessions. Every new conversation starts from the live files only.
5. **Escalation on lock.** If an AI refuses to act because of an internal lock or safety flag, it must state the exact lock and stop. The refusal becomes an open item for the Steward.

## Red-pen rule

No AI creates, edits, moves, or deletes anything without the Steward’s explicit word for that exact action, except standing authorizations in `CORE.md`. Sidecars and tagged proposals are the normal form of AI contribution.
