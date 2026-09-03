---
label: SEND_GATED
standing: agent
why:
  - ../topology.kb/the-address-is-a-path.md
---

# Sending is gated by path rules

Because the address is a path (PATH_ADDRESS), send-consent rides the
permission system the owner already trusts: within-scope postbox
writes are allowed; cross-scope writes sit under Ask, where the
prompt shows the whole body as a file diff. Unlike push messaging, an
approval is not the last word — the owner can still edit or retract
the message until it is read.
