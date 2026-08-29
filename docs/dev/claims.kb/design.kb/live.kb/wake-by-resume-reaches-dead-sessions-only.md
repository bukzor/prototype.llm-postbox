---
label: WAKE_DEAD_ONLY
standing: agent
why:
  - live-channels-carry-the-wake-phrase-only.md
---

# Wake-by-resume reaches dead sessions only

An orchestrator wakes a dead worker with `claude --resume <id> -p
"check your postbox"` — the wake phrase, nothing else (WAKE_PHRASE) —
and surfaces `claude --resume <id>` for the owner to attach
interactively. Dead sessions only: two processes on one transcript
corrupts state. This closes the overnight orchestrator/worker loop;
its safety boundary is the workers' permission allowlists (nobody is
at the prompt), plus a max-wakes guard against ping-pong.
