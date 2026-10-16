# NFL Contender Rating

**Status:** Nominated (Developer until audited)

Identifies **live contenders**, not pure game picks. A pure rating went 8–14 on playoff winners in backtests — that was never the job.

## What it does

1. **Rating** — schedule-adjusted strength from the full season so far  
2. **Trend** — last-3 / last-5 / last-10  
3. **Path** — remaining schedule, bye, home field, opponent order  
4. **Context** — checklist (QB, injuries, pedigree, home/road, division-built record) — never skipped  

**Tripwire:** divergence between full-season rating and trailing windows → dig (typically a few teams, not the whole slate).

## Companion (optional)

Weekly score predictor (`predict-week.py`) — separate machine. League-average base, unit grades, no home-field term. “Prediction isn’t a perfect science. It’s based on data and a good guess.”

## Layout

| Path | Role |
|------|------|
| `method.md` | Formula, steps, rejected ideas, provenance |
| `requirements.md` | Must-pass / nice-to-haves |
| `Settings/` | Live week data, scripts, predictions (personal; gitignored) |

Working files may still live under the old Wiki `NFL-rankings/` until fully moved into Settings/.

## Briefing

Standing NFL lane (Steelers & Bills; prediction tool) can summarize rating tripwires and the current week’s prediction card without treating either as settled truth.
