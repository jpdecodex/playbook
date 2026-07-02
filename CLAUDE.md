# CLAUDE.md — jpdecodex/playbook

## What this repo does
Central engineering playbook for every repo built by Juan Papes: naming/commit conventions, repo-structure requirements, architecture decision records (ADRs), and the CLAUDE.md template all repos are bootstrapped from.

## Current state
Standards defined for git conventions and repo structure (`standards/`). Five ADRs recorded: no heavy JS frameworks, Cloudflare stack, Sheets as input layer, no platform lock-in, Quarto + GitHub Pages. CLAUDE.md template (`templates/CLAUDE.md`) just updated to the 4-section session-loop standard.

## Next action
Keep `standards/github-repo-standards.md` and the ADRs current as the ecosystem consolidates — in particular, track the July 2026 plan to merge es-core-vol-targeting, etf-vol-targeting, and quant-strategies into a new `jpdecodex/vol-targeting` monorepo and retire the three source repos.

## Architecture decisions
- No third-party platforms with data lock-in (no Notion, Airtable, Zapier) in any repo.
- No heavy JS frameworks without explicit justification.
- Every repo must have: CLAUDE.md, README.md, .gitignore, .env.example, docs/.
- Commit format: `[scope] short imperative description`.
- Language: English everywhere (code, comments, commits, docs).
