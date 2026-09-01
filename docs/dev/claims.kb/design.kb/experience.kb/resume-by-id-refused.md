---
label: NO_RESUME
standing: user
authority: 'user testimony, 2026-09-01: "claude --resume $UUID is flatly refused, redirects to `please run claude agent`"'
---

# Resume by id is refused for an agent

`claude --resume` with an agent's id is flatly refused and redirects the
person to the agent command. The one way they resume a session does not
work on a sub-agent.
