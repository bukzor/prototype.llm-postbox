---
label: OWNER_IS_THE_BOUNDARY
standing: agent
why:
  - the-design-is-foolproofing-not-security.md
---

# The owner is the only boundary the agent cannot reach around

Every constraint the agent places on itself is a guard: a script it
can edit, an allowlist it can propose, a marker it can omit. The
owner's attention is the one thing in the loop the agent cannot reach
around, which makes it this design's only boundary in the containing
sense — and the reason SEND_GATED spends an interactive prompt where a
silent rule would have been cheaper.

Pricing a guard as though it were a boundary is the error this claim
exists to forestall: it buys false confidence, and it spends effort at
points where no effort holds.
