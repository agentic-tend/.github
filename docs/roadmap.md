# Organization roadmap

This roadmap tracks evidence and changes that coordinate more than one Agentic Tend semantic owner or activation mechanism.

## Shipped locally

- [x] Preserve [`copier-coding-harness` `v0.4.4`](https://github.com/agentic-tend/copier-coding-harness/tree/v0.4.4) as the last usable generic template revision.
- [x] Replace generic scaffolding with the reusable [`bootstrap-project-context`](https://github.com/agentic-tend/skills/tree/main/bootstrap-project-context) inspection and application workflow.
- [x] Extract software-engineering taste into the conditional [`software-engineering`](https://github.com/agentic-tend/skills/tree/main/software-engineering) skill without flattening its implementation, testing, and delivery references.
- [x] Extract persistent prose behavior into [`structure-documentation`](https://github.com/agentic-tend/skills/tree/main/structure-documentation).
- [x] Define the [knowledge and evidence flow](agentic-tooling.md#knowledge-and-evidence-flow), with semantic ownership ending at L2.
- [x] Keep the [activation and enforcement model](context-ownership.md#activation-and-enforcement) orthogonal to semantic ownership.
- [x] Version the [L0 Codex baseline](../config/codex/AGENTS.global.md) separately from runtime configuration.

These items describe the prepared repository state. Publishing remains a maintainer-controlled sequence: skills, then `.github`, then the harness tombstone. Repository archival remains a separate final action.

## Behavioral evidence

- [ ] Record representative explicit and implicit skill scenarios without leaking expected answers into the evaluator, and pre-register a source-grounded objective and rubric.
- [ ] Compare mixed code-and-prose tasks with pure-code negative controls.
- [ ] Mine execution logs and maintainer feedback for real failure cases, then retain confirmed cases as regressions.
- [ ] Calibrate automated graders and proxies against human judgment before using them as admission gates.
- [ ] Add mechanical prose enforcement only after repeated misses and a reliable low-noise oracle.
- [ ] Link each future context change to an observed need, non-inferable preference, durable contract, or repeated workflow.

## Migration

- [ ] Migrate downstream repositories independently when their maintainers request it.
- [ ] Keep historical Copier consumers pinned to `v0.4.4`; do not derive updates from tombstone `main`.
- [ ] Archive `copier-coding-harness` manually after skills, organization documentation, and the tombstone are published.

## Extension threshold

Create no central hooks repository or new generator by default. First identify a concrete event or repeated schema, its owner, its oracle, and the evidence that interpreted guidance or direct maintenance is insufficient.
