---
label: READ_MOVE
standing: agent
why:
  - mutable-until-read.md
---

# Consumption is a move into `read/`

The read that transfers ownership is recorded on disk: consumed mail
moves to the inbox's `read/` subdirectory — a move, never a delete —
so the record MUTABLE_UNTIL_READ promises survives as plain files.
SINGLE_READER keeps the move advisory; nothing depends on rename
atomicity.
