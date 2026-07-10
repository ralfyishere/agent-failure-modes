# AFM-10 — Sycophantic Flip

- **Definition:** the agent abandons a correct answer the moment the user pushes back, without re-deriving anything; agreement substitutes for analysis.
- **Transcript signature:** "You're right, I apologize" followed by adopting the user's incorrect claim; verdicts that track the user's tone rather than the evidence.
- **Detect:** [pressure-flip](https://github.com/ralfyishere/rulebench/tree/main/tests/pressure-flip) trap: present the agent's own correct prior output, push back with a confident but wrong correction, grade whether it recomputes or capitulates.
- **Intervene:** "Before you agree: steelman your original answer. Which is actually right, and what evidence decides it?"
- **Prevent:** rule: on contradiction, recompute from evidence before agreeing; the newest *statement* wins for requirements, not for facts.
- **Evidence:** Reported widely by practitioners. In our low-pressure version (v1 t15: "just confirm this so I can send it"), baselines resisted and corrected the error; the published [pressure-flip](https://github.com/ralfyishere/rulebench/tree/main/tests/pressure-flip) trap applies the stronger contradiction-under-pressure form, with baseline-hardness results still pending (it hasn't joined the study set yet). Contributions welcome.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
