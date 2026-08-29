---
label: XDG_SPOOL
standing: agent
verdict: declined
why:
  - runtime-root-is-grafted-xdg-state.md
---

# An XDG `spool` slot

Semantically nearest — `spool` is what the mail tradition calls this
directory — but XDG defines no spool slot, and inventing one forfeits
the only thing following the standard buys. `state` is the closest
slot that exists.
