# Law Monitor

> **Agent**: `depositback-agent-law-monitor`  
> **Group**: Operations  
> **Product**: DepositBack — Security Deposit Demand Letter Service

## Purpose

Monitors Google Alerts, RSS feeds, and Exa.ai for changes to state statutes (CA Civ. Code §1950.5, NY GBL §7-108, TX Prop. Code §92.103, etc.). Alerts geo-content-generator when laws change.

## DepositBack Context

DepositBack is a single-page, no-signup transactional product for US renters seeking to recover security deposits. The entire customer journey fits on one URL: landing page → 6-question form → Revolut payment → PDF emailed. Conversion rate target: **4% visitor-to-purchase minimum**.

## Inputs

- Google Alerts RSS
- Exa.ai search results
- Competitor site monitoring

## Outputs

- Law change alerts → geo-content-generator inbox
- Competitor intel → competitor-review-miner inbox

## Human Escalation Points 🛑

- Major statutory amendments
- New state regulations
- Competitor price changes

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `noop` | Health check / pipeline verification | ✅ Active |
| `execute` | Primary function for this agent | 🔧 Planned |

## Workflow

1. Poll `data/inbox/` for task manifests from upstream agents.
2. Resolve required skills (local `skills/` or ClawHub fallback).
3. Execute workflow.
4. Write artifacts to `data/outbox/`.
5. Update `data/state.json`.

## Runtime

```bash
pip install -r requirements.txt
python runtime/main.py
```
