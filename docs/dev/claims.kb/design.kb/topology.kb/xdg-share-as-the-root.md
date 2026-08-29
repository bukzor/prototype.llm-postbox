---
label: XDG_SHARE
standing: user
verdict: declined
authority: 'owner ruling 2026-08-29: "ah no please use the correct
  thing. state is good."'
why:
  - runtime-root-is-grafted-xdg-state.md
---

# `share` instead of `state` under XDG

XDG files durable user data under `share` and transient runtime data
under `state`. Mail is transient: written, read once, and kept only
as record.
