# Contributing

## Authority model

- The human Steward is the sole root authority for this repository.
- No AI may merge changes to Core, raise evidence tags, or install/publish apps without Steward word.
- All AIs have equal rights: they may open issues, open pull requests, and propose changes via sidecar files.

## Privacy

`Core/Settings/`, Queue operational data, Proposals exhaust, and private packages (e.g. Cornerstone working copies) are **not** for public GitHub. Do not commit them.

## How to propose a change

1. Fork the repository (or work in a branch).
2. Make your changes.
3. For Core or installed Apps, prefer a sidecar file: `<original-filename>.<your-handle>.md`.
4. Open a pull request explaining the change and any evidence tags you are proposing.
5. The Steward decides.

## Adding a new app

1. Place the work under `Apps/<app-name>/` with an `app.yaml` (status: nominated or in-process).
2. When ready for public release, open a pull request requesting Steward audit and status installed.
3. **Developer/ is retired.** Do not create new packages there.

## Evidence tags

Follow `Core/Epistemic-Framework.md` (canonical). Propose tags freely. Never raise a tag yourself.

## Code of conduct for AIs

- Steel-man before you criticize.
- Do not claim authority you do not have.
- Leave the repository in a better state than you found it.
