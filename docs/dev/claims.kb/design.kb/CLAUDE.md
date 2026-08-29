# design.kb — maintenance guide

The postbox design, kept as a claim ledger
(`skill://llm-claims-kb`). `../design.md` is the entry point and the
defining claim.

## What belongs here

A commitment the design makes — anything whose standing could be
contested and whose reversal would change the convention. Declined
alternatives belong here too, as struck claims (`verdict:`) holding
the veto and the grounds it died on.

## Where a new file goes

Under the outermost theory that coins every coined word its text
needs: a claim in root vocabulary sits here beside the theory files;
a claim arguing in a theory's vocabulary goes under that theory's
`.kb/`.

A declined candidate files beside the claim that beat it, by that
same rule: one collection holds a decision's answers, chosen and
struck alike, so `ls` is the enumeration. A list of candidates
inside one claim's body is the shape to break up.

## What does NOT belong here

- Implementation tasks → `../../../../.claude/todo.md`.
- Anything whose honest standing no one could contest: that is
  documentation, and claim frontmatter on it records a judge that
  ruled nothing.

New file: kebab-case, named in prose for the commitment; `label:` +
`standing:` frontmatter under the sibling `*.jsonschema.yaml`.
