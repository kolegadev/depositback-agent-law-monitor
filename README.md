# depositback-agent-law-monitor

Tracks state security deposit law changes and competitor mentions

## DepositBack Agent Network — Operations

Part of the DepositBack autonomous marketing system.

## Quick Start

```bash
git clone https://github.com/kolegadev/depositback-agent-law-monitor.git
cd depositback-agent-law-monitor
pip install -r requirements.txt
python runtime/main.py
```

## Structure

```
.
├── SKILL.md, manifest.json, README.md
├── runtime/main.py
├── skills/skill_resolver.py, noop.py
├── data/inbox/, data/outbox/
└── .github/workflows/heartbeat.yml, scan.yml
```

## License

MIT — DepositBack Agent Network
