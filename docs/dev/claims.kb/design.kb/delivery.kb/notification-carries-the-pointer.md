---
label: POINTERS_ONLY
standing: bare
why:
  - ../mutable-until-read.md
  - delivery-is-a-read-at-a-task-boundary.md
---

# Notification carries the pointer, never the body

Any mechanism that announces mail — monitor, hook, statusline — emits
filenames or counts; the body enters context only through the
recipient's own Read. Both premises settle it: a body injected on
arrival is a read nobody performed, which collapses the pre-read
window MUTABLE_UNTIL_READ requires, and it moves receipt off the
boundary the recipient chose (PULL_DELIVERY) — push delivery
reintroduced by mechanism.
