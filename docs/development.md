# Development capability composition

This human-facing model composes capabilities from the traits and uncertainty of current work without imposing a fixed workflow.

## Compose what the task needs

One task may combine software behavior, a programming language, persistent prose, and user-owned semantics. Select each capability for the concern it addresses rather than assigning the entire task to one category.

Resolve uncertainty at its source: inspect discoverable facts, let the applicable capability choose contract-equivalent implementation details, and involve the user only when a choice would change established meaning or observable behavior. The executable boundary lives in the [global interaction contract](../config/codex/AGENTS.global.md) and [`$clarifying-contracts`](https://github.com/agentic-tend/skills/tree/main/clarifying-contracts).

Use `/plan` when implementation-path uncertainty benefits from a decision-complete design. Use `/goal` for durable multi-step work whose outcome and completion evidence are already defined. These are optional coordination surfaces, not stages that every task must pass through.

The Codex [long-running work](https://learn.chatgpt.com/docs/long-running-work) guidance documents these coordination surfaces; this model only determines when their use follows from current task state.

## Composition scenarios

These examples exercise composition boundaries rather than define an exhaustive taxonomy:

| Task state | Capability composition |
| --- | --- |
| Edit plain durable prose without making an artifact-syntax or software decision | `$structure-documentation` |
| Add a table and Mermaid topology to a GitHub README | `$structure-documentation` + `$markdown-authoring` |
| Edit a Documenter.jl manual page or docstring | `$structure-documentation` + `$markdown-authoring` + `$julia-development` |
| Refactor Julia behavior without changing persistent prose | `$software-engineering` + `$julia-development` |
| Choose between two user-visible behaviors in that Julia refactor | Add `$clarifying-contracts` to the same composition |
| Resolve a suspected implementation fact from source or a focused test | Use the applicable software or domain capability; do not activate clarification merely because the fact was initially unknown |
| Perform an indexed Obsidian move | `$obsidian-cli`; add `$markdown-authoring` and `$structure-documentation` only if content changes |

The agent may interleave topology, implementation, prose, and evidence as the current state requires. Capability selection preserves semantic ownership; it does not prescribe a signature-to-implementation-to-comments-to-tests trajectory.

## Revisit perspectives as evidence changes

Inspection, architecture review, planning, and execution may recur in any order as evidence changes the task. They are perspectives to revisit, not a required number of agents or a pipeline.

Start a nontrivial loop from observable success and a working hypothesis, then choose the cheapest evidence that distinguishes the live alternatives. Interpret whether feedback falsifies the implementation, reveals an invalid check or environment, or exposes a user-owned semantic decision. Revisit the relevant perspective and stop when the agreed evidence is complete. Use dialogue when alternatives change the contract; use agent judgment when alternatives are implementation-equivalent.

## Change control

- Update this model when organization-level capability composition or authority boundaries change.
- Update global `AGENTS.md` or a skill only when its executable behavior or dispatch predicate changes.
- Keep public capability and ownership theory in the [capability model](capability-model.md) and [context ownership](context-ownership.md); keep the human composition model here.
- Keep transient execution state in prompts, plans, goals, issues, pull-request bodies, commits, or test failures rather than this durable model.
