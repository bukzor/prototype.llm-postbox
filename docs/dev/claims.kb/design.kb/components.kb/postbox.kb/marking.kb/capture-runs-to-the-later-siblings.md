---
label: CAPTURE_TRAILING
standing: bare
why:
  - an-unclosed-element-takes-later-siblings.md
---

# Capture runs to the marker's later siblings

The marker's scope is everything after it in the same container. This
is not a rule the convention imposes: it is what an HTML parser
already does with an element nobody closed (HTML_NESTS).

Describing the parse rather than fighting it means a reader who
resolves the document as HTML gets the intended scope for free, and a
reader who does not can be told the rule in one sentence.
