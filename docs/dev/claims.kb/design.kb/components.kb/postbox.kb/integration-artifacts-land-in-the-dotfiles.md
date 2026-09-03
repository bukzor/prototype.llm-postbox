---
label: INTEGRATION_HOME
standing: user
authority: 'owner ruling 2026-08-29: the postbox is its own sub-project repo.'
---

# The prototype is a repo; integration artifacts land in `~/.claude`

The postbox design and implementation live in this repo. What must
integrate with the owner's Claude Code environment when implemented —
trigger-bank entries, hooks, permission rules — lands in `~/.claude`,
not here: the dotfiles are what a session actually reads.
