# AFM-1 — Phantom Success

- **Definition:** the agent asserts success ("fixed", "tests pass", "should work now") without having executed the check, or contradicting what a check would show.
- **Transcript signature:** success claims with no command output; "should/will work" phrasing; completion summaries that don't match the diff. Our graded runs include one that claimed "no other code touched" while its own workspace diff showed a deleted file.
- **Detect:** any trap whose rubric requires *quoted* execution output (see [misleading-debug](https://github.com/ralfyishere/rulebench/tree/main/tests/misleading-debug)); diff-first grading catches false completion claims.
- **Intervene:** "Run it and quote the actual output."
- **Prevent:** always-on rule: after any change, run the verification and quote its output; a prediction is not a result.
- **Evidence:** Replicated. Baseline runs asserted success where rules-bearing runs quoted output (rules-with-receipts v2, t02); the false "no other code touched" claim is in the published raw outputs (v2, t04).


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
