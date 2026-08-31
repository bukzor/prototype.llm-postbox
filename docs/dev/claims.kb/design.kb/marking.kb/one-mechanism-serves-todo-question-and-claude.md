---
label: FAMILY
standing: user
authority: 'owner ruling 2026-08-29: "I like that <callout> can be used
  for TODO and QUESTION too."'
why:
  - no-inline-callout-form-exists.md
---

# One callout mechanism serves TODO, QUESTION, and `@claude` alike

`<callout tag="...">` is one mechanism with a type parameter, not a
marker invented for agent attribution. The same tag carries the
doc-driven-development markers — `[!TODO]` for decided-not-built,
`[!QUESTION]` for undecided — which today have only the blockquote
form and the same per-line cost (NO_INLINE).

A separate `<voice>` element for attribution was declined: it would
have split one mechanism in two and asked agents to learn a second
concept for the same job.
