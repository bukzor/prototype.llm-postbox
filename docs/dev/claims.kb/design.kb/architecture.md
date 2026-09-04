---
label: ARCHITECTURE
standing: open
ontology:
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

Answering it is the next pass. Until then this rung holds the shape
decisions the person has already ruled, in `architecture.kb/`: that a
delegate is an ordinary session, that an inbox is the optional
cooperative channel, that a standing delegate is a pattern rather than
a primitive, that every inbox has one reader and every address is a
path, and that the substrate is local for now. Two of those decisions are
kept as questions with their answers beside them, chosen and declined
alike: what a delegate is, settled for the session (DELEGATE_PICK),
and what carries the conversation channel, open between the postbox
and SendMessage (CHANNEL_PICK).

The word this rung stipulates: a **watcher** is whatever keeps a
delegate attentive to its inbox between turns.

Existing mechanisms become admissible here, as evidence of what the
substrate can do, only now that mission, goals, and requirements are
settled (FRESH).
