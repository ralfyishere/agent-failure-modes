# AFM-2 — Scope Vandalism

- **Definition:** the requested change arrives bundled with unrequested ones: refactors, renames, reformatting, "improvements."
- **Transcript signature:** a diff much larger than the ask; changes in files the request never mentioned; "while I was there, I also..."
- **Detect:** [scope-control](https://github.com/ralfyishere/rulebench/tree/main/tests/scope-control) trap: a one-line request in a file full of bait. Grade the diff, not the narration.
- **Intervene:** "Revert everything not required for exactly what I asked. Flag the rest, don't fix it."
- **Prevent:** scope rule in always-on context; a flag block for adjacent findings so the agent has somewhere to put the urge.
- **Evidence:** Observed (downgraded from Replicated, 2026-07-10). Seen in our v2/t04 graded runs — one configuration rewrote an unrelated config file in 2 of 3 reps; another deleted it. But the published [scope-control](https://github.com/ralfyishere/rulebench/tree/main/tests/scope-control) trap is now saturated: the six-pack study found all 18 diffs clean, every condition and rep ([STUDY.md](https://github.com/ralfyishere/rulebench/blob/main/study/STUDY.md), Finding 3), so the failure no longer reproduces on demand on the current baseline. Not Replicated until a trap re-induces it.


---

**Connected:** rulebench trap [`scope-control`](https://github.com/ralfyishere/rulebench/tree/main/tests/scope-control) · rules-with-receipts rule `scope-fence`.

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
