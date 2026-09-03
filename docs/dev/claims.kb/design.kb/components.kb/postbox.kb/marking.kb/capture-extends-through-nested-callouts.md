---
label: CAPTURE_NESTS
standing: user
authority: 'owner ruling 2026-08-29: "we can specify that <callout/>
  captures *all* later-sibling content, even further callout blocks,
  which means a subsequent <callout tag=\"@user\"> is (correctly) read as
  claude mentioning a @user callout."'
why:
  - capture-runs-to-the-later-siblings.md
---

# Capture extends through later callout tags

A later marker does not end the capture in force; it is captured too.

So a `<callout tag="@user"/>` appearing inside an `@claude` capture
reads as Claude mentioning a `@user` callout — which is what in fact
happened — rather than as a hand-back to the user. The reading that
falls out of the parse is also the true one.
