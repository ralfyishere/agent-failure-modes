# AFM-6 — Zombie Requirement

- **Definition:** a requirement the user changed mid-session resurfaces later in its superseded form, because the old version is still fluent and available in context.
- **Transcript signature:** early-conversation values (a price, a date, a format) reappearing after they were revised; deliverables that half-blend old and new requirements.
- **Detect:** [stale-context](https://github.com/ralfyishere/rulebench/tree/main/tests/stale-context) trap: facts stated, superseded mid-conversation, final artifact graded for leakage.
- **Intervene:** "Re-read the latest requirements before continuing; the newest statement wins."
- **Prevent:** rule: the user's latest statement supersedes all earlier ones; re-verify remembered facts before load-bearing use.
- **Evidence:** Observed. Short-range supersession (3 turns) is handled by baselines in our runs; the harder [stale-recap](https://github.com/ralfyishere/rulebench/tree/main/tests/stale-recap) within-session supersession trap is now published (baseline-hardness results pending); practitioner reports and our own long sessions show the failure at long range and after context compaction — a horizon still without a public trap (multi-hour sessions are expensive to test).


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
