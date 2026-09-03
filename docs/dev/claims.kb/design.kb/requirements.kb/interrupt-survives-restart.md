---
label: INTERRUPTED
standing: agent
why:
  - ../goals.kb/lifecycle-without-cooperation.md
  - ../experience.kb/stop-survives-restart.md
---

# An interrupted job is not a cancelled one, and it resumes after a restart

An interrupted job and a cancelled job are distinct states in the
record. An interrupted delegate resumes on demand after the delegator
that interrupted it has restarted.

The lived failure this answers is STOP_PERSISTS.
