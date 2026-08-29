---
managed-by: Skill(llm-subtask)
---

Scope: the postbox prototype. The claim ledger
(`docs/dev/claims.kb/design.md`) is the normative surface; this list
is the work queue over it.

- [ ] Core protocol: postbox root resolution
      (`<root>/.local/state/llm-postbox/`, cwd-grafted XDG, plain XDG
      outside repos), message naming (`<timestamp>-<from>-<slug>.md`),
      `read/` move on consume
- [ ] Trigger-bank entries via skill://llm-triggers: hand-off, boundary
      inbox check, live-channels-carry-no-content
- [ ] Global gitignore of `.local/` via `core.excludesFile`
- [ ] Permission scoping: within-project postbox writes allowed,
      cross-scope under Ask
- [ ] Optional mechanisms, each gated on the mutable-until-read
      invariant:
  - [ ] Monitor opt-in interruption (filenames only)
  - [ ] wake-by-resume for dead sessions (max-wakes guard)
  - [ ] user-turn hook: unread-mail pointers, silent when empty
  - [ ] draft stage (`*.draft.md`) for unattended loops
  - [ ] statusline unread count
