# CLAUDE.md — jpdecodex/playbook

## What this repo does
Central engineering playbook for every repo built by Juan Papes: naming/commit conventions, repo-structure requirements, architecture decision records (ADRs), and the CLAUDE.md template all repos are bootstrapped from.

## Current state
Standards defined for git conventions and repo structure (`standards/`). Five ADRs recorded: no heavy JS frameworks, Cloudflare stack, Sheets as input layer, no platform lock-in, Quarto + GitHub Pages. CLAUDE.md template (`templates/CLAUDE.md`) just updated to the 4-section session-loop standard.

## Next action
Keep `standards/github-repo-standards.md` and the ADRs current. The es-core-vol-targeting/spy-core-vol-targeting/quant-strategies → `jpdecodex/vol-targeting` consolidation is deferred to the Notion backlog (trigger: perpetuals adapter build) — focus is ETF v1 (IOL adapter) and Dog Capital's ES Core research page for now.

## Architecture decisions
- No third-party platforms with data lock-in (no Notion, Airtable, Zapier) in any repo.
- No heavy JS frameworks without explicit justification.
- Every repo must have: CLAUDE.md, README.md, .gitignore, .env.example, docs/.
- Commit format: `[scope] short imperative description`.
- Language: English everywhere (code, comments, commits, docs).
