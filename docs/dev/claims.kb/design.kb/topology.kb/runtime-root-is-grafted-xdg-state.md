---
label: RUNTIME_ROOT
standing: user
authority: 'owner rulings 2026-08-29: cwd-grafted XDG layout; "ah no
  please use the correct thing. state is good."'
---

# The postbox root is `<root>/.local/state/llm-postbox/`

The postbox lives at `<root>/.local/state/llm-postbox/`, where
`<root>` is the nearest enclosing `.git/` walking up from `$CWD`;
outside any repo the graft degrades to genuine XDG,
`~/.local/state/llm-postbox/`. `state`, not `share`: mail is transient
runtime data. The declined alternatives and their grounds — bare
`postbox/`, `.claude/postbox/`, `postbox.kb/`, `share`, `spool` — are
recorded in `../../../../../design.kb/convention.md` (runtime location
why-nots).
