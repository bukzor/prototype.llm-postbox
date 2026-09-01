# Devlog: 2026-08-31 — Marking and trust theories filed

## Focus

Persist the 2026-08-29 reasoning about marking agent-authored text,
and the reframe that came with it, into `docs/dev/claims.kb/design.kb/`
as two new theories.

## Decisions

### The reframe came before the mechanism

The session started as a notation question — the owner wanted an
inline callout form, since the blockquote form costs a `> ` on every
line — and turned when the owner filed the whole area under
"foolproofing" rather than "security": *"If claude was a security
concern, i shouldn't let it write scripts at all."*

That reordered the argument. Two of the agent's proposals were
security-shaped and died on the spot:

- **A paired `<callout>…</callout>` form.** Recommended on the ground
  that unbounded scope was dangerous. The owner's correction: the
  marker is a privilege *drop*, so over-capture is a minor correctness
  issue, not a threat — the agent had priced an asymmetric error
  symmetrically. Now `NO_CLOSER`, with the paired form named in its
  body as the declined alternative.
- **A `deny`-rule requirement** conditioning the design on blocking a
  sender that omits the marker. Void under `FOOLPROOFING`: it answers
  an adversary the design does not model.

The owner's parity argument is what made the mechanism admissible at
all — the plan of record, sending a bare "check your inbox", *also*
arrives in human-user voice and *also* relies on convention. Filed as
`CONVENTION_PARITY`, and it is the claim that disposes of "an agent
could just omit it" whenever that objection returns.

### `<voice>` was declined in favor of one callout family

The agent proposed renaming the element to `<voice>` for precision.
Declined: one mechanism serving `TODO`, `QUESTION`, and `@claude`
alike is the better subtraction, and `callout` is a word agents
already bring, where `voice` would have to be taught. `FAMILY` and
`BROUGHT_WORD`.

`BROUGHT_WORD` also settled the ontology: `MARKING` does *not* coin
`callout`, because a theory lists only words it fixes a meaning for
that a reader could not have brought. It coins `privilege drop` and
`capture` only.

### The five substrate facts were certified, not asserted

`MD_PASSTHROUGH` and `HTML_NESTS` were checked rather than believed:
markdown emits `<callout tag="x"/>` verbatim with the next paragraph
as a sibling, and html5 parsing puts that paragraph *inside* an
unclosed `<callout>` but *beside* a closed one. Both carry the command
in `verify:` and stand `bare`. Prompted by the standing-honesty audit
— a bare claim resting on neither `verify:` nor `why:` is a hidden
judge.

The check also corrected a claim the agent had drafted: a heading does
**not** end capture in the HTML parse. `SCOPE_RESET` is therefore a
convention laid over the parse and stands `agent`, with the
disagreement stated in its body rather than papered over.

## Conventions Established

- **Substrate facts live with their only consumer.** The five
  Markdown/HTML facts coin nothing, so the placement rule ("outermost
  theory coining every word the claim needs") does not force them
  upward. They sit in `marking.kb/` because `MARKING` is the only
  theory that reads them; a second consumer is the signal to promote
  them to a shared prior, per the confinement audit.
- **`git mv` before writing.** `FOOLPROOFING` and
  `OWNER_IS_THE_BOUNDARY` predated `TRUST` and moved into it, so the
  moves went in first and the `why:` sweep followed.

## Open Questions

- Whether `TRUST` and `MARKING` belong *inside* the postbox ledger at
  all. In chat they rendered as siblings of `POSTBOX`; on disk they
  are its children, which inverts the support relation (`POSTBOX <-
  TRUST`). Filed as children anyway, both `standing: agent`, on the
  grounds that a prototype with nothing implemented should not mint
  three ledgers. A second subject leaning on `TRUST` is the signal to
  promote it to a sibling ledger under `claims.kb/`.
- `MARKING` is arguably not postbox-specific at all: `FAMILY` says the
  same mechanism carries `TODO` and `QUESTION`, which is a house-wide
  documentation convention, and `INTEGRATION_HOME` already routes that
  class of artifact to `~/.claude`.

## Judgment calls open to veto

The ledger's own review queue is `grep -rl '^standing: agent'` (28
files). These are the calls that queue does *not* announce on its own,
because the file records the decision without recording that it was a
choice:

- **`POSTBOX` widened by `driver` and `orchestrator`** to coin what
  `ROLES_POSITIONAL` fixes. Widening an ontology is a revision to the
  defining claim and wants a signature.
- **Two stipulations uniquified.** `DELIVERY`'s `boundary` →
  `task boundary` was forced: the confinement audit names the
  head-noun truncation, and `TRUST` needs the bare word in the
  containing sense. `TOPOLOGY`'s `reader` → `single reader` was *not*
  forced — it freed the ordinary word for `MARKING`'s use, and the
  alternative was rewording three `marking.kb` claims instead.
- **Two theory-level imports added** — `live.md` → `trust.md`, and
  `delivery.md` → `topology.md`. Both theories were already saying the
  other's words with only a claim-level `why:`, which does not license.
  An import asserts support at theory grain, which is stronger than
  what the claim-level arrow said; if that overstates it, the repair is
  rewording one sentence in each.
- **Two labels renamed** under the no-prefix rule: `WRAPPER` →
  `WRAPPER_MARKS` (it prefixed `WRAPPER_ONLY`), and the pre-existing
  `POSTBOX_KB` → `MAIL_AS_KB`.
- **`READING_RULE` carries `todo: true`**, which the chat render did
  not have. The rule applied: mark the claims naming an artifact to
  build, leaving notation claims like `TAG_FORM` untensed.

## References

- `../claims.kb/design.md` — the ledger roll-up and re-entry point
- Session `c80a6431-2ca1-41a9-82ee-b01b7f91a4dc`
- `~/.claude/skills/llm-claims-kb/skill.kb/self-audit.kb/` —
  confinement and standing-honesty audits, both of which fired here
