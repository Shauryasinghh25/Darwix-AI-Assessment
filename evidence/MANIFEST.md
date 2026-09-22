# test_reports Directory Manifest (`test_reports/my-run`)

This directory contains fresh, fully reproducible test_reports generated from executing the actual project components.

## Subdirectory Structure & Files

### Voice: Voice Agent Lead Qualification (`test_reports/my-run/Voice/`)
- `cooperative/` -> `transcript.txt`, `result.json`
- `objection/` -> `transcript.txt`, `result.json`
- `incomplete/` -> `transcript.txt`, `result.json`
- `conflicting/` -> `transcript.txt`, `result.json`
- `out_of_scope/` -> `transcript.txt`, `result.json`
- `human_escalation/` -> `transcript.txt`, `result.json`

### Knowledge: Grounded Retrieval Knowledge Base (`test_reports/my-run/Knowledge/`)
- `build_report.json` -> Complete index statistics, doc count (5 docs, 21 records), PII masking log
- `retrieval_cases.json` -> 6 benchmark retrieval queries across categories
- `retrieval_report.json` -> Retrieval accuracy and BM25 algorithm parameters

### Regional: Multilingual & Multi-Register Bots (`test_reports/my-run/Regional/`)
- `philippines/english/` -> `transcript.txt`, `evaluation.json`
- `philippines/filipino/` -> `transcript.txt`, `evaluation.json`
- `philippines/taglish/` -> `transcript.txt`, `evaluation.json`
- `indonesia/formal/` -> `transcript.txt`, `evaluation.json`
- `indonesia/colloquial/` -> `transcript.txt`, `evaluation.json`
- `indonesia/regional/` -> `transcript.txt`, `evaluation.json`
- `indonesia/regional/regional_validation_status.json` -> Javanese polite keyword validation

### Realtime: Real-Time Audio Stream Intelligence (`test_reports/my-run/Realtime/`)
- `missed_cross_sell/` -> `transcript.txt`, `evaluation.json`
- `compliance/` -> `transcript.txt`, `evaluation.json`
- `frustration/` -> `transcript.txt`, `evaluation.json`
- `noisy_call/` -> `transcript.txt`, `evaluation.json`
- `latency.json` -> Latency metrics (P50, P95, mean)
- `latency_report.md` -> Markdown report on stream latency & simulation parameters
- `false_positive_report.json` -> Noisy audio false positive test results

### Execution Summaries (`test_reports/my-run/summary/`)
- `regression_summary.json` -> Complete output of 81-test regression matrix
- `run_summary.json` -> Overall run metadata, environment info, timestamp

## Reproducibility
To regenerate all test_reports files in this directory at any time, run:
```powershell
python tools/generate_test_reports.py
```
