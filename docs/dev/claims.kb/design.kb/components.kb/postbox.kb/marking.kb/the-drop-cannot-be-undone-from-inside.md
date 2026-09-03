---
label: MONOTONE
standing: bare
why:
  - capture-extends-through-nested-callouts.md
  - the-marker-is-a-privilege-drop.md
---

# The drop cannot be undone from inside

Capture swallows later markers (CAPTURE_NESTS) and every marker lowers
authority (DROP), so nothing written inside a capture can raise the
authority of what comes after it. Authority within a captured region
is monotonically non-increasing.

Two things follow: a sender cannot escalate by composing markers, and
a reader never has to compute a net level — the outermost marker is
the answer.
