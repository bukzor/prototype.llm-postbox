---
label: NO_INLINE
standing: bare
why:
  - a-callout-is-a-blockquote.md
---

# Neither dialect has an inline callout form

A blockquote is a block construct, so there is no way to mark a run of
text inside a paragraph as a callout, and no way to open one without
prefixing every line it covers with `> `.

Marking a long message in the existing form therefore costs an edit to
every line of it. That cost is what sent this design looking for
another form.
