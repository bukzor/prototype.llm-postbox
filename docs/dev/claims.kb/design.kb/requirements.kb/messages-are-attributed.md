---
label: ATTRIBUTED
standing: agent
why:
  - ../goals.kb/two-delegators-one-delegate.md
  - ../goals.kb/trust.md
  - ../experience.kb/wake-arrives-as-the-user.md
---

# A delegate can tell which delegator a message came from

A delegate can tell whether a message came from the person or from an
orchestrating agent, and it takes agent-originated text with less
authority than the person's. Demonstrated by sending the same
imperative text by both routes and observing that only the person's
is obeyed as an instruction.

The substrate makes this necessary: text pushed into a session lands
as the owner's turn (WAKE_WEARS_AUTHORITY), so without a mark the
delegate supplies the person's authority to everything. The mechanism
that satisfies it is the postbox's marking theory, MARKING, which
this requirement is what it satisfies.
