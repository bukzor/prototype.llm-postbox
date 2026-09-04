---
label: SENDMESSAGE
standing: agent
why:
  - ../../experience.kb/receiving-is-ungated.md
  - ../../experience.kb/wake-arrives-as-the-user.md
  - ../../requirements.kb/messages-are-attributed.md
---

# SendMessage as the channel

The conversation channel is the built-in cross-session transport:
sending is a SendMessage call naming the recipient session, and
receiving is delivery into the recipient's context between tool
calls, or as a new turn if it is idle, subject to the owner's inbound
setting of accept, hold, or refuse (RECEIVE_UNGATED). Nothing is
written to disk but the two transcripts.

What the option has today: attribution and a bar on approvals come
built in, so ATTRIBUTED is met without a marking theory; bursts are
refused at the sender and loops throttled at the receiver; a `claude
-p` worker binds an inbox socket, so a headless delegate is reachable
by name.

What it lacks by construction: a sent message cannot be edited or
withdrawn after the call; there is no record outside the two
transcripts; and the moment of reading is the substrate's, not the
recipient's.
