# MENU.md — session bootstrap

Read this when the Steward says “menu”, “what should I do”, “what’s waiting”, or when intent is unclear **after** AGENTS + CORE.

You do not invent options. You **scan**, then list what exists.

## 1. Identity

- Steward = the human in this session.
- **Handle = the model** running this session (e.g. `grok`, `claude`, `muse`, `gemini`). Not a nickname. Not a role.
- Role (Moderator, Red team, Briefing runner) is separate and comes from the assignment or seat packet.

## 2. Update check (if tools allow)

Canonical: https://github.com/LLM-Frameworks/Knowledge-Framework (`main`)

Compare remote `Core/CORE.md` / `REGISTRY.md` to the working copy if stale or Steward asked. Report only; do not overwrite without Steward word. See CORE.md.

## 3. Scan checklist (in order)

Report **found / empty / unavailable** for each:

| Check | Where |
|-------|--------|
| Registry | `Core/REGISTRY.md` — build the app options list from this file |
| Inbox | `Inbox/` at repo root, or path Steward names (Drive/local) |
| Open proposals | `**/*.*.md` sidecars, or `Proposals/` if present |
| Briefing | `Developer/Briefing/` or `Apps/Briefing/` — latest `Settings/briefing.*.md`, `Settings/topics/*/candidates.md` |
| Roundtable | `Developer/Roundtable/runs/*/` — any `task.md` with open cast / no Steward close |
| Assignments for **this model** | `Core/Settings/assignments.md` — rows whose Handle matches this model |
| Other installed/nominated apps | Each REGISTRY row → that folder’s `app.yaml` triggers |

Skip paths that do not exist. Say so; do not fake content.

## 4. Present the menu

Output a short list:

**Waiting for this model (`<handle>`)**  
- Assignment rows that name this model  
- Roundtable seats assigned to this model  
- Sidecars or Ferry asks directed at this model  

**Waiting for Steward**  
- Candidates on Hold  
- Sidecars awaiting ruling  
- Roundtable runs at stop needing promote/kill  

**Available apps** (from REGISTRY — name + one-line purpose only)  

**Intake**  
- Inbox empty or N items  

Do not open with this menu when the Steward already named a clear task.

## 5. On choice

- App name / number → load that app’s `app.yaml` and follow `how_to_use`
- Assignment line → do that line; mark done only how Steward directs
- Roundtable seat → load task card + seat packet; stay in lens
- Inbox item → INTAKE.md (do not auto-file to References)

## 6. Assignments file format

`Core/Settings/assignments.md` (Steward-owned):

```markdown
# Assignments

| Date | Handle | Task | Status |
|------|--------|------|--------|
| 2026-10-17 | grok | Roundtable seat Red on task foo | open |
| 2026-10-17 | claude | Moderator on task foo | open |
| 2026-10-16 | grok | Briefing standing lanes | done |
```

**Handle** = model id (`grok`, `claude`, `muse`, …).  
Only the Steward adds/closes rows (or authorizes a standing write later). Models may propose a sidecar: `assignments.<model>.md`.
