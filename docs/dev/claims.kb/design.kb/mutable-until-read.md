---
label: MUTABLE_UNTIL_READ
standing: user
authority: 'owner ruling 2026-08-28: "the ability to see, review, even
  **edit** sent post. That''s a feature i want to preserve no matter our
  final solution."'
---

# A message belongs to the sender until it is read

A message belongs to the sender until it is read; after reading it
belongs to the record. Pre-read, the file is visible, editable, and
deletable by sender or owner; post-read it is immutable audit trail;
the transition happens exactly once, at read time.

This is the design's non-negotiable: every mechanism — hook, CLI,
mount, monitor — is checked against it before adoption
(`../../../../design.kb/convention.md`).
