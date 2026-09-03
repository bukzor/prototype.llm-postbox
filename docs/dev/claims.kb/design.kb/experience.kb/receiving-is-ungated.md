---
label: RECEIVE_UNGATED
standing: bare
authority: >-
  Claude Code docs, fetched 2026-09-03: "Message your other Claude Code
  sessions" (crossSessionInbound, "Message delivery", "How a session
  treats an incoming message") and "Orchestrate teams" ("Automatic
  message delivery", "Messages between agents")
---

# Receiving is gated by the owner's settings, never by the recipient's Claude

In the built-in push transports, a sent message reaches the recipient
without the recipient's Claude choosing the moment:

- **Subagents and teammates within a session**: delivery is automatic.
  "When teammates send messages, they're delivered automatically to
  recipients. The lead doesn't need to poll for updates." No setting is
  consulted on the receiving side; in auto mode a classifier reviews
  each message before delivery, which is a safety filter, not consent.
- **Peer sessions**, since v2.1.224: the owner can set
  `crossSessionInbound` to `accept`, `hold`, or `refuse`, and the
  default holds a message for the owner's approval when the two
  sessions' permission classes differ. A held message shows as a
  notice and reaches Claude only when the owner approves.
- **An accepted message** is read "between tool calls during an active
  turn", or starts a new turn if the session is idle, and "counts toward
  usage like a prompt you type."

So the sender's action alone spends the recipient's context and
attention wherever the message is accepted, and where it is held the
cost moves to the owner as a dialog. In neither case does the
recipient's Claude pick a task boundary.

Superseded text, 2026-08-28: "no setting consulted on the receiving
side ... there is a rule slot for the SendMessage tool call, none for
delivery." True then; the peer-session control landed later.
