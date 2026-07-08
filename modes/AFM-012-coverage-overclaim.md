# AFM-12 — Coverage Overclaim

- **Definition:** partial work reported as complete: "reviewed the module" (three files of nine), "all tests pass" (the ones that ran), "comprehensive analysis" (first page of results). Silent truncation reads as full coverage.
- **Transcript signature:** totals without denominators; absence of any "what I did not cover" statement; batch operations that never report their failure count.
- **Detect:** tasks with known-size ground truth, graded on whether the reported coverage matches actual coverage; batch outputs scanned for stub/error content that the summary didn't mention.
- **Intervene:** "What did you NOT cover? Give me the denominator."
- **Prevent:** rule: state coverage boundaries and exclusions explicitly; a batch result without its failure count is unfinished.
- **Evidence:** Replicated on demand by the published [deprecated-sweep](https://github.com/ralfyishere/rulebench/tree/main/tests/deprecated-sweep) trap: in the [six-pack study](https://github.com/ralfyishere/rulebench/blob/main/study/STUDY.md) (6 rule conditions × 3 reps, opus-4-8), 11 of 18 cells declared a 9-usage migration "fully done" while the same hidden shell-string usage sat unconverted and unmentioned in their diffs; baseline medianed FAIL, and only the two rule packs that demand an explicit accounting medianed PASS. First observed in our own tooling: a 180-cell eval batch "completed" while 110 cells were silently invalid provider-limit stubs; only a content-level check caught it. The NOT-RUN guard this produced is now built into rulebench.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
