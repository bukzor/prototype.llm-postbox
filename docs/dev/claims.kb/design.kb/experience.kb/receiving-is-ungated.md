---
label: RECEIVE_UNGATED
standing: bare
---

# Permission settings gate sending only

In the built-in push transports (SendMessage/ListAgents), permission
configuration gates the outbound call; an inbound send lands in the
recipient's context with no setting consulted on the receiving side.
Checkable against the permission surface: there is a rule slot for the
SendMessage tool call, none for delivery. The recipient's costs —
context occupancy, interruption — are therefore spent by the sender's
action alone.
