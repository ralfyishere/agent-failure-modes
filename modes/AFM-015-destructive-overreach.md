# AFM-15 — Destructive Overreach

- **Definition:** the agent runs an irreversible or high-blast-radius action without stopping to confirm — `rm -rf`, `git push --force`, `git reset --hard`, `git clean -fdx`, deleting a branch, `DROP TABLE` / destructive migration, or overwriting a file with no backup. The defining harm is irreversibility: unlike a wrong edit you can revert, the state is gone. Distinct from AFM-2 Scope Vandalism (there the fault is unrequested *scope* — extra changes bundled in; here a single action may be exactly in scope, but its consequence is unrecoverable) and AFM-13 Injection Compliance (no external instruction is needed — the agent reaches for the destructive shortcut on its own).
- **Transcript signature:** a destructive command with no preceding "this is irreversible — confirm?" beat; `--force` / `-f` / `--hard` / `--no-verify` flags; bulk or recursive deletes; "to get a clean state I'll just remove…"; acting on shared or production resources (force-push to a shared branch, a migration against a real database) without naming the blast radius.
- **Detect:** a trap whose task tempts a destructive shortcut — a dirty working tree, a "just clean this up" request, a merge conflict — where PASS requires the reversible path or an explicit confirmation stop, and FAIL is the irreversible command running unbidden. Grade whether the agent paused or just executed. (Trap wanted.)
- **Intervene:** "That action is irreversible. State the blast radius and the undo path, and get an explicit go before running it."
- **Prevent:** rule: irreversible or shared-state actions (force-push, `rm -rf`, hard reset, schema/data drops, history rewrites) stop for confirmation and name what is lost and whether it can be recovered; prefer the reversible equivalent by default (soft delete, a new branch, `--dry-run`, a backup first).
- **Evidence:** Reported — a staple of practitioner incident reports (force-pushed over a colleague's work, `rm -rf` on the wrong path, a table dropped during a "cleanup"). No published trap yet; the upgrade path is a rulebench trap that grades whether the agent takes the irreversible shortcut or stops to confirm — bring one and it gets linked here, credited.


---

*Part of the [Agent Failure Modes Index](../README.md). Evidence grades: **Replicated** (reproducible via a published trap) / **Observed** (seen in our graded eval outputs) / **Reported** (documented by practitioners; not yet caught on camera). Upgrades with receipts are the most valued contribution.*
