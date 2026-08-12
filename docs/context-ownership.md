# Context ownership

Persistent context belongs to the semantic owner and activation boundary that can preserve its meaning without broader loading or duplicated authority.

## Semantic ownership

| Semantic layer               | Content                                                                                     | Canonical context                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Model capability             | General intelligence already available to the model                                         | Do not persist unless a non-inferable preference or contract changes the result                            |
| L0 cross-domain epistemology | Reasoning preferences plus the smallest unconditional authority and routing appendix        | `~/.codex/AGENTS.md`                                                                                     |
| L1 conditional realization   | Domain taste, reusable workflows, or expertise                                              | `~/.agents/skills/`                                                                                      |
| L2 repository truth          | Repository-specific facts, public contracts, local workflows, and evidence-backed rationale | Repository `AGENTS.md`, `.agents/skills/`, or `decisions/` according to activation and retrieval need |
| Transient task state         | One-time constraints, exploration notes, and unconfirmed ideas                              | Current prompt, plan, issue, or other temporary work surface                                               |

A repository needs no `AGENTS.md`, `decisions/`, local skill, hook, or generator when no evidence crosses its creation threshold.

## Activation and enforcement

Activation mechanisms remain orthogonal to semantic ownership:

| Mechanism                  | Activation                                          | Responsibility                                               |
| -------------------------- | --------------------------------------------------- | ------------------------------------------------------------ |
| `AGENTS.md`              | Loaded ambiently at user or repository scope        | Expose the applicable L0 or L2 context                       |
| Skill                      | Loaded when metadata matches or the user invokes it | Realize L1 taste or a reusable workflow conditionally        |
| Human document or decision | Retrieved for its question or rationale             | Preserve motivation, public theory, or durable rationale     |
| Test, hook, or CI          | Triggered by execution or an event                  | Check a mechanically observable part of a canonical contract |
| Generator                  | Invoked explicitly                                  | Materialize repeated deterministic structure                 |

Tests, hooks, and CI are authoritative for the mechanically decidable predicates they execute. They do not own the non-executable rationale, preference, or decision authority behind those predicates. A generator materializes a representation owned elsewhere; neither template presence nor generated output justifies the policy.

## Global and repository rules

[`config/codex/AGENTS.global.md`](../config/codex/AGENTS.global.md) is the public, version-controlled source for the L0 Codex baseline inside a local working tree of `agentic-tend/.github`. `~/.codex/` is Codex's machine-local runtime directory. Linking its `AGENTS.md` to the versioned source exposes the public baseline while leaving `config.toml`, permissions, credentials, sessions, logs, and databases unversioned.

The same L0 meaning may support a future agent runtime by reference or adaptation, with that runtime adding only the discovery and routing required by its own model. Do not extract an agent-neutral base until a second runtime creates concrete pressure.

Codex reads global guidance before more specific repository instructions, so repository `AGENTS.md` files add local context rather than copy L0 or L1 policy. See [AGENTS.md discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md) for the product behavior.

## Skills and mixed work

Skills use progressive disclosure. Codex initially sees skill names and descriptions, then loads full instructions when a task matches. A direct `$skill-name` in a user prompt is documented explicit invocation; the same name inside `AGENTS.md` is an interpreted routing instruction, not a parser-level dispatch guarantee. See [Build skills](https://learn.chatgpt.com/docs/build-skills).

The L0 baseline tells the agent to load and follow `$structure-documentation` for persistent prose, including comments and docstrings inside mixed coding work. This reduces routing misses without copying the prose workflow into every repository. `$software-engineering` remains conditional through metadata that covers software design, implementation, debugging, refactoring, testing, optimization, review, and delivery.

## One owner per decision

Keep one canonical owner for each rule, preference, fact, or rationale. Downstream files navigate to the owner instead of restating it.

When context is inconsistent, classify the problem before changing structure:

- authority conflict: multiple sources claim the same decision;
- abstraction gap: no source owns a repeated decision;
- instance drift: one clear source exists, but an instance violates it.

Correct an authority conflict at the owner, add an abstraction only when the gap blocks work or recurs, and fix instance drift without broadening the policy.

## Decisions, enforcement, and generators

A decision preserves durable rationale; it is not a second instruction file. Link it for human retrieval when useful, but do not require recursive reading to discover executable behavior.

Add event-triggered enforcement only when a canonical contract exposes a reliable mechanical predicate. Punctuation enforcement, for example, should become mechanical only after repeated misses show that routing and skill guidance are insufficient and an acceptable parser exists.

Use a generator only to reduce repeated deterministic materialization of an already owned representation. The former Copier harness was retired because repositories should absorb only the context increment created by their actual data, logic, tooling, and contracts.

## Migration rule

Separate meaning-preserving mechanics from user-owned semantic changes. Treat frequent legacy usage as evidence, not authority, and inspect representative instances before a broad semantic migration.

Pressure-test every applicable operation:

- add only when absence creates a future failure, ambiguity, or repeated cost;
- retain detail that preserves a non-inferable preference, authority, rationale, source, or local contract;
- move useful content when its semantic owner or activation boundary is wrong;
- compress only when structure, behavior-changing distinctions, and citations survive;
- delete only when the content is inferable, obsolete, or already preserved once by its canonical owner.

[`$bootstrap-project-context`](https://github.com/agentic-tend/skills/tree/main/bootstrap-project-context) performs this inspection and applies the minimum sufficient local result. Existing downstream repositories migrate separately when their maintainers choose; retiring the generator does not rewrite consumers automatically.
