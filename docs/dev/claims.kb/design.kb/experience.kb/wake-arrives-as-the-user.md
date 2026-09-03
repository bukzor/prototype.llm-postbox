---
label: WAKE_WEARS_AUTHORITY
standing: bare
authority: >-
  Claude Code docs, fetched 2026-09-03: "Run Claude Code
  programmatically" shows `claude -p "Continue that review" --resume
  "$session_id"`, the argument to -p being the prompt; by contrast
  "Message your other Claude Code sessions" says of SendMessage that
  "Claude Code tells B's Claude that the message came from another
  session, not from you"
---

# Injected wake text arrives wearing the owner's authority

Text delivered into a session by `claude --resume <id> -p "..."` or
`tmux send-keys` lands as a user-role turn: the argument to `-p` is
the prompt, and typed keys are typed keys, so the transcript shows the
owner saying it. A transport that lets an agent speak as the owner is
an authority hazard independent of whatever content it carries.

The built-in SendMessage transport is the contrast: it attributes the
message to the sending session and forbids it to approve anything.
The hazard is specific to the resume and keystroke routes, which are
the ones a wake uses.
