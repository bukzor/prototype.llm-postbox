---
label: SCOPE_RESET
standing: agent
why:
  - capture-runs-to-the-later-siblings.md
---

# A heading ends capture

By convention a heading ends capture: text under the next heading is
unmarked again. This is the one escape a long document needs, and a
heading is already where a reader resets context, so it costs nothing
to remember.

The convention and the parse disagree at exactly this point — HTML
keeps the heading and everything after it inside the open element
(HTML_NESTS). The alternative that would remove the disagreement is a
closing tag, which NO_CLOSER declines for reasons that outweigh it.
