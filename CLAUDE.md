# CLAUDE.md — jpdecodex/playbook

## What this repo does
Central engineering playbook for every repo built by jpdecodex: naming/commit conventions, repo-structure requirements, architecture decision records (ADRs), and the CLAUDE.md template all repos are bootstrapped from.

## Current state (2026-08-28)
Scope narrowed after a full environment audit found `standards/github-repo-standards.md` (a June 2026 one-off repo-list snapshot) permanently out of date — it still listed a repo deleted weeks earlier. Removed rather than maintained going forward: a repo list is derivable from `2.repos/`/`3.no-repos/` directly, not worth hand-keeping here. What actually stays alive: the CLAUDE.md template (`templates/CLAUDE.md`, 5 sections including the optional `Origin`) and the `/audit-repos` slash command (documented in README.md — the working copy Claude Code reads lives at the projects root, this repo holds the source-of-truth copy). Five ADRs recorded: no heavy JS frameworks, Cloudflare stack, Sheets as input layer, no platform lock-in, Quarto + GitHub Pages.

## Next action
Candidate ADR, not yet written: generalize the "Regla de Oro" from `es-core-vol-targeting/docs/ES_Core_PLAN_DEFINITIVO.md` ("nothing gets published/sent/applied without being defensible with real criteria and citations") beyond ES Core specifically — this repo's existing ADRs cover infrastructure choices, nothing covers rigor/defensibility of a claim. Don't write it yet; revisit once the broader projects-root reorganization (in progress, 2026-08-28) settles.

## Architecture decisions
- No third-party platforms with data lock-in (no Notion, Airtable, Zapier) in any repo.
- No heavy JS frameworks without explicit justification.
- Every repo must have: CLAUDE.md, README.md, .gitignore, .env.example, docs/.
- Commit format: `[scope] short imperative description`.
- Language: English everywhere (code, comments, commits, docs).
