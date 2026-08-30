---
label: FOOLPROOFING
standing: user
authority: 'owner ruling 2026-08-29: "i file this all under
  ''foolproofing'' rather than ''security''. If claude was a *security*
  concern, i shouldn''t let it write scripts *at all*." Revisit
  condition: wanting a design that resists a malicious agent, which
  would look wholly unlike claude-code.'
---

# The design is foolproofing, not security

Every mechanism here — permission rules, allowlists, markers,
wrappers, the `read/` record — protects against accident, drift, and
confusion, not against an agent that means harm. An agent trusted to
write scripts and run Bash can reach whatever these mechanisms rest
on, so none of them binds one that tries; the design that resisted
that would refuse the agent such access, and would look wholly unlike
claude-code.

The consequence is a reading rule for every other claim here: what
they bound is mistakes. A guard, never a boundary.
