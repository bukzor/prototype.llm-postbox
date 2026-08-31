---
label: NO_CLOSER
standing: user
authority: 'owner ruling 2026-08-29: "the markdown parser already parses
  it as self-closing, so in some sense the self-closing version is more
  honest. As such, remembering the closing tag is cognitive overhead
  that adds no value."'
why:
  - scope-error-is-asymmetric.md
  - a-closing-tag-carries-no-parser-meaning.md
---

# There is no closing form

Nothing closes a marker. A closing tag would buy no parser-side
behavior (NO_PARSER_MEANING) and no correctness worth having, since
over-capture is the cheap direction (FAIL_SAFE). Requiring one would
add something to remember in exchange for nothing.

The paired `<callout>…</callout>` form was declined on that ground: it
prices scope error symmetrically, when the drop makes it asymmetric.
