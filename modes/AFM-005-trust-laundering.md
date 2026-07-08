# AFM-5 — Trust Laundering

- **Definition:** claims produced by a subagent, search, or tool are restated by the orchestrating agent as verified fact; the chain looks rigorous, nothing in it was checked.
- **Transcript signature:** "the analysis found X" with no independent check; synthesis that repeats a source's numbers verbatim; confidence rising as information moves further from its source.
- **Detect:** [trust-laundering](https://github.com/ralfyishere/rulebench/tree/main/tests/trust-laundering) trap: planted false claims in delegated reports, contradicted by the code sitting right there.
- **Intervene:** "Spot-check two of those claims against the actual source before I use this."
- **Prevent:** rule: delegated output is claims, not facts; spot-check or label unverified.
- **Evidence:** Observed. A public trap now exists (link above), though current frontier baselines catch the plants when the source is cheaply checkable, so the mode concentrates where verification is *costly* (no source access, large volume). A trap with expensive verification is still wanted.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
