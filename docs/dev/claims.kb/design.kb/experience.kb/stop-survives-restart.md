---
label: STOP_PERSISTS
standing: user
authority: >-
  user testimony, 2026-09-01: "restarting a session with an agent in
  'stopped by user' status makes it un-resumable (but why?!)"; mechanism
  from the person's own tooling (~/.claude/must-read.kb/when/a-stopped-or-killed-agent-needs-resuming.md
  and Skill(claude-code-surgery))
---

# A stop survives a restart and makes the agent unresumable

Restarting a session while an agent is in stopped-by-user status leaves
that agent unresumable.

The mechanism, from the person's own tooling: the harness persists the
stop as a flag in the agent's metadata and reads it on restart as a
permanent verdict. An interrupt meant as "pause and redirect" is
recorded as "terminated by owner", and nothing on disk
distinguishes the two intents. The person's unstop tool exists to clear
the flag by hand.
