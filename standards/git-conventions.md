# Git Conventions

## Commit format

```
[scope] short imperative description
```

- Scope is the module or layer being changed.
- Description is imperative mood, lowercase, no period.
- Keep it under 72 characters.

Good examples:
- [trading] add gap strategy skeleton
- [life-os] connect net-worth module to dashboard
- [etl] fix fx rate conversion for ARS
- [docs] update schema after SQLite migration

## Scopes by repo

| Repo | Common scopes |
|------|--------------|
| life-os | [life-os] [dashboard] [modules] |
| es-futures-strategy | [strategy1] [strategy2] [strategy3] [strategy4] [analysis] |
| net-worth-tracker | [etl] [dashboard] [data] [docs] |
| revolucion-dulce | [ops] [dashboard] [docs] |
| playbook | [standards] [templates] [decisions] [docs] |

Use [chore] for maintenance. [docs] for documentation only. [fix] when scope is unclear.

## Branching

- main — always deployable. Never commit broken code here.
- Feature branches: feature/description
- Hotfix branches: fix/description

For solo projects, committing directly to main is fine as long as it works.

## What to commit

- Working, tested code only to main.
- Never commit: .env, data/, credentials, gitignored files.
- Always commit: requirements.txt changes, config.json changes, CLAUDE.md updates.
