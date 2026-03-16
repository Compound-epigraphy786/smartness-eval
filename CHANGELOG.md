# Changelog

All notable changes to this project are documented in this file.

## [0.2.1] - 2026-03-16

### Added
- `scripts/state_probe.py` to replace inline probe commands with safer local probes.
- command validation guardrails in `scripts/eval.py`.

### Changed
- removed inline `python -c` style commands in `config/task-suite.json`.
- updated metadata author to `圆规`.
- clarified external API behavior for `--llm-judge` in `SKILL.md`.

### Security
- blocked unsafe command patterns: `-c`, `exec(`, absolute path, and path traversal.

## [0.2.0] - 2026-03-16

### Added
- 12-dimension capability evaluation framework.
- 28 automated tests + anti-gaming probes.
- CI-like scoring outputs and Markdown report generation.
- optional LLM judge scoring.
