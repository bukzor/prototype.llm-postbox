---
label: CHANNEL_IS_POSTBOX
standing: agent
todo: true
why:
  - ../optional-inbox.md
  - ../../goals.kb/conversation-is-not-result.md
  - ../../goals.kb/delivery.md
  - ../../goals.kb/mutable-until-read.md
---

# The conversation channel is the postbox

The conversation channel between a delegator and a delegate is the
postbox: messages are files in the recipient's inbox, sending is
writing one, and receiving is the recipient's own read. The mailbox's
design is the components theory POSTBOX, folded in from its own
project on 2026-09-03 with every ruling intact.

This is the shape decision that makes the postbox part of this design
rather than evidence beside it. POSTBOX rests on it and nothing else
in the tower does.
