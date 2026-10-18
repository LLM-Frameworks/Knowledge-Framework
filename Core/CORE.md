# CORE.md — the kernel

Small, stable, rarely changed. Everything else is registered and managed through the system calls below.

## Kernel rules (standing orders)

1. **Red-pen authority.** Nothing is filed, published, sent, or applied without the Steward’s explicit word for that exact action.
2. **Evidence tags.** No AI raises, lowers, or changes evidence tags on standing material. Only the Steward may apply or modify a tag after verifying the receipt (or consciously accepting a lower bar).
3. **Sidecar proposals only.** Visiting AIs propose changes in `<file>.<handle>.md` sidecars. The Steward alone adjudicates.
4. **Equal AI status.** All AIs have identical rights and identical restrictions. No model has special privileges.
5. **Silent edits forbidden.** Every change to standing files is logged and surfaced. Nothing lands silently.
6. **Removal = archive + log.** Never silent delete. Archive with reason.
7. **Apps travel; references evolve.** Only apps go through the Developer → Apps pipeline. References are living documents that evolve in place.

## Working copy vs GitHub

**Runtime home is local** — the Steward’s working tree (Google Drive `LLM Frameworks/`, a git clone on disk, or whatever path the Steward names). Sessions load AGENTS, CORE, MENU, REGISTRY, and apps **from that local copy**.

**GitHub is the update source and public canonical**, not the day-to-day workspace:

https://github.com/LLM-Frameworks/Knowledge-Framework (`main`)

### Update check (when tools allow)

An AI **should** compare GitHub → local when:

- the Steward asks to sync or check for updates, or
- the local copy may be stale (long gap, missing Core files, conflicting versions), or
- MENU/orientation is about to run and local REGISTRY is missing or clearly old.

**Procedure:**

1. Read remote `Core/CORE.md`, `Core/AGENTS.md`, `Core/REGISTRY.md` (and other paths the Steward names).
2. Compare to the **local** working copy.
3. Report what would change — do not silently overwrite local files.
4. **Apply updates to local only on the Steward’s word** (Steward-directed sync). After a sync, continue from local.

Direction of truth for routine work: **local**. Direction of publish for the public tree: Steward pushes or approves publish to GitHub. Do not treat “read GitHub only and never use local” as the default.

If network/tools are unavailable: use local only; note that update check was skipped.

Private packages (e.g. Cornerstone) have their own repos; this section covers the public Knowledge-Framework tree.

## Orientation

`Core/REGISTRY.md` **in the local working copy** is the single options list for app names.

- Unclear intent / “what’s possible” / “what’s waiting” → follow local `Core/MENU.md` (scan local paths).
- Clear app trigger → run that local app path.
- Do not maintain a second ad-hoc menu.
- After a Steward-approved sync, local REGISTRY matches GitHub; until then, local wins for the session.

## Package manager

Every component (app, evidence rule, framework, thesis) is a package with a lifecycle:

- `repo` — mentioned and available, not installed. Index entry only.
- `install` — on the Steward’s word: files created in their canonical home and registered.
- `upgrade` — substantive changes require the Steward’s word.
- `uninstall` — on the Steward’s word: files archived (never deleted), unregistered, logged with reason.
- `list` — the registry of what is installed and what is available.

## Permissions

- **Steward (human):** root. Install, uninstall, upgrade, raise/lower/change tags — no further approval needed.
- **All AIs:** may propose via sidecar only. May draft installs for the Steward’s word. May never act unilaterally except under Standing authorizations below.

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

### A. Briefing log (always, when automated)

```
Developer/Briefing/Settings/briefing.<date>.<model>.md
```

(or the same path under Apps/Briefing/Settings/ after graduation).

### B. Topic candidates (conditional)

Automated jobs may **append** only to:

```
Developer/Briefing/Settings/topics/<lane>/candidates.md
```

(or `Core/Settings/topics/<lane>/candidates.md` if the Steward consolidates there).

**Every gate must pass** or the item stays in the briefing log only:

1. Source + warrant present (not vibe or unsourced summary)
2. Proposed confidence at most [Likely] — never auto-[Certain]
3. No personal names, dossier paths, or private-lane material
4. No normative “ought” framed as settled doctrine
5. Not a publish to References/ or Apps/ (candidates only)
6. Optional: ≥ N models agree on the same atomic claim (Ferry) — ranking signal only
7. Steward may freeze any lane at any time (circuit breaker)

Fail any gate → write briefing file only, or mark `needs-steward` in the candidate line.

**Not authorized:** raising tags, editing Core, graduating apps, publishing posts, or treating candidates as settled thesis.

New write paths require an explicit Steward amendment to this section.

Intake procedures (Inbox, Propose, Ferry) are documented in `Core/INTAKE.md`.

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

Paths in this repository are relative to the repository root (local working copy).
