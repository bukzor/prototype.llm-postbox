---
label: PULL_DELIVERY
standing: user
authority: owner-ratified direction, 2026-08-28 (the transport decision
  point, ../../../../../design.kb/transport.md)
why:
  - push-delivery-is-the-root-cause.md
  - ../mutable-until-read.md
---

# Messages are files; delivery is a Read at a task boundary

A message is a file in the recipient's inbox; sending is writing it;
receiving is a deliberate Read at a task boundary — task start, task
end, or the owner's "check mail" — never mid-task. The declined
alternatives are the push transports
(`../../../../../design.kb/transport.kb/`). Pull gives receive-consent (the
recipient chooses the moment), batches queued mail at one boundary
instead of interrupting serially, and makes receipt an ordinary tool
call in an ordinary turn — which is what lets /rewind excise it.
