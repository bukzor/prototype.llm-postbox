---
label: POSTBOX
standing: agent
ontology:
  - postbox
  - message
  - sender
  - recipient
  - inbox
  - read
  - record
stale-when: a commitment that is not the postbox design's — implementation
  detail with no contestable standing, or another subject's claims, filed
  here
---

# The postbox design, as a ledger

`design.kb/` holds what the design commits to, one claim per file with
its label and standing. The design prose — the convention, its
`[!TODO]` surface, the transport decision point and its kill records —
is `../../../design.kb/` at the repo root; this ledger is the standing
behind that prose, and the place to argue with it.

The root coins the mail objects; under it, `MUTABLE_UNTIL_READ` states
the invariant in root vocabulary alone, and three theories argue on
top, each in its own:

| theory | thesis | coins |
|---|---|---|
| `DELIVERY` | delivery is the recipient's act | push, pull, boundary, pointer |
| `LIVE` | a live channel wakes; the postbox carries | live channel, wake, wake phrase |
| `TOPOLOGY` | where mail lives is a path question | reader, address, mount, graft |

## Standing

```bash
grep -rH '^standing:' design.kb/    # every claim, signed
grep -rl 'verdict:' design.kb/      # what a judgment took out of force
```

Three claims carry the owner's `!` — the invariant
(`MUTABLE_UNTIL_READ`), the transport direction (`PULL_DELIVERY`), the
runtime root (`RUNTIME_ROOT`) — each naming its ruling in `authority:`.
The `agent` set is the veto surface: judgments made on the owner's
behalf, standing until vetoed. The bare set is facts and derivations;
arguing with one means arguing with its premises or its check.
