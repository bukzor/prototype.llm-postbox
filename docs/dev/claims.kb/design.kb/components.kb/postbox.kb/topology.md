---
label: TOPOLOGY
standing: agent
ontology:
  - address
  - mount
  - graft
  - roster
why:
  - ../../architecture.kb/single-reader-inboxes.md
  - ../../architecture.kb/the-address-is-a-path.md
---

# Where mail lives is a path question

How a postbox is addressed and where its root sits are one subject:
the convention's shape on disk. The commitments here keep that shape
trivial, a grafted XDG root and a legible filename, so that every
transport a filesystem can wear stays in play. The two shape
constraints this rests on, one reader per inbox (SINGLE_READER) and
every address a path (PATH_ADDRESS), sit on the architecture rung.

The root question is settled: RUNTIME_ROOT won, and the five declined
roots stay in `topology.kb/` with their verdicts. MESSAGE_SHAPE is the
other commitment here, the filename.
