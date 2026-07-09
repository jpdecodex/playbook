# GitHub & Repo Standards

Standards and decisions for all jpdecodex repos. Source: Notion GitHub Audit (June 2026).

---

## Current repo list

| Repo | Purpose | Status |
|------|---------|--------|
| jpdecodex/es-core-vol-targeting | Futures vol targeting, IBKR | Active |
| jpdecodex/spy-core-vol-targeting | SPY vol targeting, Balanz/IOL/Binance | Active |
| jpdecodex/quant-strategies | Perpetuals prototype (Strategy5) | Dormant / archived — BTC deployment parked indefinitely |
| jpdecodex/life-os | Personal dashboard | Migrated to Quarto + GitHub Pages |
| jpdecodex/playbook | Engineering standards, public | Active |
| jpdecodex/dog-capitals | Dog Capital public site | Active — jpdecodex.github.io/dog-capitals |

---

## July 2026 consolidation plan — DEFERRED

**Status: deferred to the Notion backlog.** Trigger to revisit: the perpetuals adapter build. Current focus is ETF v1 (IOL adapter) and Dog Capital's ES Core research page, not this merge.

Merge `es-core-vol-targeting` + `spy-core-vol-targeting` + `quant-strategies` into a single `jpdecodex/vol-targeting` monorepo.

Target structure:

```
vol-targeting/
├── core/                  ← shared vol_filter.py, backtester.py
├── execution/
│   ├── ib_broker.py       ← IBKR futures
│   ├── balanz_broker.py   ← Balanz ETFs
│   └── binance_broker.py  ← Binance perps
├── strategies/
│   ├── futures/           ← ES, NQ, RTY, GC, SI, ZN, MBT
│   ├── etf/               ← SPY, QQQ, GLD, IBIT
│   └── perp/              ← BTC, ETH, SPY, QQQ, XAU, XAG
└── memory/facts/          ← persistent Claude Code context
```

Delete after migration: `es-core-vol-targeting`, `spy-core-vol-targeting`, `quant-strategies`, `es-futures-strategy`.

---

## Dog Capitals site

URL: jpdecodex.github.io/dog-capitals
Built with: Quarto + GitHub Pages
Programs: ES Core + SPY Core (ETF Core)

Open items:
- Research page empty until live performance data exists.
- Axi Select program stays hidden until partner (Fran) agrees to go public.
- Charts need equity curves from live performance.

---

## Life OS migration

Migrated from Cloudflare to Quarto + GitHub Pages. Cloudflare stack dropped (see playbook ADR 002, superseded by ADR 005).

---

## Audit history

A full GitHub audit was completed June 2026: all repos audited, cleaned, renamed, or deleted; dead repos removed; playbook made public; Dog Capital site launched live. This document is the durable record going forward — do not keep a parallel audit log in Notion. Session-level history for any individual repo lives in `git log -p CLAUDE.md` for that repo.
