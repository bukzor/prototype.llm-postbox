# Devlog: 2026-09-03 — Postbox folded into the agent-harness design

## Focus

Merge two design ledgers that turned out to be one design: the
agent-harness (mission, goals, requirements for a delegation
mechanism, written 2026-09-01 in its own repo) and the postbox (the
inter-session mail convention, ruled 2026-08-28..29 here). The owner's
call: "they seem related enough that two kb feels wrong."

## Decisions

### The postbox is a component, and its top layer is promoted

A side-by-side of the 58 postbox claims against the harness found one
obviated (the root frame, "the design's single home"), about eight
convergent, and the rest one rung below the harness: the design of
its conversation channel. So the postbox moved to
`design.kb/components.kb/postbox.md` + `postbox.kb/` with `topology`,
`live`, and `marking` nested as they were, and 21 claims plus the
`trust` and `delivery` theories moved up to the rung whose question
they answer.

**Rationale:** pushing everything down would have filed goal-level
rulings as implementation detail — `MUTABLE_UNTIL_READ` binds "no
matter our final solution" and cannot sit below the solution.
**Alternatives considered:** dissolve the postbox entirely by rung
(purest, but 45 of 58 land in components anyway and `MARKING` only
reads as a unit); a sibling theory beside the rungs (rejected: a
subject spanning rungs is what confinement exists to catch); two
ledgers with cross-imports (the owner's veto).

### Which repo survives

This one. It had the remote, the devlog, and fifteen commits; the
harness had two commits and no remote. The harness came in by
`git merge --allow-unrelated-histories -X theirs`, so both histories
are intact and `CLAUDE.md` took the harness version. The rename to a
name for the mechanism is the owner's, pending.

### Session parity absorbed the postbox's ruling

The harness's agent-signed "a delegate is a session" and the postbox's
user-signed "a worker is an ordinary session" said one thing. The
postbox file kept the history, took the harness label `IS_SESSION`,
the harness's declined alternative, and both authority quotes; it is
user-signed now and still `todo: true`.

### Three tensions resolved by reading, not by choosing

- **Enforcement.** The harness's `CONFINE`, `EVIDENCE`, and
  `GRADER_SAFE` assumed something outside the delegate enforces
  reach; the postbox's `SCRIPTS_IMPLY_TRUST` (owner-signed) says an
  agent with a shell is inside any such thing. Both hold under
  `HONEST`: the harness claims now say they read under `TRUST`, as
  guards against honest error, and `GRADER_SAFE` no longer says
  "cannot". Whether the Bash sandbox is a real boundary is `TRUST`'s
  own stale-when and a todo.
- **Interrupt.** `LIFECYCLE` gave every delegator interrupt;
  `OPT_IN_INTERRUPT` gives it to the receiver. Reconciled: the person
  interrupts a session directly because they own the terminal; an
  orchestrator's soft interrupt is a pointer the delegate reads when
  it chooses, or a kill.
- **Attribution.** `TWO_DELEGATORS` gave the person and the
  orchestrator separate channels but never said how a delegate tells
  them apart. `WAKE_WEARS_AUTHORITY` says the substrate makes that
  necessary; `ATTRIBUTED` is the new requirement, and `MARKING` is
  what satisfies it.

## Conventions Established

- **Moves commit before edits.** Three rename-only commits (the
  tower move, the duplicate retirement, the label renames) preceded
  two edit commits (arrow and schema repair, then content). `git log
  --follow` works on every file that crossed a rung.
- **The audit tools drive the repair, not memory.** Dangling arrows
  came from the flatten's stderr, word collisions from the ownership
  scan, isolated clusters from the graph's component count. Four of
  the isolated clusters predated the fold: the postbox's own
  `RUNTIME_ROOT`, `BROUGHT_WORD`, `INTEGRATION_HOME`, and the whole
  `marking` theory were never joined to anything, and now are.
- **A theory releases a word downward, never claims it upward.**
  `inbox` went from architecture to the delivery theory under goals
  because goals-level claims needed it; `message` and `read` went to
  the goals root for the same reason; the postbox culled every word a
  rung above now owns.

## Open Questions

- The repo's new name, and retiring `~/claude/agent-harness` after it.
- `MOUNT_REACH` stays open beside the user-signed `LOCAL`; the goal-
  versus-windfall question its body poses is unchanged by the fold.
- The 2026-08-31 entry asked whether `TRUST` and `MARKING` belong
  inside the postbox at all. Answered halfway: `TRUST` is goals-level
  now; `MARKING` stays a postbox theory with a harness requirement
  above it, and `FAMILY`'s point that the callout family is a
  house-wide documentation convention is still unaddressed.

## Judgment calls open to veto

The review queue is `grep -rl '^standing: agent' docs/dev/claims.kb/`.
Calls that queue does not announce on its own:

- **Placement of the promoted twenty-one**, chiefly `TRUST` under
  goals rather than mission, `MUTABLE_UNTIL_READ` at the goals root
  rather than inside `delivery`, and `RECEIVE_UNGATED` and
  `WAKE_WEARS_AUTHORITY` in `experience` under a new stipulated
  phrase, "substrate fact".
- **Vocabulary moves**: goals widened by `message` and `read`;
  `delivery` took `inbox`; the postbox's `record` became `read
  record`; `worker`, `driver`, `orchestrator`, `sender`, and
  `recipient` are no longer stipulated anywhere.
- **Four labels renamed** under the no-prefix rule: `WORKER_SESSION`
  → `IS_SESSION`, `WORKER_START` → `STARTER`, `PULL` → `OFFERED`,
  `DESIGN_FIRST` → `BUILD_LATER`.
- **`delivery.md` dropped its arrow to `topology.md`** (an upward
  citation from goals to components) in favour of `OFFERED` and
  `CONVERSE`.
- **`RETENTION` and `MOUNT_REACH`** were found staged but never
  committed by an earlier session and were committed as-is before the
  move, so the fold moved tracked files only.
- **`STOP_PERSISTS` carries a mechanism** taken from the owner's
  must-read bank and surgery skill, not from testimony; it is signed
  user on the testimony and cites the tooling for the mechanism.

## References

- `../claims.kb/design.md` — the ledger roll-up and re-entry point
- `../claims.kb/design.kb/components.kb/postbox.md` — the postbox as
  a component, with the narrative address of its own design
- `2026-08-31-000-Marking-and-trust-theories-filed.md` — the pass
  whose open questions this one half-answers
- The harness's own two commits, reachable as `harness/main`
