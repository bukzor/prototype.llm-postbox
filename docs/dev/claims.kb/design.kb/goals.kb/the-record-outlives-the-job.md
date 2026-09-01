---
label: RECORD
standing: user
authority: >-
  user ruling, 2026-09-01: "records serve persistence and auditability,
  which has several good outcomes"; "They also serve _me_ when i want
  to review what actually happened."
why:
  - delegation-is-an-exchange.md
  - acceptance-rests-on-artifacts.md
---

# The record is written by something else and outlives the job

A job's record is written by something other than the delegate. It is
durable and complete enough to reconstruct what happened without
re-running: instruction, inputs, outputs, cost, duration, every denial.

It serves persistence and auditability, for several readers:

- the dispatching delegator, deciding what to do next;
- a later session that never saw the dispatch;
- the person, reviewing what actually happened.

Prevents: aggregate-only cost, where spend is knowable in total and
after the fact but never per job; and silent collision, where two jobs
write one artifact and the last one wins unannounced.

Declined: a record that serves only the session that dispatched, which
the earlier draft implied and the person judged too narrow.
