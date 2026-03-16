# Architecture

`openclaw-smartness-eval` is composed of:

1. **Task execution layer** (`scripts/eval.py`)
   - selects tests by mode (`quick`, `standard`, `deep`)
   - validates command safety
   - executes tests and captures outputs

2. **Metric ingestion layer**
   - reads latency, error tracker, benchmark history, orchestrator logs, reasoning DB
   - applies time-window filtering

3. **Scoring layer**
   - computes task-level and dimension-level scores
   - merges into weighted overall score
   - computes confidence interval and trend deltas

4. **Output layer**
   - emits JSON run artifact
   - emits Markdown report
   - appends history row for longitudinal tracking

## Safety model

- command execution is constrained to `python3`
- blocks inline execution and suspicious tokens
- blocks absolute paths and traversal
- limits executable paths to approved prefixes
