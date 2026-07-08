# Security

This repo is a taxonomy — documentation only, no executable code, nothing to
install. Two things still matter:

1. **Detection traps are instructions for agents.** If you copy a trap into
   your own eval setup, read it first like any rules file (see
   [rulebench vet](https://github.com/ralfyishere/rulebench)). Trap fixtures
   deliberately contain misleading content — that's their job; keep them in
   isolated workspaces.
2. **Reporting:** factual errors or a misleading entry — open an issue.
   Something sensitive (e.g., an entry that could be read as an attack recipe
   rather than a detection aid): use GitHub's private vulnerability reporting.

This index documents how agents FAIL so the failures can be caught. It is not
a playbook for inducing them in systems you don't own.
