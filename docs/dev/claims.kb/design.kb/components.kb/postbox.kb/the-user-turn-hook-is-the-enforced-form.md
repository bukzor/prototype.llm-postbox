---
label: TURN_HOOK
standing: agent
why:
  - ../../goals.kb/delivery.kb/delivery-is-a-read-at-a-task-boundary.md
  - ../../goals.kb/delivery.kb/notification-carries-the-pointer.md
  - ../../experience.kb/hook-output-is-re-read-every-turn.md
---

# The user-turn hook is the enforced form

The eventual mechanical form of PULL_DELIVERY: a prompt-time hook
injects unread-mail pointers at the turn boundary, so that "rewind to
just before receipt" would hold by construction rather than by
convention. That it does is the REWIND probe, not yet run. It
must stay silent when the inbox is empty, because whatever it adds is
re-read on every later turn at a measured factor near 300
(HOOK_NOISE), and it never injects bodies (POINTERS_ONLY).
