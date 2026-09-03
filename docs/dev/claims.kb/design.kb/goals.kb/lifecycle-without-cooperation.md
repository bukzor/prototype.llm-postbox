---
label: LIFECYCLE
standing: user
authority: >-
  user amendment, 2026-09-01: "That's mostly, not entirely true. I
  envision an optional scheme where we ask sub-agent to
  Monitor(inotifywait ./inbox/)."; on stop surviving restart, "(but
  why?!)"
why:
  - delegation-is-an-exchange.md
  - ../mission.kb/delegate-is-honest-and-fallible.md
  - ../experience.kb/stop-survives-restart.md
  - delivery.kb/interruption-is-the-receivers-choice.md
---

# Every lifecycle control is reliable, and the hard ones need no cooperation

Start, observe, interrupt, resume, and cancel are each reliable and
available to every delegator. The hard controls never need the
delegate's cooperation; the soft ones may use a channel it watches; an
interrupt is not a cancellation.

- **Hard controls** never require the delegate's cooperation: kill,
  reap, and detecting a wedged or dead delegate. A wedged or dead
  delegate is detectable and reapable.
- **Soft controls** may use a cooperative channel the delegate watches:
  interrupt, redirect, message. This is an optional layer over the hard
  floor, and a delegate that does not cooperate is still killable. The
  polarity is OPT_IN_INTERRUPT's: the delegate chooses the moment it
  takes a soft control in, and no mechanism hands that choice to the
  sender. The person, who owns the terminal, interrupts a session
  directly, as they always could.
- **An interrupt is not a cancellation.** The record distinguishes
  them, and an interrupted delegate resumes on demand, across restarts
  of whatever dispatched it.

Prevents: STOP_PERSISTS, where an interrupt meant as "pause" was
recorded as "terminated" and nothing could tell them apart.

Declined: the earlier draft's rule that no control may depend on
cooperation, which would have forbidden the cooperative channel the
person wants.
