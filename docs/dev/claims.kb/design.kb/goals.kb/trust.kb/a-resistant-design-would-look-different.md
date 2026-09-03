---
label: RESISTANT_DESIGN_DIFFERS
standing: user
authority: 'owner ruling 2026-08-29: "if we want to protect against a
  malicious claude, none of this is sufficient. And so we either need
  something that looks wholly unlike claude-code or admit security
  isn''t what we''re doing here." Revisit condition: wanting that other
  design.'
why:
  - an-agent-that-writes-scripts-is-already-inside.md
---

# A design that resisted a malicious agent would look wholly unlike this one

A design that actually resisted a malicious agent would have to deny
it the tools this one grants — no scripts, no unreviewed Bash. That is
a different product, not a hardened version of this one, and no
increment of markers, wrappers, or allowlists converts one into the
other.

So the revisit condition for FOOLPROOFING is not a newly imagined
attack or a tighter rule; it is wanting that other design. Until
someone does, a proposal justified by what a hostile agent could do is
answering a question this design does not ask.
