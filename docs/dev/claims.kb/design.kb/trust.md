---
label: TRUST
standing: agent
ontology:
  - foolproofing
  - guard
stale-when: claude-code grows a boundary the agent cannot reach around —
  a sandbox it cannot edit its way out of — which would make "security"
  the right word for this design after all
---

# What the mechanisms here are answerable to

Every mechanism in this design answers to foolproofing, not to
security. Foolproofing bounds accident, drift, and confusion; a guard
is a mechanism so bounded — it lowers the odds of a mistake and holds
nothing whatever against intent.

The distinction is a reading rule for the rest of the ledger: where a
claim elsewhere says a mechanism prevents something, what it prevents
is a mistake. The rest of this theory's work follows from that — which
objections are admissible (CONVENTION_PARITY), how to price a failure
(BLAST_RADIUS), and where the design's scarce effort belongs
(SPEND_AT_THE_OWNER).
