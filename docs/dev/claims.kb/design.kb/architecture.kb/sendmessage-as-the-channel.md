---
label: SENDMESSAGE
standing: open
authority: >-
  owner, 2026-08-28, declining it as the transport on PUSH_GROUNDS with
  the note "I doubt claude-code team will 'fix' all these aspects
  anytime soon. Even if they do, i don't trust they won't add other
  problems (for me)"; owner, 2026-09-03, on what that note meant: "even
  if they *attempt* to fix it (which is in fact a flock of ~12 bugs and
  misfeatures), I have very low prior liklihood that I'll evaluate their
  fixes and find them suitable for use. Between the two small
  liklihoods, it seems very unlikely"; and reopening the narrow
  question the same day: "'Can SendMessage be our postbox?' I'd set it
  down as OPEN. It's genuinely worth discussion and thought. I'm
  leaning toward no, mainly because i vcs/audit/control aspects of our
  filesystems approach, but it's not a forgone conclusion." And on the
  grounds: "it's unclear whether/how we can hit those goals in the
  fs-postbox approach, either."
why:
  - ../experience.kb/receiving-is-ungated.md
  - ../experience.kb/push-messaging-bit-three-ways.md
  - ../requirements.kb/history-rewinds.md
  - ../requirements.kb/a-message-waits-for-its-reader.md
  - ../requirements.kb/messages-are-attributed.md
---

# Can SendMessage be the channel?

Open. The built-in SendMessage transport is the second contending
answer to what carries the conversation channel; the first is
CHANNEL_IS_POSTBOX. It was declined as the transport on 2026-08-28 on
the owner's three grounds, inane sends, recipient distraction, and
unrewindable receipt (PUSH_GROUNDS), and reopened on 2026-09-03 as
this narrower question, after the substrate grew an owner-side hold
and refuse for peer-session messages (RECEIVE_UNGATED).

What settles it is the same probes run against both candidates. The
owner's grounds are not yet shown to be met by the filesystem postbox
either, so they do not discriminate until run: REWIND and
UNINTERRUPTED are what the second and third grounds became, and
ATTRIBUTED is one SendMessage meets today and the postbox meets by its
marking theory. The owner leans toward the postbox for the version
control, audit, and control a filesystem gives. A lean is not a
ruling.

The 2026-08-28 note about not trusting fixes is a prior on evaluating
the substrate's fixes, not a refusal to revisit: two small
likelihoods, that the flock of about twelve bugs and misfeatures gets
an attempt and that the attempt passes the owner's evaluation,
multiply to a very small one.
