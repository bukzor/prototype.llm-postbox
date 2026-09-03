---
label: POSTBOX
standing: agent
ontology:
  - postbox
  - read record
  - draft
stale-when: >-
  a commitment here that is not the mailbox's own -- a delegation-level
  claim that belongs on a rung above, or implementation detail with no
  contestable standing
why:
  - ../architecture.kb/the-channel-is-the-postbox.md
  - ../goals.kb/delivery.md
  - ../goals.kb/trust.md
  - ../goals.kb/mutable-until-read.md
---

# The postbox

The conversation channel and the delegate's mailbox, realized as files
at a known address. A **postbox** is the directory tree that holds
every inbox; the **read record** is where consumed mail moves and
stays; a **draft** is mail composed but not yet visible to its reader.

This component implements what the rungs above it commit to. Which
message goes where and when it may be read is `../goals.kb/delivery.md`;
what the mechanisms here are answerable to is `../goals.kb/trust.md`;
the invariant every mechanism is checked against is MUTABLE_UNTIL_READ;
that the postbox is the channel at all is CHANNEL_IS_POSTBOX, the
architecture claim this theory hangs from and the one to strike if a
different shape wins.

Older claims here say *worker*, *orchestrator*, and *driver*. Those are
the mission's delegate and delegator by position (ROLES_POSITIONAL);
the words survive in rulings quoted verbatim and nowhere else are
stipulated.

Three theories argue on top, each in its own vocabulary:

| theory | thesis | coins |
|---|---|---|
| `TOPOLOGY` | where mail lives is a path question | address, mount, graft, roster |
| `LIVE` | a live channel wakes; the postbox carries | live channel, wake, wake phrase |
| `MARKING` | agent-authored text says so in the body | privilege drop, capture |

The claims at this level are the mailbox's own mechanics: the read
move (READ_MOVE), the draft stage (DRAFT_STAGE), retention
(RETENTION), send gating by path rules (SEND_GATED), the turn hook
(TURN_HOOK), and where integration artifacts land (INTEGRATION_HOME).

## Standing

```bash
grep -rH '^standing:' postbox.kb/         # every claim, signed
grep -rl '^verdict:' postbox.kb/          # the kills -- load-bearing, not debris
grep -rl '^standing: agent' postbox.kb/   # the owner's review queue
grep -rl '^todo: true' postbox.kb/        # decided, not yet built
```

Rulings are quoted in `authority:` at the claim they govern. The
struck claims hold the grounds each dead alternative died on: skipping
them re-proposes dead ideas and re-pays the litigation.

## Narrative address

The postbox design emerged in
`~/claude/how-to-claude-code/findings/2026-08-28-usage-review.md`
("Amendments") and session `c80a6431-2ca1-41a9-82ee-b01b7f91a4dc`
under `~/.claude/projects/-home-bukzor-claude-how-to-claude-code/`.
The `TRUST` and `MARKING` theories were argued on 2026-08-29 and filed
on 2026-08-31 (`../../../devlog/2026-08-31-000-Marking-and-trust-theories-filed.md`).
It was folded into the agent-harness design on 2026-09-03; the
promoted claims and the struck `AGENTS_INTERFACE` live on the rungs
above.
