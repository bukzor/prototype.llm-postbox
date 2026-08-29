# design.claims.kb — maintenance guide

The postbox design's commitments, kept as a claim ledger
(`Skill(llm-claims-kb)`). `../design.claims.md` is the entry point and
the defining claim.

## What belongs here

A commitment the design makes — anything whose standing could be
contested and whose reversal would change `../../../design.kb/`.

## What does NOT belong here

- The design prose and its declined alternatives → `../../../design.kb/`
  (`transport.kb/` holds the kill records; cite them, never copy).
- Implementation tasks → `../../../.claude/todo.md`.
- Anything whose honest standing no one could contest: that is
  documentation, and claim frontmatter on it records a judge that
  ruled nothing.

New file: kebab-case, named in prose for the commitment; `label:` +
`standing:` frontmatter under `jsonschema/claim.jsonschema.yaml`.
