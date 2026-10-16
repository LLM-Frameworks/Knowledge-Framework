# Knowledge Framework

A reusable operating system for building and evaluating knowledge.

Where many AI systems focus on memory, this one focuses on thinking straight, proving it, and answering for it — with a human Steward holding the pen. Frameworks here are impersonal logic libraries: they must work against the Steward’s own arguments, not merely for them.

This repository provides:

- **Core** — rules for separating facts from opinions, framing problems, weighing evidence, and collaborating with AIs.
- **Apps** — finished, standalone tools that use the Core.
- **Developer** — in-progress or example apps.
- **References** — settled public theses and supporting material.

## Quick start for any AI or human

1. Read `AGENTS.md` (in Core/) first.
2. Read `Core/CORE.md` for the kernel rules.
3. Check `Apps/` for finished tools you can use immediately.
4. Check `References/theses/` for settled public positions.

## Core principles

- Human Steward is the sole authority. No AI may install, uninstall, raise evidence tags, or publish without the Steward’s explicit word.
- All AIs have equal rights and equal restrictions.
- Evidence is tagged at capture: [Certain], [Likely], [Theory], [Guessing].
- Apps can stand alone. The Core improves the quality of their theses.

## Adding your own app

Fork the repo. Place your work under `Developer/`. When it is finished and the Steward (or you, if you are the Steward of your fork) approves, move it to `Apps/`.

See `CONTRIBUTING.md` for the full process.

## Related

- [VA-Claim-Scout](https://github.com/LLM-Frameworks/VA-Claim-Scout) — also shipped under Apps/Claim Scout in this tree
- [Cornerstone](https://github.com/LLM-Frameworks/Cornerstone) — private formation system

## License

See LICENSE.
