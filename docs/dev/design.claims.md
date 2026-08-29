---
label: POSTBOX
standing: agent
ontology:
  - read
  - record
  - inbox
  - boundary
  - live channel
  - wake phrase
  - address
  - postbox
stale-when: a commitment that is not the postbox design's — implementation
  detail with no contestable standing, or another project's claims, filed
  here
---

# The postbox design, as a ledger

`design.claims.kb/` holds what the design commits to, one claim per
file with its label and standing. `../../design.kb/` is the design
prose — the convention, its `[!TODO]` surface, the transport decision
point and its kill records; this ledger is the standing behind that
prose, and the place to argue with it.

One theory, this file: the claims share one vocabulary, and no
subsection yet supports a second citing theory. Nesting begins when
that stops being true, not when the list grows long.

## Standing

```bash
grep -rH '^standing:' design.claims.kb/    # every claim, signed
grep -rl 'verdict:' design.claims.kb/      # what a judgment took out of force
```

Three claims carry the owner's `!` — the invariant, the transport
direction, the runtime root — each naming its ruling in `authority:`.
The `agent` set is the veto surface: judgments made on the owner's
behalf, standing until vetoed. The bare set is facts and derivations;
arguing with one means arguing with its premises or its check.
