---
label: HTML_NESTS
standing: bare
verify: |-
  uv run --with html5lib python -c \
    "import html5lib; d = html5lib.parse('<div><callout><p>x</p></div>',
     namespaceHTMLElements=False);
     print([(e.tag, [c.tag for c in e]) for e in d.iter()
            if e.tag in ('div', 'callout')])"
  # 2026-08-31: <p> is a child of the unclosed <callout>; closing the
  # tag instead makes the two siblings
---

# An unclosed unknown element takes its later siblings as descendants

HTML parsing has no notion of a self-closing unknown element: the `/`
in `<callout tag="@claude"/>` is discarded, the element stays open,
and everything following it in the same container is parsed as its
descendant. Writing an explicit closing tag is what would make the
following content a sibling instead.
