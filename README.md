# OpenClaw Smartness Eval

[![Version](https://img.shields.io/badge/version-0.2.1-blue)](./CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT--0-green)](./LICENSE)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-2026.3.13-orange)](./SKILL.md)

A production-focused evaluation skill for measuring how "smart" an AI agent actually is across **12 dimensions**.

It combines:
- repeatable automated task tests,
- real runtime telemetry/log evidence,
- trend comparison over time,
- anti-gaming probes,
- and optional LLM judge scoring.

## Why this project matters

Most agent improvements are anecdotal. This project makes capability evolution measurable.

`openclaw-smartness-eval` turns day-to-day runtime data into:
- a structured score,
- confidence interval,
- risk flags,
- and concrete upgrade recommendations.

## Quick Start

### 1) Health check

```bash
python3 scripts/check.py
```

### 2) Quick eval

```bash
python3 scripts/eval.py --mode quick --no-probes
```

### 3) Standard eval + Markdown report

```bash
python3 scripts/eval.py --mode standard --format markdown
```

## What gets scored

### Main dimensions
- understanding
- analysis
- thinking
- reasoning
- self_iteration
- dialogue_communication
- responsiveness

### Expanded dimensions
- robustness
- generalization
- policy_adherence
- tool_reliability
- calibration

## Output

Artifacts are written under `state/smartness-eval/`:
- `runs/<timestamp>.json`
- `reports/<date>.md`
- `history.jsonl`

## Repository structure

```text
.
├── SKILL.md
├── _meta.json
├── config/
│   ├── config.json
│   ├── rubrics.json
│   └── task-suite.json
├── scripts/
│   ├── eval.py
│   ├── check.py
│   └── state_probe.py
└── docs/
```

## Compatibility

- OpenClaw `2026.3.13+`
- Workspace V5.1 compatible
- macOS / Linux

## Author

- 圆规

## Contributing

Issues and PRs are welcome. Start with:
- `CONTRIBUTING.md`
- `SECURITY.md`
- `docs/ROADMAP.md`

## Star & Share

If this project helps your agent workflow:
1. ⭐ Star this repo
2. 🧪 Share your benchmark result screenshot
3. 🔁 Post your before/after trend in X / GitHub Discussions
