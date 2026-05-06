# CLAUDE.md — [repo-name]

> Replace all [bracketed] fields before committing. Delete this line.

## Project

**Name:** [Project name]
**Owner:** Juan Papes
**Purpose:** [One sentence: what this repo does and why it exists]
**Type:** [dashboard | etl-pipeline | strategy-research | business-ops]

## Stack

| Layer | Technology |
|-------|-----------|
| [Frontend] | [HTML · Vanilla JS · CSS] |
| [Backend] | [Python · Cloudflare Workers] |
| [Data] | [Google Sheets · SQLite] |
| Hosting | Cloudflare Pages |
| Version control | GitHub |

## Conventions

Follow jpdecodex/playbook standards:
- Naming: kebab-case repos/files, snake_case Python, camelCase JS
- Commits: [scope] short imperative description
- Language: English everywhere
- Data: never commit data/, .env, or sensitive values

## Restrictions

- No third-party platforms with lock-in
- No heavy JS frameworks without justification
- No sensitive data in the repo
- [Add project-specific restrictions here]

## Current state

[Describe what exists, what works, what is in progress. Update this each session.]

## Session rules

1 chat = 1 concrete task.
At the start of each session: read this file + describe the current task.
At the end: commit working code, update current state if needed.
