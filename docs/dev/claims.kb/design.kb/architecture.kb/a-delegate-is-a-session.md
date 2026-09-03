---
label: WORKER_SESSION
standing: user
authority: 'owner ruling 2026-08-29: a worker is "an ordinary
  claude-code session, just with instructions to leave its result in a
  postbox".'
---

# A worker is an ordinary session with postbox instructions

A worker is an ordinary claude-code session, given instructions to
leave its result in a postbox. There is no worker runtime and nothing
to install: what makes a session a worker is the prompt it started
with.

Two things follow. Declining AGENTS_INTERFACE cost the design nothing,
since that interface was never what made a worker a worker. And a
worker is dead in exactly the way any ordinary session is dead, which
is the fact WAKE_DEAD_ONLY leans on.
