---
label: RUNTIME_ROOT
why:
  - ../../../architecture.kb/the-address-is-a-path.md
standing: user
authority: 'owner rulings 2026-08-29: cwd-grafted XDG layout; "ah no
  please use the correct thing. state is good."'
---

# The postbox root is `<root>/.local/state/llm-postbox/`

The postbox lives at `<root>/.local/state/llm-postbox/`, where
`<root>` is the nearest enclosing `.git/` walking up from `$CWD`;
outside any repo the graft degrades to genuine XDG,
`~/.local/state/llm-postbox/`. `.local/` is ignored once, globally
(`core.excludesFile`), never per-repo. The graft is what buys both
properties at once: mail sits with the work it concerns, and the
layout stays the standard one wherever no repo encloses it.
