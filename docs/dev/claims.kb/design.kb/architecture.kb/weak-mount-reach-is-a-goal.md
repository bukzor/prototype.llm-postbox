---
label: MOUNT_REACH
standing: open
why:
  - single-reader-inboxes.md
  - the-address-is-a-path.md
  - substrate-is-local-for-now.md
---

# Weak-mount reach is a goal

Cross-machine operation via dumb mounts (s3fs, sshfs, syncthing) is a
standing constraint: a future mechanism must stay within what a weak
mount can honor, or be declined.

The ledger leans on this without a ruling: SINGLE_READER declines the
shared claim-queue partly because weak mounts cannot lock, and
PATH_ADDRESS presents cross-machine mounting as a payoff. Candidates:

- **Goal** — sign this claim. Every future mechanism (an inotify
  monitor, any rename-atomicity assumption) is checked against
  weak-mount semantics before adoption.
- **Windfall** — strike it (`verdict: rejected`). SINGLE_READER
  stands on simplicity alone — no claim races, no locking protocol —
  and mount reach licenses and vetoes nothing.

Recommendation (agent): windfall. Nothing in the ruled record runs
agents across machines, and a constraint nobody ordered would
silently veto future mechanisms. Sign it instead if syncthing/sshfs
reach is part of why you want this design. Silent, it stays open:
citable only as `MOUNT_REACH?`, licensing nothing.
