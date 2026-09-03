---
label: DELIVERY
standing: agent
ontology:
  - inbox
  - push
  - pull
  - task boundary
  - pointer
why:
  - mutable-until-read.md
  - output-is-offered-never-forced.md
  - conversation-is-not-result.md
---

# Delivery is the recipient's act

How a message moves: the sender only ever writes; everything after —
when the message enters a context, and as what — is the recipient's
act. Push and pull name the two answers, and the claims here argue
that pull is the only one the invariant, MUTABLE_UNTIL_READ, survives.
An inbox is the directory a recipient reads from, and a delegator
writes there to reach it. A task boundary is the moment the recipient
chooses; a pointer is what may travel without consent where a body may
not.

This theory sits under the goals because it states properties any
channel must have, not how the postbox has them. It is the
message-channel instance of OFFERED: what a job returns is offered,
and so is what a delegator sends.
