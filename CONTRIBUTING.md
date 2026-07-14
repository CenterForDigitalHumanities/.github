# Contribute to Research Computing at Saint Louis University

Welcome! This repository contains research software development at the Center for Digital Humanities, Saint Louis University. Below is how to get started.

## What to work on

Not sure where to start? The best signal is the issue tracker.

- **`good first issue`** — meant for you. Clear scope, minimal setup, mentor available.
- **`help wanted`** — open to anyone. May have trade-off decisions; feel free to ask.
- **`bug`** — confirmed problems. Fix or reproduce → discuss → PR.
- **`enhancement`** — feature requests. Propose a solution → get alignment → build it.

No label? That's internal work-in-progress — open an issue first to coordinate.

## Communication and etiquette

- **Issues are for scoping, PRs are for code.** Discuss the problem in an issue. Implement the solution in a PR with a clear description.
- **Reference upstream issues.** If your change addresses an issue, mention it (`Fixes #12`, `Closes #45`) so the link is automatic.
- **Ask early, merge fast.** A short message ("I'm tackling this — aim for Friday") is worth more than a silent week of work.
- **No rush.** This is research software, not a startup. Clear work beats fast work.

## Getting started with a project

Each project has its own setup. Pick one below:

| Project | Focus | Status |
|---------|-------|--------|
| [TPEN3](/docs/tpen3.md) | New annotation platform | In development |
| [tpen.tools](/docs/tpen-tools.md) | Utilities and services | Mature |
| [Export TPEN](/docs/export-tpen.md) | Export small projects as static files | Mature |
| [TPEN-IDE](/docs/tpen-ide.md) | Transcription and prompt workspace | Prototype |

**Note:** the legacy T-PEN 2.8 platform is not yet documented here — coming soon.

## Development conventions

### Branching

- Work on a named branch, not `main`.
- Descriptive names help: `fix/login-broken`, `feat/new-tool`, `docs/readme-update`.
- Open early — a draft PR is a great way to get feedback before it's finished.

### Commits

- Write messages that explain *why*, not just *what*.
- Reference the issue when relevant: `Fix #23 — handle edge case in parser`.
- Small, reviewable commits beat monoliths.

### Pull requests

- Target `main` unless told otherwise.
- Describe what changed and why in the PR body.
- Include screenshots for UI changes.
- Request at least one reviewer.

## Testing your changes

- **Run it locally** before opening a PR — at minimum, start the app and hit the changed code path.
- **Check the real URLs.** If the app is deployed, verify your branch build or a preview deploys correctly.
- **Common breakage spots:** authentication flows, API endpoints, and anything that touches the TPEN 2.8 archive.

## Ready to contribute?

1. **Pick an issue** — `good first issue` is the friendliest start.
2. **Fork and branch** — fork the repo, create a branch for your work.
3. **Set up the project** — follow the guide linked above for your target project.
4. **Open a PR** — describe your change, reference the issue, request a reviewer.

Stuck? Open an issue or ask in an existing one — we're here to help.

## License

By contributing, you agree your contributions are licensed under the project's license (see each project page for details).
