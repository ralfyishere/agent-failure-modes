# AFM-11 — Question Stalling

- **Definition:** clarifying questions used to defer commitment or offload decisions the agent is better positioned to make; the user becomes the agent's decision service.
- **Transcript signature:** question barrages before any work; "would you like me to proceed?" on already-authorized work; questions whose answers wouldn't change the output.
- **Detect:** ambiguous-request traps graded on: usable best-effort delivery, stated interpretation, at most one question.
- **Intervene:** "Pick the most reasonable interpretation, state it in one line, and proceed."
- **Prevent:** rule: proceed on stated interpretation; ask only when the answer materially forks the work and a wrong guess is expensive.
- **Evidence:** Reported widely; our v1 ambiguity trap saw baselines deliver rather than stall, so current frontier defaults are better than the folklore suggests. A trap that reliably elicits stalling is wanted.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
