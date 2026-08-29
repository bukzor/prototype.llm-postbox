# claims.kb — the project's claim ledgers

One ledger per subject: `<subject>.md` — the defining claim and
roll-up — beside `<subject>.kb/`. `skill://llm-claims-kb` is the form.
The collection exists so the roll-ups are members too: sibling
ledgers all validate under `../claims.jsonschema.yaml`, and
`jsonschema/claim.jsonschema.yaml` here is the one schema they share.

## What belongs here

A subject whose commitments need standing. Add a ledger when a
subject starts making contestable commitments of its own — an
implementation ledger once there is code.

## What does NOT belong here

- Prose, procedures, tasks — a ledger holds claims only.
- A claim of an existing subject: file it in that ledger, under the
  outermost theory that coins its words.
