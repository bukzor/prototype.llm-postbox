---
label: PATH_ADDRESS
standing: agent
why:
  - single-reader-inboxes.md
---

# The convention's only address is a path

Everything the convention names — inbox, message, the `read/` record —
is a filesystem path; there is no registry, no API, no daemon. The
roster is `ls` of the postbox plus tmux window names. Any
mount (s3fs, sshfs, syncthing) therefore extends the convention
cross-machine with no change to agent instructions. This holds only
while SINGLE_READER does: a claim-queue would smuggle in operations
weak mounts cannot honor.
