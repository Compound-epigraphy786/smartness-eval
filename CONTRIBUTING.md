# Contributing

Thanks for contributing to OpenClaw Smartness Eval.

## Development setup

```bash
git clone https://github.com/yh22e/smartness-eval.git
cd smartness-eval
python3 scripts/check.py
```

## Pull request scope

Please keep PRs focused. Good examples:
- scoring formula improvements,
- safer command execution rules,
- new test definitions in `config/task-suite.json`,
- reporting/visualization improvements.

## PR checklist

- [ ] No unsafe command execution patterns introduced
- [ ] No absolute-path assumptions
- [ ] `scripts/check.py` passes
- [ ] `scripts/eval.py --mode quick --no-probes` runs
- [ ] Changelog updated

## Commit message style

Use conventional style:
- `feat: ...`
- `fix: ...`
- `docs: ...`
- `chore: ...`

## Bug reports

Please include:
- OpenClaw version
- OS
- exact command used
- full error output
- minimal reproducible setup
