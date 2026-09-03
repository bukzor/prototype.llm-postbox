---
label: MESSAGE_SHAPE
standing: agent
why:
  - ../../../architecture.kb/the-address-is-a-path.md
---

# A message is a markdown file at a known address

`<postbox>/<recipient>/<timestamp>-<from>-<slug>.md`: a two-line
header (from, re) and the body. Sending is writing that file — no
compose API, nothing to install. The timestamp prefix sorts the queue
in `ls`; the from and slug make the filename legible on its own.
