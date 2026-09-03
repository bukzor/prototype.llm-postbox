---
label: RESUMES_FORK
standing: bare
verify: |-
  bin/two-resumes-one-session: seeds a throwaway haiku session, runs
  two `claude -p --resume` on it concurrently, then resumes a third
  time asking for every reply so far. Both writers exit 0, the
  transcript stays valid JSONL, and the third resume reports the
  last-written branch only ("seed, bravo", never "seed, alpha,
  bravo"). Run 2026-09-03 against claude 2.1.259; four haiku calls.
---

# Two concurrent resumes fork the transcript, and the next resume follows one branch

A substrate fact. Two `claude -p --resume <id>` processes on one
session both succeed and both append: each new turn parents on the
last line its process read at start, so the transcript holds two
branches under one session id. Nothing is corrupted and nothing
refuses. The next resume walks back from the last line written, so
one branch stays on disk and out of the conversation, silently.

The hazard is therefore a lost turn, not a crash: whichever writer
finished first has its exchange dropped from every later resume. A
resume racing a live process on the same session loses the same way,
and no lock exists, so whatever discipline keeps writers apart is the
caller's to supply.
