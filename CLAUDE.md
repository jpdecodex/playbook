# CLAUDE.md — jpdecodex/playbook

## What this repo does
Central engineering playbook for every repo built by jpdecodex: naming/commit conventions, repo-structure requirements, architecture decision records (ADRs), and the CLAUDE.md template all repos are bootstrapped from.

## Current state (2026-09-05)
Six ADRs now recorded: no heavy JS frameworks, Cloudflare stack, Sheets as input layer, no platform lock-in, Quarto + GitHub Pages, and (new) ADR 006 — a common 5-element project methodology (Current State / Next Action / Decision Log / Evidence / Target Impression), applied across every project in the workspace, format adapted per project, role never dropped. `templates/CLAUDE.md` updated to 6 sections (added `Target Impression`) as the reference implementation for code repos.

## Next action
Pointers sent, ADR 006 adopted across active projects (confirmed in the 2026-09-11/12 workspace audit — CLAUDE.md now exists for revolucion-dulce and job-search too, Target Impression sections in place where they apply). No open action here right now — revisit only if a new project's CLAUDE.md drifts from the 5-element shape.

## Architecture decisions
- No third-party platforms with data lock-in (no Notion, Airtable, Zapier) in any repo.
- No heavy JS frameworks without explicit justification.
- Every repo must have: CLAUDE.md, README.md, .gitignore, .env.example, docs/.
- Commit format: `[scope] short imperative description`.
- Language: English everywhere (code, comments, commits, docs).
