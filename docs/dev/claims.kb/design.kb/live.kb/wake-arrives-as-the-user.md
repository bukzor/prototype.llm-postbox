---
label: WAKE_WEARS_AUTHORITY
standing: bare
---

# Injected wake text arrives wearing the owner's authority

Text delivered into a session by `claude --resume <id> -p "..."` or
`tmux send-keys` lands as a user-role turn: the transcript shows the
owner saying it. Checkable in any transcript so produced. A transport
that lets an agent speak as the owner is an authority hazard
independent of whatever content it carries.
