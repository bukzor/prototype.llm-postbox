---
label: TAG_FORM
standing: user
authority: 'owner proposal 2026-08-29, accepted: "<callout tag=@claude/>
  marks all subsequent content as \"callout=@claude\"? Which in turn is
  known to agents to be \"from Claude\"."'
why:
  - no-inline-callout-form-exists.md
  - markdown-passes-raw-html-through.md
---

# The marker is a self-closing callout tag

The marker is `<callout tag="@claude"/>`, written inline in the
message body at the point where the drop begins.

It borrows HTML syntax because markdown offers no inline callout of
its own (NO_INLINE) and passes the tag through untouched
(MD_PASSTHROUGH). The same text therefore degrades to a visible
literal in any renderer that does not know the convention, which is
the failure mode a marking scheme wants: unrecognized, not
misinterpreted.
