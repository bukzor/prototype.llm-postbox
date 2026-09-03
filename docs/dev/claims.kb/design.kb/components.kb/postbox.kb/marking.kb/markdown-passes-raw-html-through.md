---
label: MD_PASSTHROUGH
standing: bare
verify: |-
  uv run --with markdown-it-py python -c \
    "from markdown_it import MarkdownIt; print(MarkdownIt('commonmark')
     .render('<callout tag=\"x\"/>\n\nafter\n'))"
  # 2026-08-31: emits the tag verbatim, then a sibling <p> — nothing paired
---

# Markdown passes raw HTML through opaquely

A markdown renderer copies an unrecognized HTML tag into its output
untouched, and pairs nothing: it neither validates the element nor
matches an opening tag against a closing one. Whatever structure the
tag implies is settled later, by whatever parses the resulting HTML.
