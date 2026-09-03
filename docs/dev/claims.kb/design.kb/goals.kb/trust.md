---
label: TRUST
standing: agent
ontology:
  - foolproofing
  - guard
stale-when: claude-code grows a boundary the agent cannot reach around —
  a sandbox it cannot edit its way out of — which would make "security"
  the right word for this design after all
why:
  - ../mission.kb/delegate-is-honest-and-fallible.md
---

# What the mechanisms here are answerable to

Every mechanism in this design answers to foolproofing, not to
security. Foolproofing bounds accident, drift, and confusion; a guard
is a mechanism so bounded — it lowers the odds of a mistake and holds
nothing whatever against intent.

The distinction is a reading rule for the rest of the ledger: where a
claim elsewhere says a mechanism prevents something, what it prevents
is a mistake. That includes the harness goals that speak of
enforcement, CONFINE and EVIDENCE, and the requirements that probe
them, DENIAL and GRADER_SAFE: each is met by a mechanism an honest
delegate cannot stumble past, and none claims to bind one that tries.
The premise is the mission's HONEST; this theory is what it costs. The rest of this theory's work follows from that — which
objections are admissible (CONVENTION_PARITY), how to price a failure
(BLAST_RADIUS), and where the design's scarce effort belongs
(SPEND_AT_THE_OWNER).
