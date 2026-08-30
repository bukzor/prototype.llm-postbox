---
label: WORKER_SESSION
standing: user
authority: 'owner ruling 2026-08-29: a worker is "an ordinary
  claude-code session, just with instructions to leave its result in a
  postbox"; on what runs it, "Human or agent could."'
---

# A worker is an ordinary session with postbox instructions

A worker is an ordinary claude-code session, given instructions to
leave its result in a postbox. There is no worker runtime and nothing
to install: what makes a session a worker is the prompt it started
with — which is why declining AGENTS_INTERFACE cost the design
nothing.

Either a human or an agent may start one, and either may revive it: a
human may start what an agent later resumes, or the reverse. "Driver"
and "orchestrator" therefore name a position held at a moment, not a
kind of session, and a worker is dead in exactly the way any ordinary
session is dead.
