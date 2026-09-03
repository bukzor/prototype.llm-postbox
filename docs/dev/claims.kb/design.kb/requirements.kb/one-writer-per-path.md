---
label: SOLE_WRITER
standing: agent
why:
  - ../goals.kb/the-record-outlives-the-job.md
---

# No two concurrent jobs write the same path

No two concurrent jobs can write the same output path. A collision is
refused at dispatch, never resolved by last-write-wins.
