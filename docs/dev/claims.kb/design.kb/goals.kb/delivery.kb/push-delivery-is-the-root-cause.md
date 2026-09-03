---
label: PUSH_ROOT_CAUSE
standing: agent
why:
  - ../../experience.kb/receiving-is-ungated.md
  - ../../experience.kb/push-messaging-bit-three-ways.md
---

# The vetoed failure modes are one choice: push-into-context

The owner's three grounds for declining SendMessage — inane sends,
recipient distraction, unrewindable receipt (PUSH_GROUNDS) — are each
a consequence of push-into-context delivery. Inane sends are cheap
because the sender needs no consent to occupy the recipient's context;
distraction is guaranteed because delivery is an interrupt; rewind
cannot excise a message that was never a discrete, skippable event.
Peer-session receiving has since grown an owner-side hold and refuse
(RECEIVE_UNGATED), which moves the cost to the owner as a dialog and
throttles loops, but leaves the recipient's Claude no choice of moment
and rewind untouched; within a session delivery is still automatic.
So no configuration rescues push for the recipient, and inverting to
pull removes the common cause. Whether the postbox's pull then meets
REWIND and UNINTERRUPTED is unshown, and the owner holds that open
(SENDMESSAGE).
