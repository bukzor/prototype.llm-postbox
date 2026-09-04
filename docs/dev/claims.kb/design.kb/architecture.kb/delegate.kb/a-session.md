---
label: IS_SESSION
standing: user
todo: true
authority: >-
  owner ruling 2026-08-29: a worker is "an ordinary claude-code
  session, just with instructions to leave its result in a postbox";
  restated 2026-09-01: "Monitor plus `claude --resume` covers all the
  cases i can think of"; "I refuse to use `claude agent`"
why:
  - ../goals.kb/a-delegate-lacks-nothing-a-session-has.md
  - ../requirements.kb/never-the-agent-tool.md
  - ../mission.kb/delegation-is-avoided-today.md
---

# A delegate is an ordinary session

A delegate is an ordinary claude-code session, started and resumed
through the claude command line and never through the built-in agent
tool, given instructions to leave its result at a known address. There
is no delegate runtime and nothing to install: what makes a session a
delegate is the prompt it started with.

Three things follow. PARITY holds by construction: whatever the person
can do to a session they can do to a delegate, with the same commands.
NO_AGENT_TOOL is satisfied by never creating an agent at all, so
declining AGENTS_INTERFACE cost the design nothing, since that
interface was never what made a delegate a delegate. And a delegate is
dead in exactly the way any ordinary session is dead, which is the
fact WAKE_DEAD_ONLY leans on.

Declined: a bespoke harness re-implementing each session capability,
which would re-pay every capability the session already has and still
miss the next one the person reaches for.
