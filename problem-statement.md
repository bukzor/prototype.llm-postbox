# Problem statement: delegation as a first-class mechanism

> [!DRAFT] agent-authored 2026-09-01, vetoable. Written to be argued with.
> Nothing here is settled; the framing is the part most worth attacking.

## The exchange being made

An agent delegates for two reasons, and only two: to do more work than fits in
one context, and to obtain a reading that its own assumptions did not produce.

Both are purchases, and the currency is the delegator's attention. A delegation
mechanism is good exactly insofar as it improves that exchange rate:

- **attention spent per unit of work delegated** -- setup, supervision, and
  reading the result all count, and the last is usually the largest
- **authority granted per unit of work delegated** -- what the delegate may
  see, change, and send
- **confidence obtained per unit of attention spent** -- how cheaply the
  delegator can establish that the work was actually done

A mechanism that returns a confident summary the delegator must read in full has
sold nothing: the attention was spent, merely later and in a worse form. A
mechanism that grants a delegate the run of the machine to edit one file has
overpaid in authority. A mechanism whose output must be trusted because checking
it costs as much as doing it has failed at the third.

## What the mechanism must provide

**Attention.** Dispatch costs a small bounded act. Output does not enter the
delegator's attention by default -- it lands somewhere addressable and stays
there until asked for. Many jobs cost little more attention than one. Progress
and completion are observable without polling.

**Authority.** Each job declares its reach: what it may read, write, run, fetch,
and send. Something other than the delegate enforces this, and the enforcement
leaves evidence in the record, so compliance is auditable without trusting the
delegate's account of itself. The default is the least authority that could
accomplish the task; every widening is deliberate and visible.

**Verifiability.** A job's *claims* and its *artifacts* are separable, and
acceptance rests on the artifacts. The run record is durable and complete
enough -- instruction, inputs, outputs, cost, duration, every denial -- to
reconstruct what happened without re-running. Whatever grades a job is beyond
that job's reach.

**Communication.** The delegator can reach a running delegate and be reached by
it. This channel is distinct from the result channel, so that a conversation
does not silently become an artifact, nor an artifact a conversation. Neither
direction spins.

**Lifecycle.** Start, observe, interrupt, resume, cancel -- each reliable, each
available to the delegator, none requiring the delegate's cooperation. A wedged
or dead delegate is detectable and reapable.

**Provenance.** A delegate begins from an explicitly chosen basis: nothing, a
named brief, or a designated slice of the delegator's context. Which one, and
exactly what was transmitted, is recorded -- otherwise "independent
confirmation" is unfalsifiable, because nobody can say what was assumed.

**Reproducibility.** A job is a value. It can be written down, stored, re-run,
and diffed against its previous run.

## Failure modes to design against

These are the classes worth engineering against, in rough order of how quietly
they do damage:

1. **Unearned confidence.** The delegate reports success it did not achieve,
   and the report is the only evidence anyone looks at.
2. **Jurisdiction drift.** The delegate reaches material outside its task and
   treats it as evidence -- diligently, correctly, and wrongly.
3. **Grader capture.** The delegate modifies whatever evaluates it, and then
   passes. Especially dangerous because it looks like initiative.
4. **Silent collision.** Two delegates write the same artifact; the last one
   wins and nothing announces it.
5. **Attention flood.** Results return in a form that must be read, so
   delegating costs more than doing.
6. **Aggregate-only cost.** Spend is knowable in total and after the fact, never
   per job and never in time to change a decision.
7. **Data acting as instruction.** Text that entered the delegate's view as
   material to examine gets obeyed as a directive.
8. **Unintended inheritance.** The delegate absorbs the delegator's assumptions
   through some channel nobody declared, and its agreement means nothing.

## Threat model

The delegate is **capable, well-intentioned, and fallible**. It is not an
adversary. The adversary, insofar as there is one, is *text*: material a job was
asked to examine, which reads as instruction.

This choice sets the engineering budget. Defences should be cheap, mechanical,
and aimed at honest error -- confinement that catches a wrong turn, gates that
catch a wrong claim -- not at a delegate actively trying to escape.

## Non-goals

- A general workflow or DAG engine. Jobs are mostly independent; fan-out with a
  gate is the shape that matters.
- Multi-user or multi-tenant operation.
- A security sandbox against hostile code.
- Preserving any existing interface, vocabulary, or decomposition.

## The question this directory exists to answer

What is the smallest mechanism that delivers the seven properties above, given
that the delegate is an agent, the substrate is a filesystem and a process
table, and the delegator is itself an agent with a finite context?
