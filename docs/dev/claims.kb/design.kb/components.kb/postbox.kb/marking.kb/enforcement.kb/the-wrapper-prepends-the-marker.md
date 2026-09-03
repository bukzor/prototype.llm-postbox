---
label: WRAPPER_MARKS
standing: user
todo: true
authority: 'owner proposal 2026-08-29, accepted as the probationary plan
  of record: "a simple claude-sub-agent script that prepends our callout
  tag to input, and is preapproved for Bash()."'
---

# The wrapper prepends the marker to everything it sends

A `claude-sub-agent` script is how an agent starts or messages another
session, and it prepends `<callout tag="@claude"/>` to every payload
it passes on. The sender never types the marker, so the sender cannot
forget it.

The plan is probationary: it is accepted as the thing to build, and it
is the first place to look if the marking convention turns out to
misfire in practice.
