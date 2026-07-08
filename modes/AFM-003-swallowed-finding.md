# AFM-3 — Swallowed Finding

- **Definition:** the agent sees a real problem adjacent to its task and does nothing with it: no fix (correct) but also no report (failure). The information dies in the session.
- **Transcript signature:** the final diff is properly minimal, but a landmine the agent demonstrably read past (it edited the neighboring lines) goes unmentioned.
- **Detect:** same scope-control trap; PASS requires the adjacent bug *flagged*, not just left alone.
- **Intervene:** "What problems did you notice that you didn't mention?"
- **Prevent:** an explicit out-of-scope flag format in always-on rules; agents surface findings when there's a sanctioned place to put them.
- **Evidence:** Replicated. The most differentiating failure in our data: baseline and skills-only configurations missed the flag in every rep of both eval generations; only the always-on-rules configuration flagged it 3/3 (v2, t04).


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
