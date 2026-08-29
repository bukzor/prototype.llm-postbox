--- # workaround: anthropics/claude-code#13003
git-caution: personal
---

# prototype.llm-postbox

House convention for inter-session agent collaboration: messages are
files; delivery is a Read at a task boundary. Replaces
SendMessage/ListAgents (owner-vetoed) for cross-session traffic.

Status: design converged and fully ruled (2026-08-28..29); nothing
implemented.

Re-entry for a cold agent: `design.kb/CLAUDE.md`.

Collections: `design.kb/` is the design prose; its claim ledger is
`docs/dev/claims.kb/design.md` + `.kb/` — the commitments with their
standing, the place to argue with the design (`Skill(llm-claims-kb)`).

## Current Work

Check `.claude/todo.md` for active efforts. Load `Skill("llm-subtask")`
for maintenance.
