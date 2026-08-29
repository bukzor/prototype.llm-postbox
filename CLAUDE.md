--- # workaround: anthropics/claude-code#13003
git-caution: personal
triggers:
  - when: creating or maintaining a .kb/ collection
    read: skill://llm-kb
---

# prototype.llm-postbox

House convention for inter-session agent collaboration: messages are
files; delivery is a Read at a task boundary. Replaces
SendMessage/ListAgents (owner-vetoed) for cross-session traffic.

Status: fully ruled (2026-08-28..29); nothing implemented.

Re-entry for a cold agent: `docs/dev/claims.kb/design.md` — the claim
ledger (`skill://llm-claims-kb`): the commitments with their standing,
the owner's vetoes as struck claims. The struck claims are
load-bearing, not debris.

## Current Work

Check `.claude/todo.md` for active efforts. Load `Skill("llm-subtask")`
for maintenance.
