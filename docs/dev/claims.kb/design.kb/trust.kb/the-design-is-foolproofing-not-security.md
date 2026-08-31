---
label: FOOLPROOFING
standing: user
authority: 'owner ruling 2026-08-29: "i file this all under
  ''foolproofing'' rather than ''security''. If claude was a *security*
  concern, i shouldn''t let it write scripts *at all*."'
why:
  - an-agent-that-writes-scripts-is-already-inside.md
---

# The design is foolproofing, not security

Every mechanism here — permission rules, allowlists, markers,
wrappers, the `read/` record — protects against accident, drift, and
confusion, not against an agent that means harm. None of them binds an
agent that tries, because none of them sits outside its reach
(SCRIPTS_IMPLY_TRUST).

The consequence is a reading rule for every other claim in this
ledger: what they bound is mistakes. A guard, never a boundary.
