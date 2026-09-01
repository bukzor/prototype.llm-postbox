# agent-harness

Designing a mechanism by which one agent creates, constrains, observes,
converses with, and judges other agents.

## Read first

- `problem-statement.md` -- what the mechanism is for, what makes it good, and
  the failure classes it exists to prevent.
- `acceptance-criteria.md` -- how anyone would know it worked.

Both are **agent-authored drafts, unratified**. They were written to give a
fresh sitting something to push against, not to constrain it. The framing is
the part most worth attacking: if the exchange-rate argument in the problem
statement is wrong, everything downstream of it is wrong too.

## Mode

This is a design sitting. The output of the next pass is a settled problem
statement and a chosen shape -- not code. Resist building; the cost of building
the wrong shape here is high, because whatever gets built becomes the way work
is delegated afterward.

Design against the failure classes, not against a feature list.

## Standing constraint

Do not frame this work as an increment on anything that already exists. Derive
the shape from the problem. Existing mechanisms may be examined later as
evidence about what is achievable on this substrate, and should not be examined
before the problem statement is settled -- an incumbent read early becomes the
design by default.
