# Core OS Requirements

The build specification for the knowledge framework.

## 1. Kernel

- Small, stable, rarely changed.
- Red-pen authority: nothing is filed, published, sent, or applied without the Steward’s explicit word for that exact action.
- No AI raises evidence tags — only the Steward, after personally verifying the receipt.
- Visiting AIs propose in `<file>.<handle>.md` sidecars; the Steward alone adjudicates.
- All AIs have equal rights and equal restrictions. No privileged models.
- Every background edit to standing files is logged and surfaced — nothing lands silently.
- Removal = archive + log with reason. Never silent delete.

## 2. Package manager

- Every component is a package with a lifecycle: `repo` → `install` → `upgrade` → `uninstall`, plus `list`.
- Install and uninstall are clean — one action registers or removes everything, no orphans left behind.

## 3. Permissions

- **Steward (human):** root.
- **All AIs:** sidecars only. No direct edits to Core or installed Apps.

## 4. Registry

- The Core knows what every component is and does.
- App schema: name, type, one-line purpose, status, epistemic status (settled / developing / theory), how to use it.

## 5. App types

- **rules** — applied to evaluate work (evidence tiers, debate rules).
- **knowledge** — consulted for content (theses, topic modules).
- **method** — a repeatable way of working.

New types may be defined by the Steward’s word when needed.

## 5b. App descriptor (required)

Every app folder must contain a committed `app.yaml` with at least:

- name
- type
- status
- purpose
- triggers (keywords + ideas)
- how_to_use

AIs may propose an `app.yaml` by reading the app. Only the Steward approves it.

## 6. Announcement

Any AI working in the library reads the `app.yaml` descriptors first. Installed and nominated apps are announced by the Core via their descriptors.

## 7. Evidence discipline

Every atomic claim receives exactly one tag at capture time. Untagged = [Guessing]. A receipt = source + warrant.

## 8. Universal project requirements (must pass)

These apply to every app in addition to any project-specific requirements:

- Plain language: jargon defined on first use
- No fabrication: no source → no fact
- Evidence tags used correctly where claims are made
- Valid `app.yaml` present and accurate
- No personal or private material in the shipped files
- Follows Core authority model (Steward disposes)

Project-specific requirements and nice-to-haves live with the project (see `Developer/requirements.template.md`).

## 9. Settings folders

- `Core/Settings/` — Steward’s personal configuration, open-items, audit checklist. Not shipped publicly.
- Every app may have its own `Settings/` folder for instance-specific files (trackers, local notes, etc.). These are personal and should be gitignored.
