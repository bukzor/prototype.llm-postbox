---
label: DEGRADED
standing: bare
why:
  - tui-default-refused.md
  - escape-opens-agent-list.md
  - rewind-does-nothing-useful.md
  - resume-by-id-refused.md
  - branch-may-not-work.md
  - stop-survives-restart.md
  - interrupt-stops-orchestrator.md
  - fork-distracts-mother.md
  - distracted-by-cwd.md
  - output-arrives-unbidden.md
---

# Six of the ten lived failures are session capabilities an agent lacks

Six of the ten lived failures are capabilities a session has and an
agent lacks; two are the person's controls fused with the
orchestrator's; one is an unconfined view; one is output forced into
attention.

Sorted by what each is a failure *of*:

- **Six are capabilities a session has and an agent lacks:** the tui
  setting (TUI), undo by escape (ESC), rewind itself (NO_REWIND),
  resume by id (NO_RESUME), branching (NO_BRANCH, unconfirmed), and
  surviving a restart (STOP_PERSISTS). An agent is a degraded session.
- **Two are the person's controls fused with the orchestrator's:** an
  interrupt reaching both (STOP_PROPAGATES), a fork's activity reaching
  its mother (FORK_LEAKS).
- **One is an unconfined view:** extraneous files in sight (DISTRACTED).
- **One is output forced into attention:** (FORCED_OUTPUT).

This stands bare: it is a classification of the listed claims, checkable
by reading them, and needs no judge.
