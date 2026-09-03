---
label: RETENTION
standing: open
why:
  - mutable-until-read.md
---

# The read record is permanent

Post-read mail is kept indefinitely: `read/` is an archive, and
cleanup tooling is permanently out of scope.

MUTABLE_UNTIL_READ makes post-read mail "immutable audit trail" but
rules nothing about duration; today keep-forever holds by omission
only. Candidates:

- **Sign** — permanence is itself a goal: the record joins the
  design's commitments, and a future cleanup proposal is
  non-conforming.
- **Strike** (`verdict: rejected`, body notes deferral) — retention
  is deferred past the prototype; `read/` growth is accepted until it
  hurts, and cleanup stays proposable.

Recommendation (agent): strike as deferred — nothing implemented yet
gives the question weight, and an unbounded archive nobody chose
should not harden into a commitment by silence.
