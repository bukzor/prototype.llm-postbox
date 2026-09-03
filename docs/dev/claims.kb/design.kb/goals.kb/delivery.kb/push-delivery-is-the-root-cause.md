---
label: PUSH_ROOT_CAUSE
standing: agent
why:
  - ../../experience.kb/receiving-is-ungated.md
  - ../../experience.kb/push-messaging-bit-three-ways.md
---

# The vetoed failure modes are one choice: push-into-context

The owner's three grounds for declining SendMessage — inane sends,
recipient distraction, unrewindable receipt (quoted verbatim in
SENDMESSAGE) — are each a
consequence of push-into-context delivery. Inane sends are cheap
because the sender needs no consent to occupy the recipient's context;
distraction is guaranteed because delivery is an interrupt; rewind
cannot excise a message that was never a discrete, skippable event.
With receiving ungated, no configuration rescues push; inverting to
pull dissolves all three at once rather than patching them severally.
