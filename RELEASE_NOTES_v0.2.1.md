# Release v0.2.1

## Highlights
- Security hardening for test command execution.
- Removed inline script execution patterns from task suite.
- Added safer probe script for local checks.
- Updated author to `圆规`.

## Upgrade notes
No breaking changes to command interface.

## Recommended command
```bash
python3 scripts/eval.py --mode quick --no-probes
```
