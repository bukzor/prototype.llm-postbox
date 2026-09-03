---
label: ARCHITECTURE
standing: open
ontology:
  - inbox
  - watcher
why:
  - requirements.md
  - goals.md
  - mission.md
---

# Architecture

**How do we satisfy the requirements?**

Open. The question this project exists to answer is:

> What is the smallest mechanism that delivers the goals, given that the
> delegate is an agent, the substrate is claude-code sessions over a
> local filesystem and a process table, and the delegator is itself an
> agent with a finite context?

Answering it is the next pass. Until then this rung holds only the shape
decisions the person has already ruled, in `architecture.kb/`: that a
delegate is a session, that an inbox is the optional cooperative
channel, that a standing delegate is a pattern rather than a primitive,
and that the substrate is local for now.

Words this rung stipulates:

- an **inbox** is a directory a delegate watches, into which a delegator
  writes to reach it;
- a **watcher** is whatever keeps a delegate attentive to its inbox
  between turns.

Existing mechanisms become admissible here, as evidence of what the
substrate can do, only now that mission, goals, and requirements are
settled (FRESH).
