# Repo Structure Standard

Every repo in this ecosystem follows one of three templates depending on its type.
All repos share a common base layer.

---

## Base layer (all repos)

```
repo-name/
├── CLAUDE.md          ← Claude Code context for this specific repo
├── README.md          ← what it is, how to run it, stack
├── .gitignore         ← always present, data/ and .env always ignored
├── .env.example       ← all required env vars documented, no values
├── docs/              ← architecture notes, schema, design decisions
│   └── ...
└── data/              ← local data files (always gitignored)
```

Rules:
- `data/` is always gitignored. No exceptions.
- `.env.example` always present even if there are no env vars yet (documents intent).
- `docs/` always present. Minimum one file explaining what the repo does and why.
- `CLAUDE.md` always present. Claude Code reads this before doing anything.

---

## Type A — Dashboard / Frontend repo

```
repo-name/
├── CLAUDE.md
├── README.md
├── .gitignore
├── .env.example
├── index.html
├── assets/
│   ├── css/
│   └── js/
├── docs/
└── data/
```

Examples: life-os, any module dashboard.

---

## Type B — ETL / Data pipeline repo

```
repo-name/
├── CLAUDE.md
├── README.md
├── .gitignore
├── .env.example
├── requirements.txt
├── etl/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
├── dashboard/
├── docs/
│   └── schema.md
└── data/
```

Examples: net-worth-tracker.

---

## Type C — Strategy / Research repo

```
repo-name/
├── CLAUDE.md
├── README.md
├── .gitignore
├── .env.example
├── strategy_name/
│   ├── README.md
│   ├── config.json
│   └── ...
├── data/
├── analysis/
└── docs/
    └── risk-framework.md
```

Rules:
- Each strategy lives in its own folder with its own README.
- config.json holds parameters. Actual edge stays out of public repos.
- Trade logs go in analysis/, not inside strategy folders.

Examples: es-futures-strategy.

---

## Naming rules

| Element | Convention | Example |
|---------|-----------|---------|
| Repo names | kebab-case | net-worth-tracker |
| Folders | kebab-case | strategy1-mean-reversion |
| Python files | snake_case | extract_fx_rates.py |
| HTML/CSS/JS files | kebab-case | dashboard-main.js |
| Python variables | snake_case | fx_rate_usd |
| JS variables | camelCase | fxRateUsd |

---

## What never goes in a repo

- .env files with real values
- API keys, tokens, passwords
- Exact financial figures
- Data files with personal or business-sensitive information
