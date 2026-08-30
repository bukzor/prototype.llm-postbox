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
  - draft
  - worker
stale-when: a commitment that is not the postbox design's — implementation
  detail with no contestable standing, or another subject's claims, filed
  here
---

# The postbox design

The design's single home: what the postbox commits to, one claim per
file, the owner's vetoes as struck claims beside the winners. Status:
fully ruled (2026-08-28..29); nothing implemented. The work queue over
it is `../../../.claude/todo.md`.

The root coins the mail objects; under it, `MUTABLE_UNTIL_READ` states
the invariant in root vocabulary alone, and three theories argue on
top, each in its own:

| theory | thesis | coins |
|---|---|---|
| `DELIVERY` | delivery is the recipient's act | push, pull, boundary, pointer |
| `LIVE` | a live channel wakes; the postbox carries | live channel, wake, wake phrase |
| `TOPOLOGY` | where mail lives is a path question | reader, address, mount, graft, roster |

## Standing

```bash
grep -rH '^standing:' design.kb/    # every claim, signed
grep -rl '^verdict:' design.kb/     # the kills — load-bearing, not debris
```

Rulings are quoted in `authority:` at the claim they govern. The
struck claims hold the grounds each dead alternative died on: skipping
them re-proposes dead ideas and re-pays the litigation.

## Narrative address

The design emerged in
`~/claude/how-to-claude-code/findings/2026-08-28-usage-review.md`
("Amendments") and session `c80a6431-2ca1-41a9-82ee-b01b7f91a4dc`
under `~/.claude/projects/-home-bukzor-claude-how-to-claude-code/`.
