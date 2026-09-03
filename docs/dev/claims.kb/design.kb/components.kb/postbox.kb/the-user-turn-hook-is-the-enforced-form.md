---
label: TURN_HOOK
standing: agent
why:
  - ../../goals.kb/delivery.kb/delivery-is-a-read-at-a-task-boundary.md
  - ../../goals.kb/delivery.kb/notification-carries-the-pointer.md
---

# The user-turn hook is the enforced form

The eventual mechanical form of PULL_DELIVERY: a prompt-time hook
injects unread-mail pointers at the turn boundary, so "rewind to just
before receipt" holds by construction rather than by convention. It
must stay silent when the inbox is empty — hook noise was measured at
3.5 Mtok over three weeks — and it never injects bodies
(POINTERS_ONLY).
