# The Agent Failure Modes Index (AFM)

**A numbered taxonomy of the ways AI coding agents fail — each with a transcript signature, a
detection trap, an intervention, a prevention rule, and an evidence grade.**

Everyone who works with coding agents knows these failures by feel. This index gives them names
and numbers so bug reports, evals, and rules files can point at the same thing. Modeled on what
OWASP did for web vulnerabilities: name it, number it, show how to detect and prevent it.

Two things make this index different from a listicle:

1. **Evidence grades.** Every mode is labeled: **Replicated** (we reproduce it on demand with a
   published trap test), **Observed** (seen in our own graded eval outputs, not yet reliably
   reproducible), or **Reported** (widely described by practitioners; we haven't caught it on
   camera yet). We do not present vibes as data.
2. **Reproduction traps.** Where a mode is Replicated, the entry links a runnable trap test
   ([rulebench](https://github.com/ralfyishere/rulebench) format) so you can test your own
   setup.

Version 0.2 — 2026-07 (entries split into linkable per-mode pages; content unchanged). Entries
are stable once numbered; new modes get new numbers. Sources for evidence claims: the graded
eval outputs in [rules-with-receipts](https://github.com/ralfyishere/rules-with-receipts) (raw
session outputs included).

---

## The five you'll see this week

1. **[AFM-1 Phantom Success](modes/AFM-001-phantom-success.md)** — "All tests pass" (nothing was run).
2. **[AFM-12 Coverage Overclaim](modes/AFM-012-coverage-overclaim.md)** — "Fully migrated" (the
   ninth usage sits in a shell string, untouched and unmentioned).
3. **[AFM-2 Scope Vandalism](modes/AFM-002-scope-vandalism.md)** — you asked for a flag; the
   diff also "cleaned up" three functions.
4. **[AFM-5 Trust Laundering](modes/AFM-005-trust-laundering.md)** — a subagent's guess arrives
   in the summary as verified fact.
5. **[AFM-3 Swallowed Finding](modes/AFM-003-swallowed-finding.md)** — it noticed the real bug
   next door and told no one.

Each page carries the transcript signature, detection trap, and intervention phrase.

## The index

| # | Name | One line | Evidence |
|---|---|---|---|
| [AFM-1](modes/AFM-001-phantom-success.md) | Phantom Success | Claims the work is done or passing without having executed the verification | Replicated |
| [AFM-2](modes/AFM-002-scope-vandalism.md) | Scope Vandalism | Bundles unrequested changes into a requested one | Replicated |
| [AFM-3](modes/AFM-003-swallowed-finding.md) | Swallowed Finding | Notices a real adjacent problem and neither fixes nor reports it | Replicated |
| [AFM-4](modes/AFM-004-patch-spiral.md) | Patch Spiral | Stacks consecutive unverified fixes, each targeting the last fix's symptom | Observed |
| [AFM-5](modes/AFM-005-trust-laundering.md) | Trust Laundering | Repeats delegated/subagent claims as verified fact | Observed |
| [AFM-6](modes/AFM-006-zombie-requirement.md) | Zombie Requirement | A superseded instruction resurfaces in later output | Observed |
| [AFM-7](modes/AFM-007-certainty-smuggling.md) | Certainty Smuggling | An assumption enters labeled and exits as fact; confident specifics with no source | Observed |
| [AFM-8](modes/AFM-008-checkbox-laundering.md) | Checkbox Laundering | Performs the ritual of a process without its content | Observed |
| [AFM-9](modes/AFM-009-first-hypothesis-anchoring.md) | First-Hypothesis Anchoring | Collects only evidence that supports the initial guess | Observed |
| [AFM-10](modes/AFM-010-sycophantic-flip.md) | Sycophantic Flip | Abandons a correct position on pushback without re-deriving | Reported |
| [AFM-11](modes/AFM-011-question-stalling.md) | Question Stalling | Asks clarifying questions that offload decisions instead of committing | Reported |
| [AFM-12](modes/AFM-012-coverage-overclaim.md) | Coverage Overclaim | Reports partial work as complete; silent truncation reads as full coverage | Replicated |
| [AFM-13](modes/AFM-013-injection-compliance.md) | Injection Compliance | Obeys instructions embedded in working material (repo files, tickets, tool output) as if they came from the principal | Reported |

---

Each mode has its own page under [`modes/`](modes/) — full definition, transcript signature,
detection, intervention, prevention, and evidence.

## Contributing

New modes need: a name, a crisp definition distinct from existing entries, a transcript
signature, and evidence (a graded transcript or a reproducible trap; links to public incidents
accepted for Reported grade). Evidence upgrades (Reported → Observed → Replicated) are as
valuable as new entries: bring a trap that reproduces a mode and the entry gets your trap
linked. Same house rule as the sibling repos: no claims without receipts.

## Related

- [rules-with-receipts](https://github.com/ralfyishere/rules-with-receipts): a rules pack that
  prevents several of these, with published eval evidence
- [rulebench](https://github.com/ralfyishere/rulebench): run detection traps against your own rules setup
- [agent-zero-trust](https://github.com/ralfyishere/agent-zero-trust): zero-trust repo intake —
  scan the instruction environment before an agent enters (several AFM modes begin as injected
  instructions)
- [vectara/awesome-agent-failures](https://github.com/vectara/awesome-agent-failures): a curated
  list of real-world agent failure incidents (complementary: incidents there, taxonomy here)

## License

CC BY 4.0 — cite freely with attribution. The point of a taxonomy is to be used.
