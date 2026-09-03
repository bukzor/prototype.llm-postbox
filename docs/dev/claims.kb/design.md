---
label: DESIGN
standing: agent
ontology:
  - mission
  - goals
  - requirements
  - architecture
  - components
  - deliverables
  - experience
  - session
stale-when: a rung nothing cites and nothing fills, or a claim that fits no rung -- the stratification wants re-deriving from what this project actually argues about
---

# agent-harness -- the design, as a ledger

A mechanism by which one agent creates, constrains, observes, converses
with, and judges other agents. This ledger is the design record
(`Skill(llm-design-kb)`): one claim per file, label and standing in
frontmatter, one theory per collection. Argue with a claim by editing
its file; the git diff is the strikethrough.

A **session** is the interactive claude-code session the person works
in. It is the thing a delegate is measured against, and the word is
stipulated here so every rung may use it.

Six rungs, each a theory whose `why:` names the rung it serves, plus one
auxiliary theory of evidence the rungs rest on and do not argue:

| Theory | The question it answers |
|---|---|
| `experience` | What has the person actually hit, delegating today? |
| `mission` | What problem are we solving? Who benefits? |
| `goals` | How do we accomplish the mission? |
| `requirements` | How do we validate the goals are achieved? |
| `architecture` | How do we satisfy the requirements? |
| `components` | How do we implement the architecture? |
| `deliverables` | How do we build the components? |

Mission, goals, and requirements are filled and mostly user-signed.
Architecture holds the open question this project exists to answer and
the few shape decisions already ruled. Components and deliverables are
empty: nothing is built.

Priors are a DAG, not a ladder: a claim's `why:` names whatever claims
it would be revisited over, one rung up or four.

## Scans

```bash
grep -rH '^standing:' docs/dev/claims.kb/     # who signed what
grep -rHE '^standing: (open|agent)' docs/dev/claims.kb/   # wants an answer, or a veto
grep -rl '^todo: true' docs/dev/claims.kb/    # decided, not yet built
grep -rl 'verdict:' docs/dev/claims.kb/       # taken out of force
llm-claims-kb-flatten docs/dev/claims.kb/design.kb   # the whole ledger as one text
```
