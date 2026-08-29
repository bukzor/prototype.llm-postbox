---
label: CLAUDE_POSTBOX
standing: agent
verdict: declined
why:
  - runtime-root-is-grafted-xdg-state.md
---

# The postbox under `.claude/`

The agent's own directory, already present in every project — and
committed in many, which leaves transient mail one careless `git add`
from history. Traffic and configuration want opposite fates in
version control.
