---
label: FAIL_SAFE
standing: user
why:
  - the-marker-is-a-privilege-drop.md
---

# Scope error is asymmetric

Because the marker only lowers authority (DROP), capturing more than
intended costs nothing but a little under-weighting: some of the
owner's own words are taken as an agent's. Capturing less than
intended is the failure that matters, and a fiddly scope rule is what
makes it likely.

So where the two trade off, the design prefers over-capture, and it
spends no correctness effort on tightening scope.
