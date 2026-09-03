---
label: HOOK_NOISE
standing: bare
verify: |-
  bin/hook-noise 21: over every transcript under ~/.claude/projects
  touched in the last 21 days, sums what hooks added to context, once
  as written and once multiplied by the assistant turns that followed
  in the same session. Run 2026-09-03: 386 transcripts, 52,573
  assistant turns; no hook injected context of its own; the Bash
  preamble's trace lines inside tool results came to 1.6 Mtok written
  and 468 Mtok re-read.
---

# Hook output is paid once to write and on every later turn to re-read

A substrate fact. Whatever a hook adds to a session's context stays in
the transcript, so the model reads it again on every turn that
follows. Over three weeks of this person's transcripts the one hook
that adds text, the Bash preamble's trace lines, wrote 1.6 Mtok and
was re-read to 468 Mtok, a factor near 300. Cache pricing makes each
re-read cheap, and the total is still the largest line item the hook
incurs.

So a hook that fires every turn must add nothing when it has nothing
to say: a line announcing that there is nothing to read costs its
length times the rest of the session, in every session.
