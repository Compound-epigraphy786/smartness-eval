# Security Policy

## Supported versions

| Version | Supported |
|---------|-----------|
| 0.2.x   | ✅ |

## Reporting a vulnerability

Please do not open public issues for sensitive vulnerabilities.

Contact via private channel and include:
- affected version
- reproduction steps
- impact analysis
- suggested mitigation (optional)

## Security design notes

This project intentionally restricts command execution in `scripts/eval.py`:
- only `python3` commands are accepted,
- blocks `-c` inline execution,
- blocks `exec(` patterns,
- blocks absolute paths and path traversal,
- restricts path prefixes to controlled directories.

Optional external API calls are off by default and only enabled with `--llm-judge`.
