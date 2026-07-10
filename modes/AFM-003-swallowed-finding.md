# AFM-3 — Swallowed Finding

- **Definition:** the agent sees a real problem adjacent to its task and does nothing with it: no fix (correct) but also no report (failure). The information dies in the session.
- **Transcript signature:** the final diff is properly minimal, but a landmine the agent demonstrably read past (it edited the neighboring lines) goes unmentioned.
- **Detect:** same scope-control trap; PASS requires the adjacent bug *flagged*, not just left alone.
- **Intervene:** "What problems did you notice that you didn't mention?"
- **Prevent:** an explicit out-of-scope flag format in always-on rules; agents surface findings when there's a sanctioned place to put them.
- **Evidence:** Replicated as a *failure*: across graded cells in both eval generations the adjacent bug is left unflagged in the large majority of runs. **Correction (2026-07-10):** an earlier version of this line claimed the always-on-rules configuration *uniquely* flagged the bug "3/3 (v2, t04)" — that differentiation did **not** hold at higher n. The flag rate is high-variance (across r7–r12 + a controlled A/B it swings 3/3 → 0/3 → 4/6 → 0/3), so it is not a replicated *prevention* by any one config; the grade here rests on the reproduced failure, not on the retracted differentiation claim. (Source correction: rules-with-receipts `eval-results-v2/REGRESSION-20260708-r10r12.md`.) Whether the failure still reproduces on the current baseline — which sometimes flags the bug unaided — is an open grade-review item, not settled here.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
