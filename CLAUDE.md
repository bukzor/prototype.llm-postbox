--- # workaround: anthropics/claude-code#13003
git-caution: personal
requires:
  - Skill(llm-design-kb)
triggers:
  - when: creating or maintaining a .kb/ collection
    read: skill://llm-kb
---

# agent-harness

A mechanism by which one agent creates, constrains, observes, converses
with, and judges other agents. Its conversation channel, the postbox,
is the first component designed in full: messages are files, delivery
is a read at a task boundary, and the built-in agent tool and push
messaging are owner-vetoed.

Status: mission, goals, and requirements settled 2026-09-01; postbox
ruled 2026-08-28..29 and folded in 2026-09-03; architecture's own
question open; nothing implemented.

Re-entry for a cold agent: `docs/dev/claims.kb/design.md`, the claim
ledger. The struck claims are load-bearing, not debris. The policies
binding this work, including when an existing mechanism may be read,
are `docs/dev/claims.kb/technical-policy.md`.

## Current Work

Check `.claude/todo.md` for active efforts. Load `Skill("llm-subtask")`
for maintenance.
