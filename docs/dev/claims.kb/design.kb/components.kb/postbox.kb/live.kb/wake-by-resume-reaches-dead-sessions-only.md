---
label: WAKE_DEAD_ONLY
standing: agent
why:
  - live-channels-carry-the-wake-phrase-only.md
  - ../../../architecture.kb/delegate.kb/a-session.md
  - ../../../goals.kb/trust.kb/the-design-is-foolproofing-not-security.md
  - ../../../experience.kb/concurrent-resumes-fork-the-transcript.md
---

# Wake-by-resume reaches dead sessions only

An orchestrator wakes a dead worker with `claude --resume <id> -p
"check your postbox"` — the wake phrase, nothing else (WAKE_PHRASE) —
and surfaces `claude --resume <id>` for the owner to attach
interactively. Dead sessions only: a resume racing a live process forks the
transcript and one branch is silently lost (RESUMES_FORK). This closes the overnight orchestrator/worker loop;
what bounds an unattended one is the workers' permission allowlists
(nobody is at the prompt) plus a max-wakes guard against ping-pong —
guards against mistakes, not boundaries (FOOLPROOFING).
