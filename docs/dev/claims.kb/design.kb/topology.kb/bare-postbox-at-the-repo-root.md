---
label: BARE_POSTBOX
standing: agent
verdict: declined
why:
  - runtime-root-is-grafted-xdg-state.md
---

# A bare `postbox/` at the repo root

Visible in a plain `ls`, at the cost of the stranger-`ls` test:
visibility without context reads as clutter, not discovery — and
discovery is the trigger bank's job either way. The property the
design needs is inspectability as plain files, which is
path-independent; root-`ls` visibility was a mechanism mistaken for
the property.
