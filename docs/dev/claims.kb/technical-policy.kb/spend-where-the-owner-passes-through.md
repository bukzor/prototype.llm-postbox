---
label: SPEND_AT_THE_OWNER
standing: agent
force: should
why:
  - ../design.kb/goals.kb/trust.kb/the-owner-is-the-only-boundary.md
---

# Spend where the owner passes through

Put what must not go wrong at a point the owner's attention already
crosses, and keep everything else cheap. This design has two such
points:

- SEND_GATED's Ask prompt, which shows a cross-scope message as a diff
  before it is written;
- the keybinding the owner presses to hand work to a stopped session
  (WAKE_WEARS_AUTHORITY).

Both hold because the agent is not the one enforcing them. Everything
else should be built to a guard's standard — cheap, obvious, and not
relied upon — and effort spent hardening it past that standard is
effort spent where nothing holds.
