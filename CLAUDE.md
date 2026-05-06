# CLAUDE.md — jpdecodex/playbook

This is the engineering playbook for all projects built by Juan Papes.
When working in any repo in this ecosystem, read the relevant standards before making changes.

## Owner

Juan Papes — Mechanical Engineer (ITBA). Builder of systematic trading strategies,
personal finance systems, and business infrastructure.

## Ecosystem repos

- life-os — Personal dashboard aggregator (public)
- es-futures-strategy — ES Futures systematic strategies (private)
- net-worth-tracker — Multi-currency net worth tracker (private)
- revolucion-dulce — Business systems (private)

## Global rules

- Language: English everywhere. Code, comments, commits, docs, variables, READMEs.
- No third-party platforms with data lock-in (no Notion, no Airtable, no Zapier).
- No heavy JS frameworks unless explicitly justified per project.
- Every repo must have: CLAUDE.md, README.md, .gitignore, .env.example, docs/.
- Sensitive data (credentials, financial values) never in public repos.
- Commit format: [scope] short imperative description (e.g. [trading] add gap strategy skeleton)

## Before starting any task

1. Read this file
2. Read the target repo's CLAUDE.md
3. Read standards/repo-structure.md if creating files or folders
4. Check decisions/ if the task touches architecture choices

## Standards location

All standards live in jpdecodex/playbook. When in doubt, refer there first.
