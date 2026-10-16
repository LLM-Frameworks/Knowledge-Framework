# The Method — NFL Contender Rating

**Status: developing.** Formula and ruled items below are established by Steward word. Proposal-marked items are not adopted until explicit approval.

**Purpose:** identify live contenders, not predict games. Pure rating went 8–14 picking playoff winners across the 2005/2008 tests — that was never its job.

## The formula (established)

For team T over G games:

- **Base:** T's own raw win percentage. (Steward ruling: base is raw record, not prior-adjusted.)
- **Win:** adds the opponent's adjusted win%.
- **Loss:** subtracts the opponent's adjusted *loss* percentage.
- **Tie:** half a win; contributes (opponent adjusted win% − .500).
- **Opponent adjusted win%** = (opponent wins + 1) / (opponent games + 2). One phantom win, one phantom loss — pulls early extremes toward .500.
- Divide the summed adjustment by games played; add to the base.
- Ratings can exceed 1.000. This is a strength score, not a probability.

## The four steps (established)

1. **Rating** — full season. Who belongs.
2. **Trend** — trailing last-3, last-5, last-10. Who is this team *now*.
3. **Path** — bye, home field, opponent order, opponent ratings.
4. **Context** — the checklist below. Never skipped.

## The tripwire (established)

Divergence between the full-season rating and the trailing windows is the signal to dig — not all playoff teams, just the divergences (typically 2–4 per postseason).

**Steward refinement:** a last-3 slump may be a rest artifact. Before reading a slump as decline, check the finale: if the game was effortless (seed locked, starters rested), the slump is schedule information, not team information.

**Home/away split tripwire:** a lopsided home/road record is data worth looking for — flag it the same way as a rating/trend divergence. It stays out of the formula (no home/away term), but a team that is dominant at home and lost on the road (or vice versa) gets Step 4 digging.

## Finale classification (checklist, not formula)

- **Rest games:** REJECTED as a mechanical formula exclusion (7-season stratified test worsened champion rank with no overlap gain). Survives as a Step 4 checklist flag.
- **Full-effort dead rubbers vs elite opponents (PROPOSED):** positive signal *even in a loss*. Judgment call; not mechanically testable. Not adopted until Steward word.

## Context checklist — Step 4 (established, ordered)

1. **QB quality in January** — first on the list. Irreducible context, never a formula term.
2. **Injuries** — who was out, who's back.
3. **Pedigree** — defending champs, playoff experience. Narrative-aware, not narrative-driven.
4. **Home/road extremes** — weak signal only.
5. **Division-built record** — note where the record was built: feasting on a weak division or surviving a strong one.

## In-season use (established)

- Computable any week from Week 4–5 on. Before that, opponent samples are too thin.
- Use current opponent records, not final. Accept the wobble; confidence grows weekly.
- Step 3 becomes remaining schedule plus the division race.

## Companion: weekly score predictor (adopted)

Separate machine alongside the rating, not part of it.

- League average is the base; every unit graded vs base (positive = good).
- Each game is two battles — away offense vs home defense, home offense vs away defense.
- Margin = SCALE × (battle1 − battle2). SCALE fitted weekly by least squares.
- Early-season prior through Week 3: blend last 4 games of prior regular season (no playoffs) at 0.5 weight.
- No home-field term. Turnover component tested and excluded (near-zero correlation).
- Interface: predicted score, yards edges, key injuries (flags for human read, not formula inputs), venue/weather.

Scripts and week files live in Settings/ (or the working data folder): `predict-week.py`, `build-week-data.py`, `week-N-data.json`, `week-N-predictions.md`.

## What the method doesn't do (established)

- Price a QB catching fire (irreducible variance — owned, not fixed).
- College (the .500 prior assumes talent balance).
- "Catch" wild anomalies by overfitting (e.g. forcing 10–6 over 18–0).

## Tested and rejected (established)

- Quality-wins companion as playoff-pack tiebreak.
- Margin of victory / recency weighting as formula terms.
- Rest-game exclusion as arithmetic (kept as checklist only).

## Provenance

- Formula and rulings: Steward design, October 2026.
- Backtests: 2025, 2008, 2005 playoffs; path + injuries tests.
- Method log: AI judgment is used at every step — and authorized at none. Step 4 is never skipped.
