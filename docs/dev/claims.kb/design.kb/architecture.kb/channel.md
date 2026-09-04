---
label: CHANNEL_PICK
standing: open
authority: >-
  owner, 2026-09-03: "'Can SendMessage be our postbox?' I'd set it
  down as OPEN. It's genuinely worth discussion and thought. I'm
  leaning toward no, mainly because i vcs/audit/control aspects of our
  filesystems approach, but it's not a forgone conclusion"; and, of
  the grounds against SendMessage, "it's unclear whether/how we can
  hit those goals in the fs-postbox approach, either"
stale-when: REWIND or UNINTERRUPTED runs against both candidates, or the substrate changes when a pushed message is read or whether it can be rewound
why:
  - channel.kb/the-postbox.md
  - channel.kb/sendmessage.md
  - ../goals.kb/mutable-until-read.md
  - ../goals.kb/the-record-outlives-the-job.md
  - ../requirements.kb/history-rewinds.md
  - ../requirements.kb/a-message-waits-for-its-reader.md
  - ../requirements.kb/messages-are-attributed.md
  - ../experience.kb/push-messaging-bit-three-ways.md
  - ../experience.kb/receiving-is-ungated.md
---

# What carries the conversation channel?

Open. `channel.kb/` holds two live answers: files in the recipient's
inbox (CHANNEL_IS_POSTBOX), which the components theory POSTBOX
designs in full, and the built-in SendMessage transport (SENDMESSAGE).
The owner leans to the files, for the version control, audit, and
control a filesystem gives, and calls that a lean, not a ruling.

History. SendMessage was declined as the transport on 2026-08-28 on
three lived failures, inane sends, recipient distraction, and
unrewindable receipt (PUSH_GROUNDS), three of what the owner counts as
about twelve bugs and misfeatures. The note attached then, "Even if
they do, i don't trust they won't add other problems (for me)", is a
prior on evaluating the substrate's fixes, not a refusal to revisit:
two small likelihoods, that the flock gets an attempt and that the
attempt passes the owner's evaluation, multiply to a very small one.
The question reopened in this narrower form on 2026-09-03, after the
substrate grew an owner-side hold and refuse for peer-session messages
(RECEIVE_UNGATED), which weakens the first ground and leaves the other
two untouched.

What discriminates today. MUTABLE_UNTIL_READ: a file can be edited or
withdrawn until its reader takes it, and a sent message cannot.
RECORD: files are a record the owner can version and audit, where
SendMessage leaves only two transcripts. ATTRIBUTED cuts the other
way: SendMessage meets it built in, and the postbox meets it by its
marking theory.

What does not discriminate yet. REWIND and UNINTERRUPTED are the
second and third grounds as probes, and neither candidate has run
them; the owner holds that the filesystem postbox is not yet shown to
meet them either.

What settles it: both probes run against both candidates, then the
owner rules. The lean stands until then.
