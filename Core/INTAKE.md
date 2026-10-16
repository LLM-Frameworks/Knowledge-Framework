# Intake protocols

How material enters the system. Not an app — pipes, not products.

## 1. Inbox

Unsorted material lands in a **Settings inbox** (personal; not public):

```
Core/Settings/inbox/     # or an app’s Settings/inbox/
```

Nothing in Inbox is live Core, Apps, or References until the Steward files it.

## 2. Propose

AIs offer changes only by:

- Sidecar: `<file>.<handle>.md` next to the target, or  
- Pull request (when git is the working surface)

Never silent overwrite of live Core, Apps, or settled References.

## 3. Ferry (optional multi-model pass)

When the Steward wants cross-model stress test of one artifact or question:

```
Settings/ferry/<topic>.<date>.<model>.md
```

Optional synthesis file: `Settings/ferry/<topic>.<date>.synthesis.md` (Steward or Steward-directed only).

Ferry output is ranking signal only. Agreement among models does not install, approve, or raise tags.

## 4. Topic candidates (automated path — gated)

See `CORE.md` standing authorizations. Briefing (or a later job) may append **candidates** only when every gate passes. Candidates are fuel, not settled thesis. Promotion to `References/` is Steward-only.
