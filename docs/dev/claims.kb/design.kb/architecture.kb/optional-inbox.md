---
label: INBOX
standing: user
todo: true
authority: >-
  user ruling, 2026-09-01: "I envision an optional scheme where we ask
  sub-agent to Monitor(inotifywait ./inbox/)."
why:
  - ../goals.kb/lifecycle-without-cooperation.md
  - ../goals.kb/conversation-is-not-result.md
---

# An inbox is the optional cooperative channel

A delegate may watch an inbox, and a delegator reaches it by writing a
message there. This is LIFECYCLE's soft-control layer and CONVERSE's
channel toward the delegate, realized on the filesystem the substrate
already provides. It is optional: a delegate that does not watch its
inbox is still killable and reapable by the hard controls.

How the delegate watches is a components question; the person's sketch
is a monitor over an inotify wait on the inbox directory.
