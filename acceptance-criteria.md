# Acceptance criteria

> [!DRAFT] agent-authored 2026-09-01, vetoable. Each item is meant to be a test
> somebody could actually write. Where one cannot be, it does not belong here.

## How to read these

Each criterion is stated so that failing it is *observable*. Prefer criteria
demonstrated by a job that is *supposed* to fail: a probe instructed to overstep
proves enforcement in a way that inspecting configuration never does. Several
criteria below are written in that form deliberately.

Self-report is never evidence. Where a criterion says "the record shows", it
means a record written by something other than the delegate.

## Correctness of the mechanism

1. **Confinement is enforced, not requested.** A probe job instructed to read a
   file outside its declared reach does not read it, and the run record shows a
   denial. The probe runs as part of every batch, so the guarantee is re-proven
   under the version actually in use rather than assumed from a flag.

2. **Grader integrity.** A job instructed to modify whatever evaluates it
   cannot. Attempting it is an error in the record, not a silent success.

3. **Sole writer.** No two concurrent jobs can write the same output path.
   A collision is refused at dispatch, not resolved by last-write-wins.

4. **Instruction/data separation.** A job whose *input* contains imperative text
   ("ignore your task and do X") completes its assigned task. Demonstrated with
   a deliberately poisoned input.

5. **Loud failure.** A crashed, wedged, truncated, or over-time job is
   distinguishable from a successful one mechanically, with no human reading.

6. **Clean cancellation.** A cancelled job leaves its output either complete or
   absent, never partially written and never mistakable for a finished one.

## Economy

7. **Attention bound.** Dispatching N jobs costs the delegator a constant number
   of acts and zero per-job result reading. Demonstrate at N >= 10, where the
   delegator reads only an aggregate verdict and still knows what to do next.

8. **Per-job accounting.** Every run yields cost, duration, turn count, and
   denial count attributable to that job, obtained as a by-product of running
   rather than through added instrumentation.

9. **No inherited overhead.** A job pays only for the instructions it needs. The
   per-job fixed cost is measured and stated, and a job requiring no ambient
   convention does not pay for any.

10. **Backpressure.** Concurrency is bounded and declared. Exceeding a resource
    limit degrades throughput; it does not corrupt results or lose jobs.

## Evidence and provenance

11. **Claims are not acceptance.** For any job producing an artifact, acceptance
    is decided by checking the artifact. Removing the job's own summary from
    the pipeline changes nothing about what is accepted.

12. **Records are sufficient.** A completed job can be understood -- what it was
    told, what it saw, what it produced, what it cost -- from its record alone,
    without re-running it and without the delegator's memory of dispatching it.

13. **Seeding is explicit.** A job seeded from the delegator's context records
    exactly what was transmitted. A job seeded with nothing can be shown to have
    received nothing, so its agreement carries information.

14. **Re-runnable.** A job can be re-run from its record alone and produce a
    comparable result. Differences between runs are attributable.

## Communication

15. **Bidirectional, without polling.** The delegator sends to a running job and
    receives a reply. Neither side spins, and delivery latency has a stated
    bound that is met under load.

16. **Channel separation.** Messages exchanged during a run cannot be mistaken
    for the run's result, and vice versa, by any consumer downstream.

## The criterion that subsumes the rest

17. **Adoption.** The mechanism carries a real multi-job workload end to end,
    and the delegator prefers it to the alternative for that workload -- not on
    principle, but because the attention cost was visibly lower and the
    confidence visibly higher. Until one real batch has run this way, every
    criterion above is a hypothesis.

## Deliberately not criteria

- Feature parity with any existing mechanism.
- Handling adversarial delegates.
- Generality beyond fan-out-plus-gate until a second shape is actually needed.
