# Presentation and human review

Presentation projects current task state into a reading path that preserves human attention and lets each reader stop after fulfilling their responsibility.

## Why: review bandwidth

AI can generate and revise artifacts much faster than a human can reread them. Repeated full-state review makes unchanged or inferable detail compete with semantic change, consumes scarce attention, and increases the chance that an almost-correct result survives because the reviewer is exhausted.

Every sentence or semantic block therefore needs a reader-facing function. It must answer the current question or supply context, a result, a relation, evidence, a boundary, or an action that the remaining reading path needs. If removing it loses none of those functions, it should not compete for attention. This task-grounded need gives the reader a reason to continue.

The reader receives a compact first view and a clear path to recover as much detail as their responsibility or curiosity requires.

## Three projection axes

Every answer, question, plan, update, summary, and handoff is a human-facing projection from current [task data](capability-model.md#task-data-feedback-loop), results, and evidence. The current judgment selects the relations it needs from three axes.

| Axis | Direction | Relation generated |
| --- | --- | --- |
| Reader responsibility | interface -> subsystem -> implementation | The detail this reader needs to act or review |
| Semantic depth | why -> what -> how | The reason for a boundary, the relation it preserves, and its next realization |
| Intra-layer traversal | prerequisite -> dependent claim | The context each following claim consumes |

### Responsibility: interface to implementation

Lead with the smallest interface-level result that lets the least implementation-responsible reader make the current judgment. Descend through subsystem contracts, evidence, and implementation as later responsibilities require. Promote detail when it changes an earlier reader's judgment.

### Semantic depth: why to what to how

Within any responsibility layer, generate the semantic roles needed for the current judgment. When more than one role is present, order them by dependency:

- **Why:** establish the pressure, stake, obstruction, or question that gives this boundary a reason to exist.
- **What:** establish the outcome, relation, and constraint that this boundary must preserve and the reader must judge.
- **How:** expose the next projection or realization required at this responsibility layer.

When a lower-layer realization becomes independently meaningful, `how_L` becomes `what_(L+1)`. The relation recurs as detail creates another current judgment. Evidence follows a separate feedback edge from a claim to the validity source that evaluates it.

### Representation and validity: inputs to generated objects

The current judgment selects a representation path for the object it needs and connects the resulting claim to evidence feedback:

| Path | Consumes | Generates | Feeds |
| --- | --- | --- | --- |
| Natural language | Task situation, intent, authority, and evidence | Motivation, meaning boundary, contract candidate, uncertainty, and open question | Human judgment and the next semantic block |
| Pseudocode or structured IR | Established meaning and domain terms | A reviewable relational model of decision owners, state owners or actors, data, conditions, ordered transformations, state transitions, effects, and failures | Discussion, clarification, or target realization |
| Target formal language | Relational model and host constraints | A syntax-governed committed artifact | Parser, compiler, runtime, renderer, or checker |
| Evidence feedback | Artifact, criterion or oracle, and observation | Support status, counterexample, measurement, provenance, and remaining uncertainty | Task data and the claim it evaluates |

A **decision owner** holds authority to choose meaning or constraints. A **state owner** is responsible for information retained across steps, while an **actor** performs a transformation or effect. **Data** is the information consumed, produced, or retained. A **condition** selects a branch. A **state transition** relates an observable before-state to an after-state. An **effect** is a consequence visible outside the selected boundary. **Failure propagation** establishes control and effects when the intended postcondition cannot be met. An **oracle** is the criterion or external source that judges the realization.

Pseudocode exposes the smallest set of these relations needed for the current judgment while leaving replaceable target-language mechanics to realization. Current intent determines whether the projection feeds human dialogue, immediate realization, or artifact delivery. The L0 interaction contract owns turn continuation; the active domain capability owns the projected relations and surfaces any user-owned meaning.

### Traversal: prerequisite DAG

Within a layer, put each prerequisite, definition, or distinction before the statement that depends on it. Start from available context, add one needed relation, and leave the context required by the next sentence.

Compression preserves every distinction that can change judgment, including observable behavior, contracts, authority, assumptions, trade-offs, material uncertainty, validation boundaries, and relevant provenance. Inferable or unchanged detail remains subordinate and reachable through the underlying artifact or evidence.

The agent chooses block boundaries and disclosure depth from these axes, validity sources, and reader choices. Use the plainest domain-appropriate language that preserves the meaning. Contrast enters the reading path when current task data contains a live alternative whose resolution can change judgment.

The resulting decomposition exposes task understanding: coherence supports the chosen reading path, while proper validity sources support the underlying claims. A mixed objective, contract, authority, uncertainty, or evidence boundary returns to task data for a better decomposition or a user-owned decision.

## Multi-agent plan and delivery

When `$multi-agent-evidence` activates, the coordinator presents a structured plan before delegation. The plan makes the effective agent boundary observable, and execution pauses for a user-owned semantic choice, new authority, or another boundary that requires human action.

The plan exposes the smallest semantic blocks needed to understand:

- the motivation and observable outcome;
- the active ports and why each exists;
- each port's inputs, outputs, and withheld information;
- the feedback edges and stopping evidence;
- authority boundaries and claims that cannot yet be validated.

Arrange these blocks by their logical dependencies and combine blocks that serve the same judgment. Delegation begins after this effective boundary is visible.

After execution, the delivery exposes the agents' effect on human judgment. Expand the roles produced by current task data:

```text
Why
Outcome
Agreement
Disagreement
Evidence
Unvalidated
Details
```

Omit empty roles, collapse a simple result, and recursively expand a complex one. Agreement records compatibility among current claims and observations. Proper validity sources determine their support. Disagreement and unvalidated claims appear in the earliest layer where they can change judgment.

Details keep design, implementation, checks, falsification attempts, provenance, and accessible raw artifacts reachable. Link to available files, tool outputs, and lane evidence. An unavailable underlying transcript or artifact produces an explicit audit gap.

Presentation compression and verification depth follow separate decisions: responsibility, authority, and the reader's questions determine how far to inspect, while the presentation preserves every available route needed to continue.

## Validity and review path

Current artifacts and their proper validity sources decide each claim. Presentation supplies the reading path and provenance needed to continue that judgment.

The human chooses review depth and may follow every available provenance path. Unavailable evidence remains an explicit limitation at the earliest layer where it can change judgment.
