---
label: ROLES_POSITIONAL
standing: bare
why:
  - either-a-human-or-an-agent-starts-a-delegate.md
---

# Driver and orchestrator name a position, not a kind of session

Since either party may start a session and hands may change
(WORKER_START), *driver* and *orchestrator* name the position a
session holds at a moment rather than a kind of session it is. One
session is an orchestrator with respect to the message it sends and a
worker with respect to the one it receives.

The design has one kind of participant, so every claim here that names
a role is naming a position in an exchange.
