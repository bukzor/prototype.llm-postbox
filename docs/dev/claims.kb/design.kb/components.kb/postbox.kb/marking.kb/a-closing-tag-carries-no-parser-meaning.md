---
label: NO_PARSER_MEANING
standing: bare
why:
  - markdown-passes-raw-html-through.md
---

# A closing tag carries no parser-side meaning here

Since markdown pairs nothing (MD_PASSTHROUGH), writing `</callout>`
changes no markdown output: it is a literal string the renderer copies
like any other. Whatever a closing tag might be thought to accomplish,
it does not accomplish it at the layer this convention is written in.
