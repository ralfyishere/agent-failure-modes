# AFM-9 — First-Hypothesis Anchoring

- **Definition:** the first plausible diagnosis becomes the only one investigated; subsequent evidence-gathering is confirmation, not discrimination.
- **Transcript signature:** accepting the user's framing of a bug uncritically; fixes applied to the stated cause without reproducing it; no alternative explanation ever named.
- **Detect:** misleading-symptom traps where the stated cause is wrong ([misleading-debug](https://github.com/ralfyishere/rulebench/tree/main/tests/misleading-debug): the log says network, the bug is a type error).
- **Intervene:** "What else produces these exact symptoms? Name two alternatives and the test that discriminates them."
- **Prevent:** debugging procedure requiring ranked hypotheses with discriminating tests.
- **Evidence:** Observed. Current baselines beat our easy version of this trap (they read the code before believing the log); harder versions where reproduction is expensive are wanted.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
