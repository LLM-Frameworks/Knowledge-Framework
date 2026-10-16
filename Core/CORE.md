# CORE.md — the kernel

Small, stable, rarely changed. Everything else is registered and managed through the system calls below.

## Kernel rules (standing orders)

1. **Red-pen authority.** Nothing is filed, published, sent, or applied without the Steward’s explicit word for that exact action.
2. **Evidence tags.** No AI raises evidence tags. Only the Steward raises a tag after personally verifying the receipt.
3. **Sidecar proposals only.** Visiting AIs propose changes in `<file>.<handle>.md` sidecars. The Steward alone adjudicates.
4. **Equal AI status.** All AIs have identical rights and identical restrictions. No model has special privileges.
5. **Silent edits forbidden.** Every change to standing files is logged and surfaced. Nothing lands silently.
6. **Removal = archive + log.** Never silent delete. Archive with reason.
7. **Apps travel; references evolve.** Only apps go through the Developer → Apps pipeline. References are living documents that evolve in place.

## Package manager

Every component (app, evidence rule, framework, thesis) is a package with a lifecycle:

- `repo` — mentioned and available, not installed. Index entry only.
- `install` — on the Steward’s word: files created in their canonical home and registered.
- `upgrade` — substantive changes require the Steward’s word.
- `uninstall` — on the Steward’s word: files archived (never deleted), unregistered, logged with reason.
- `list` — the registry of what is installed and what is available.

## Permissions

- **Steward (human):** root. Install, uninstall, upgrade, raise tags — no further approval needed.
- **All AIs:** may propose via sidecar only. May draft installs for the Steward’s word. May never act unilaterally.

## App lifecycle (canonical)

Defined only here. Other files link here; they do not redefine states.

| Status | Meaning | Location |
|--------|---------|----------|
| nominated | Proposed, not started | Indexed or Developer/ |
| in-process | Actively being built | Developer/ |
| installed | Finished and Steward-approved | Apps/ |

Nothing moves from Developer to Apps without the Steward’s explicit word.

**Graduation rule.** An app may move to Apps/ (and be released to GitHub) only after the Steward has audited it against its requirements and given explicit approval. Requirements live with the project; the audit process itself stays outside the public repository.

## Standing authorizations

By default, no AI writes to standing files without the Steward’s word for that exact action.

**Exception (standing):** Automated Briefing runs may write only:

```
Developer/Briefing/Settings/briefing.<date>.<model>.md
```

(or the same path under Apps/Briefing/Settings/ after graduation).

No other unattended write path is authorized. New paths require an explicit Steward amendment to this section.

## App descriptor (required)

Every app folder under `Apps/` or `Developer/` must contain an `app.yaml` file.  
This is the onboarding contract. Without it the folder is not a recognized app.

Minimum schema:

```yaml
name: string
type: rules | knowledge | method
status: nominated | in-process | installed
purpose: one-line string
triggers:
  keywords: [list of strings]
  ideas: [list of short phrases]
how_to_use: |
  multi-line instructions an AI can follow
depends_on: []  # optional
epistemic_status: settled | developing | theory  # optional but recommended
version: string  # optional but recommended
```

Any AI may draft a proposed `app.yaml` by reading the app contents.  
Only the Steward can approve or install the final version.

## Announcement

Any AI working in the library should read the `app.yaml` files first.  
Installed and nominated apps are announced by the Core via their descriptors, not discovered by wandering the filesystem.

## Path conventions

Paths in this repository are relative to the repository root.
