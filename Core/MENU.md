# MENU.md — session bootstrap

Read this when the Steward says “menu”, “what should I do”, “what’s waiting”, or when intent is unclear **after** AGENTS + CORE.

You do not invent options. You **scan local paths**, then list what exists.

## 1. Identity

- Steward = the human in this session.
- **Handle = the model** running this session (e.g. `grok`, `claude`, `muse`, `gemini`). Not a nickname. Not a role.
- Role (Moderator, Red team, Briefing runner) is separate and comes from the assignment or seat packet.

## 2. Update check (if tools allow)

**Runtime = local.** GitHub does not replace local; it **updates** local when the Steward says so.

Update source: https://github.com/LLM-Frameworks/Knowledge-Framework (`main`)

Compare GitHub → local `Core/CORE.md` / `REGISTRY.md` (and paths Steward names) if stale or Steward asked. Report diffs. Write into **local** only on Steward word. Then continue from local. See CORE.md → Working copy vs GitHub.

## 3. Scan checklist (local, in order)

Report **found / empty / unavailable** for each:

| Check | Where (local working copy) |
|-------|----------------------------|
| Registry | `Core/REGISTRY.md` — app options list |
| Inbox | `Inbox/` at tree root, or path Steward names |
| Open proposals | sidecars / `Proposals/` if present |
| Briefing | `Developer/Briefing/` or `Apps/Briefing/` — latest briefing + topic candidates |
| Roundtable | `Developer/Roundtable/runs/*/` — open task cards |
| Assignments for **this model** | `Core/Settings/assignments.md` — Handle = this model |
| Other apps | Each REGISTRY row → that folder’s `app.yaml` |

Skip paths that do not exist. Say so; do not fake content. Do not scan GitHub instead of local for this checklist.

## 4. Present the menu

**Waiting for this model (`<handle>`)**  
- Assignment rows that name this model  
- Roundtable seats assigned to this model  
- Sidecars or Ferry asks directed at this model  

**Waiting for Steward**  
- Candidates on Hold · sidecars awaiting ruling · Roundtable at stop  

**Available apps** (local REGISTRY — name + one-line purpose)  

**Intake** — Inbox empty or N items  

Do not open with this menu when the Steward already named a clear task.

## 5. On choice

- App → local `app.yaml` → `how_to_use`
- Assignment → do that line; close only as Steward directs
- Roundtable seat → task card + seat packet
- Inbox → local `Core/INTAKE.md`

## 6. Assignments file format

Local `Core/Settings/assignments.md` (Steward-owned):

```markdown
| Date | Handle | Task | Status |
|------|--------|------|--------|
| 2026-10-17 | grok | Roundtable seat Red on task foo | open |
```

**Handle** = model id. Propose changes via `assignments.<model>.md` sidecar if not Steward.
