---
label: FLAG_SURFACE
standing: agent
why:
  - only-the-wrapper-is-pre-approved.md
---

# The wrapper accepts a fixed flag set

Pre-approval attaches to the wrapper's name (WRAPPER_ONLY), so a
wrapper that forwarded arbitrary flags to `claude` would hand straight
back what gating the bare command withheld.

It therefore accepts a named, enumerated set of options and rejects
everything else. Widening that set is a decision about what runs
unprompted, and belongs to the owner rather than to whoever next needs
a flag.
