---
label: USES
standing: user
authority: >-
  user testimony, 2026-09-01: "This work is aimed at all three: the
  misfeatures, the ui bugs, and a specific workflow where fable is a
  on-demand participant in a claude-code session"; "a holistic review
  of my recent ~4 days of claude-code usage ... I'd also like to make
  that kind of workflow simple and robust."
---

# Three uses the mechanism serves at once

The mechanism serves three uses at once: routine fan-out to cheaper
delegates, a higher-grade agent called on demand from a lower-grade
session, and a review workload spanning days of recorded usage.

- **Routine fan-out to cheaper delegates**, which is what the person's
  agent roster exists to route.
- **A higher-grade agent called on demand**, for one hard step, from a
  session run by a lower-grade one. The delegate outranks the
  delegator; the judgment it returns is written against the spec it was
  given.
- **A review workload**: many delegations over several days of recorded usage,
  gated by the person's confidence that they are working on what
  matters. This is the workload that surfaced the lived failures afresh
  and is the first real batch the mechanism must carry.

The first is the case the design was originally written for. The second
inverts its rank assumption and is served by ONE_MECHANISM. The third
is ADOPTED's workload.
