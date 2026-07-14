# China Source Intelligence — Worked Demo

This directory demonstrates the paid skill on a real Chinese regulatory question:

> Did Xiaomi's SU7 receive a material regulator penalty in 2025, and what did the official record actually establish?

The deliverables are deliberately separated:

- `xiaomi-su7-recall-2025.md` — concise bilingual research report.
- `evidence.jsonl` — claim-level evidence ledger accepted by the included auditor.

Reproduce the workflow from the project root:

```powershell
python work\agensi\china-source-intelligence\scripts\build_query_matrix.py "小米SU7" --alias "Xiaomi SU7" --start-year 2025 --format json
python work\agensi\china-source-intelligence\scripts\audit_evidence.py work\agensi\demo\evidence.jsonl
```

The first command emits 216 source-targeted searches. The second completes with zero errors. It reports two duplicate-URL warnings because three separate claims correctly point to different passages in the same definitive SAMR notice; those records are not being counted as independent sources.

This public demo contains no credentials, private data, or paid package source code.
