# jpdecodex/playbook

Engineering standards, conventions, and architecture decisions for all systems built by jpdecodex.

---

## Who builds this

Mechanical Engineer turned systems builder. I design and operate systematic trading strategies, personal finance systems, and business infrastructure — all built in-house, without third-party platforms.

My approach: every system I run, I own. No Notion. No Airtable. No black boxes. Code, data, and logic live in repos I control and understand completely.

## What this playbook covers

This repo is the single source of truth for how every project in my ecosystem is structured, named, versioned, and documented. It exists so that:

- Every new repo starts from the same foundation
- Claude Code has full context before touching any project
- Anyone I work with (partners, collaborators) can orient themselves in minutes

## Ecosystem

| Repo | Description | Visibility |
|------|-------------|------------|
| [life-os](https://github.com/jpdecodex/life-os) | Personal life operating system dashboard | Public |
| es-futures-strategy | Systematic long-only strategies on E-mini S&P 500 | Private |
| net-worth-tracker | Multi-currency net worth tracker (USD, EUR, ARS, BGN) | Private |
| revolucion-dulce | Business systems for Revolución Dulce | Private |

## Philosophy

**Sovereignty over data and systems.** I don't use platforms I can't inspect or migrate away from. Every tool I build is designed to be replaced, extended, or handed off without vendor dependency.

**Modular by default.** Each project is an independent repo. A central dashboard (Life OS) aggregates their outputs. No monorepos, no shared state between projects.

**Built with AI, understood by humans.** Claude and Claude Code are part of my toolchain — but every decision, every line of code, is reviewed and owned by me. AI accelerates; it doesn't replace judgment.

---

## Contents

```
playbook/
├── README.md               ← this file
├── CLAUDE.md               ← global Claude Code context
├── standards/
│   ├── repo-structure.md   ← standard folder layout by repo type
│   ├── git-conventions.md  ← commits, branches, versioning
│   └── naming.md           ← file, variable, and repo naming rules
├── templates/
│   ├── CLAUDE.md           ← base template copied to each new repo
│   ├── README.md           ← base README template
│   ├── .gitignore          ← base gitignore
│   └── .env.example        ← environment variable template
├── decisions/
│   ├── 001-no-frameworks.md
│   ├── 002-cloudflare-stack.md
│   ├── 003-sheets-as-input-layer.md
│   └── 004-no-platform-lock-in.md
└── .claude/commands/
    └── audit-repos.md      ← /audit-repos slash command (see below)
```

## Custom Claude Code commands

### `/audit-repos`

Reporting-only audit of every repo under the projects root: last commit, CLAUDE.md accuracy, ACTIVE/STALE/PARKED/DEAD classification, clutter flags (stale branches, committed secrets, duplicate logic), and a professional-structure score (README/deps/.gitignore/tests/LICENSE/commit quality) per repo. Ends with a summary of what's safe to archive, what needs a CLAUDE.md fix, and what isn't presentable if shown to another developer.

Fixes nothing — it only reports.

**Where it actually lives:** Claude Code only discovers project slash commands in `.claude/commands/` at the folder a session is *launched* from — it does not walk into subdirectories. Since this audit needs to see every sibling repo, the working copy that Claude Code actually reads lives at `C:\Users\juan\projects\.claude\commands\audit-repos.md` (the projects root, not tracked by any repo). The copy in this repo, `.claude/commands/audit-repos.md`, is the documented source of truth — if you ever edit the prompt, edit both, or edit here and re-copy to the root.

Run it from a Claude Code session launched at `C:\Users\juan\projects` by typing:

```
/audit-repos
```

This was the only cross-repo audit tooling in the ecosystem as of 2026-07-24. An earlier `standards/github-repo-standards.md` recorded a June 2026 one-off manual repo-list audit — removed 2026-08-28 once it went permanently stale (it still listed a repo deleted weeks earlier); a repo list is derivable directly from `2.repos/`/`3.no-repos/`, not worth hand-maintaining here.
