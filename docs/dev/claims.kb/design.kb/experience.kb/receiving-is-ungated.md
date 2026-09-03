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

In the built-in push transports, what one session sends reaches the
recipient without the recipient's Claude choosing the moment:

- **Subagents and teammates within a session**: delivery is automatic.
  "delivered automatically to recipients. The lead doesn't need to
  poll for updates." No setting is consulted on the receiving side; in
  auto mode a classifier reviews each arrival before delivery, which is
  a safety filter, not consent.
- **Peer sessions**, since v2.1.224: the owner can set
  `crossSessionInbound` to `accept`, `hold`, or `refuse`, and the
  default holds what arrives for the owner's approval when the two
  sessions' permission classes differ. Held text shows as a notice
  and reaches Claude only when the owner approves.
- **Accepted text** is taken in "between tool calls during an active
  turn", or starts a new turn if the session is idle, and "counts toward
  usage like a prompt you type."

So the sender's action alone spends the recipient's context and
attention wherever the text is accepted, and where it is held the
cost moves to the owner as a dialog. In neither case does the
recipient's Claude pick a task boundary.

Superseded text, 2026-08-28: "no setting consulted on the receiving
side ... there is a rule slot for the SendMessage tool call, none for
delivery." True then; the peer-session control landed later.
