---
label: OPT_IN_INTERRUPT
standing: agent
why:
  - notification-carries-the-pointer.md
---

# Interruption is the receiver's choice

A recipient that chooses to be interruptible may arm a monitor on its
own inbox (inotify or poll), emitting pointers per POINTERS_ONLY. The
polarity is the commitment: interrupt power belongs to the receiver,
and no mechanism hands it to the sender.
