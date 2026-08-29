# claims.kb — the project's claim ledgers

One ledger per subject: `<subject>.md` — the defining claim and
roll-up — beside `<subject>.kb/`. `Skill(llm-claims-kb)` is the form.
The collection exists so the roll-ups are members too: sibling
ledgers all validate under `../claims.jsonschema.yaml`, and
`jsonschema/claim.jsonschema.yaml` here is the one schema they share.

## What belongs here

A subject whose commitments need standing. The design's ledger is
the first; an implementation ledger joins it when the code starts
making commitments of its own.

## What does NOT belong here

- Prose, procedures, tasks — a ledger holds claims only.
- A claim of an existing subject: file it in that ledger, under the
  outermost theory that coins its words.
