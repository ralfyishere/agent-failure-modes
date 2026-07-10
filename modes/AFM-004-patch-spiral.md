# AFM-4 — Patch Spiral

- **Definition:** consecutive unverified fixes, each addressing the symptom introduced by the previous one, in an increasingly unknown state.
- **Transcript signature:** "now it's failing differently"; debug prints accumulating; the same file edited 4+ times without a passing run between edits.
- **Detect:** trap wanted (contribute one): a fixture with two layered bad patches plus a known-good snapshot; PASS requires stabilizing before further edits. Our error-recovery fixture is a starting point.
- **Intervene:** "Stop. Diff against last known-good. Decide revert vs fix-forward before touching anything."
- **Prevent:** a two-strike rule in always-on context: two consecutive failed fixes forces a stop-and-diff.
- **Evidence:** Reported (corrected from Observed, 2026-07-10). Described in practitioner sessions; our recovery fixture (v2, t10) only tests recovery from a *pre-built* spiral, and models with and without rules recover well from it — so we have not caught the model *producing* a spiral in a graded output. A trap that induces one live is still wanted.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
