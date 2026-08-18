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

## Inspection boundary

A presentation is a derived view, never a second source of truth. When it conflicts with current artifacts or evidence, their proper validity sources win.

Progressive disclosure governs ordering and compression, not access or review depth. The agent does not assign a risk score, declare a result safe enough to stop reading, or create a special presentation ontology for high-consequence work. The human retains the choice to inspect the complete underlying work.
