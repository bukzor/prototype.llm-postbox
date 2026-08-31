---
label: WRAPPER_ONLY
standing: user
todo: true
authority: 'owner ruling 2026-08-29: the wrapper "is preapproved for
  Bash(). Note that `claude` is not."'
why:
  - ../../trust.kb/the-owner-is-the-only-boundary.md
---

# Only the wrapper is pre-approved; bare `claude` is not

The permission rules allow `claude-sub-agent` to run without a prompt
and leave a bare `claude` invocation gated behind one.

The asymmetry is the point: the marked path is the frictionless one
and the unmarked path is the one that stops for the owner. An agent
reaching for the unmarked path meets the only enforcer that holds
(OWNER_IS_THE_BOUNDARY).
