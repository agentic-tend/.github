# Presentation and human review

Agent-authored presentation uses progressive disclosure to make rapidly produced work reviewable without deciding how deeply a human should inspect it.

## Why: review bandwidth

AI can generate and revise artifacts much faster than a human can reread them. Repeated full-state review makes unchanged or inferable detail compete with semantic change, consumes scarce attention, and increases the chance that an almost-correct result survives because the reviewer is exhausted.

The goal is not to restrict inspection. It is to give the reader a compact first view and a clear path to recover as much detail as their responsibility or curiosity requires.

## What: a progressive projection

Every agent-authored answer, question, plan, update, summary, and handoff is a human-facing projection from current [task data](capability-model.md#task-data-and-feedback), results, and evidence. The first visible layer gives the smallest sufficient understanding of why the presentation exists and what materially follows. Further layers expose how that result is structured, supported, or realized.

The dependency order is:

> why -> what -> how

These are semantic roles, not mandatory headings or a fixed number of levels. A one-line factual answer may collapse them into one layer. A complex result may apply the same dependency recursively inside several blocks.

Compression removes rereading cost, not meaning. Preserve any distinction whose absence could change judgment, including observable behavior, contracts, authority, assumptions, trade-offs, material uncertainty, validation boundaries, and relevant provenance. Inferable or unchanged detail should not compete for first attention, but it remains reachable through the underlying artifact or evidence when one exists.

## How: adaptive semantic granularity

The agent chooses block boundaries and disclosure depth from the result's logical dependencies, validity sources, and independent reader choices. It does not partition by word count, file count, implementation volume, risk tier, or a universal section taxonomy.

This partition is also a check on task understanding. If a presentation cannot separate why, what, and how without mixing distinct objectives, contracts, authorities, uncertainties, or evidence, the agent should revisit the task data, derive a better decomposition, or return an unresolved semantic choice to the user. A polished hierarchy is evidence that the input has been organized coherently; it is not evidence that the underlying claims are correct.

## Multi-agent plan and delivery

When `$multi-agent-evidence` activates, the coordinator presents a structured plan before delegation. This makes the effective agent boundary observable without exposing or prescribing micro-orchestration. Plan visibility is not an approval gate; execution pauses only for a user-owned semantic choice, new authority, or another boundary that already requires human action.

The plan exposes the smallest semantic blocks needed to understand:

- the motivation and observable outcome;
- the active ports and why each exists;
- each port's inputs, outputs, and withheld information;
- the feedback edges and stopping evidence;
- authority boundaries and claims that cannot yet be validated.

These are not required headings. Collapse or arrange them according to their logical dependencies, but expose them before any delegation occurs.

After execution, the delivery exposes the agents' effect on human judgment rather than concatenating their transcripts. A useful result may progressively disclose these semantic roles:

```text
Why
Outcome
Agreement
Disagreement
Evidence
Unvalidated
Details
```

This is an example projection, not a required template. Omit empty roles, collapse a simple result, and recursively expand a complex one. Agreement means that current claims and observations are compatible, not that they prove correctness. Disagreement and unvalidated claims appear in the earliest layer where they could change judgment.

Details keep design, implementation, checks, falsification attempts, provenance, and accessible raw artifacts reachable without making agent transcripts the default reading surface. Link to available files, tool outputs, and lane evidence. If the runtime does not expose an underlying transcript or artifact, identify that audit gap instead of claiming complete traceability or creating a new transcript store.

Presentation compression and verification depth are independent: responsibility, authority, and the reader's questions determine how far to inspect, while the presentation preserves every available route needed to continue.

## Inspection boundary

A presentation is a derived view, never a second source of truth. When it conflicts with current artifacts or evidence, their proper validity sources win.

Progressive disclosure governs ordering and compression, not access or review depth. The agent does not assign a risk score, declare a result safe enough to stop reading, or create a special presentation ontology for high-consequence work. The human retains the choice to follow every available provenance path, and unavailable evidence remains an explicit limitation.
