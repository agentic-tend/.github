# Context ownership

Persistent context should preserve meaning that future readers or runtimes cannot reliably reconstruct from current state.

## What to persist

Place a durable item by asking what makes it valid and how broadly it must apply. General capability needs no stored policy; an unconditional cross-domain preference belongs at L0; a reusable capability activated by task traits belongs at L1; a repository-specific fact or contract belongs at L2; and one-time or unconfirmed state remains transient. This semantic source and scope determine the layer below, while availability requirements determine activation separately.

| Semantic layer | Identifying condition | Canonical context |
| --- | --- | --- |
| Model capability | General intelligence is sufficient and no non-inferable preference or contract changes the result | Do not persist |
| L0 cross-domain epistemology | A reasoning preference or authority boundary applies unconditionally across domains | `~/.codex/AGENTS.md` |
| L1 conditional realization | Reusable taste, workflow, or expertise applies only when task traits match | `~/.agents/skills/` |
| L2 repository truth | A fact, public contract, local workflow, or rationale is true or required for one repository | Repository `AGENTS.md`, `.agents/skills/`, or `decisions/` according to activation and retrieval need |
| Transient task state | A constraint, observation, hypothesis, or question belongs only to current work | Current prompt, plan, issue, or other temporary work surface |

These layers do not classify an entire task or file, and they do not prescribe execution order. One task may use L2 facts, several L1 capabilities, and an L0 authority boundary at the same time.

A repository needs no `AGENTS.md`, `decisions/`, local skill, hook, or CI check when no evidence crosses its creation threshold.

## Activation and enforcement

Activation answers when context becomes available, not whether its content concerns the acting subject, an operation (predicate), or the targeted object. `Ambient` is reserved here for body content loaded by scope without task-specific retrieval. Skill descriptions support dispatch before skill bodies load; semantic documents are retrieved when their question matters; tests, hooks, and CI run through execution or events.

`README.md` is repository-discovery infrastructure rather than ambient context. Its conventional name makes directory meaning and navigation discoverable before or alongside capability dispatch; the global rule owns only that retrieval protocol, while each README's content remains repository-owned task data and must be checked against current state.[^readme-discovery]

| Mechanism | Becomes available when | Responsibility |
| --- | --- | --- |
| `AGENTS.md` body | Loaded ambiently at the applicable user or repository scope | Expose the applicable L0 or L2 context |
| `README.md` | Discovered by its conventional name while establishing repository task data | Expose directory-level meaning and navigation without becoming an ambient policy owner |
| Skill | Its description supports dispatch; its body loads when traits match or the user invokes it | Realize one or more applicable L1 capabilities |
| Semantic document or decision record | Retrieved when its question or rationale matters | Preserve public theory and non-inferable semantics for humans and agents |
| Test, hook, or CI | Triggered by execution or an event | Check a mechanically observable part of a canonical contract |

Tests, hooks, and CI are authoritative for the mechanically decidable predicates they execute. They do not own the non-executable rationale, preference, or decision authority behind those predicates.

## Global and repository rules

[`config/codex/AGENTS.global.md`](../config/codex/AGENTS.global.md) is the public, version-controlled source for the L0 Codex baseline inside a local working tree of `agentic-tend/.github`. `~/.codex/` is Codex's machine-local runtime directory. Linking its `AGENTS.md` to the versioned source exposes the public baseline while leaving `config.toml`, permissions, credentials, sessions, logs, and databases unversioned.

The same L0 meaning may support a future agent runtime by reference or adaptation, with that runtime adding only the discovery and routing required by its own model. Do not extract an agent-neutral base until a second runtime creates concrete pressure.

Agents read global guidance before more specific repository instructions, so repository `AGENTS.md` files add local context rather than copy L0 or L1 policy.[^agents-discovery]

## Skills and capability composition

Skills use progressive disclosure. Agents initially see skill names and descriptions, then load full instructions when a trait matches[^skill-invocation]. These descriptions are predicates over task traits. They are not membership rules for exclusive task classes.

A software task can simultaneously require software topology and testing, Julia semantics, persistent prose, Markdown realization, and semantic clarification. Persistent natural language that is itself the task object may dispatch directly to `$structure-documentation`. In mixed software work, `$software-engineering` owns whether embedded prose is justified and which software meaning it must preserve, `$structure-documentation` owns the resulting language-independent organization and expression, an artifact-language capability such as `$markdown-authoring` owns source realization, and a host-language capability owns its syntax and renderer extensions.

Each selected capability encapsulates the validity source for its concern and exposes inputs and outputs at the same boundary. Shared task data and contracts form the composition seam; orchestration does not merge owners or prescribe a fixed internal trajectory.

## One canonical source

Define each durable fact, rule, preference, or rationale in one canonical source. Other files link to it instead of restating behavior-changing details.

When context is inconsistent, classify the problem before changing structure:

- authority conflict: multiple sources define the same fact, rule, preference, or rationale;
- abstraction gap: no source preserves a repeated requirement;
- instance drift: one clear source exists, but an instance violates it.

Correct an authority conflict at the canonical source, add an abstraction only when the gap blocks work or recurs, and fix instance drift without broadening the policy.

## Migration rule

Separate meaning-preserving mechanics from user-owned semantic changes. Treat frequent legacy usage as evidence, not authority, and inspect representative instances before a broad semantic migration.

Pressure-test every applicable operation:

- add only when absence creates a future failure, ambiguity, or repeated cost;
- retain detail that preserves a non-inferable preference, authority, rationale, source, or local contract;
- move useful content when its semantic owner or activation boundary is wrong;
- compress only when structure, behavior-changing distinctions, and citations survive;
- delete only when the content is inferable, obsolete, or already preserved once by its canonical owner.

[`$bootstrap-project-context`](https://github.com/agentic-tend/skills/tree/main/bootstrap-project-context) performs this inspection and applies the minimum sufficient local result. Existing downstream repositories migrate separately when their maintainers choose.

[^skill-invocation]: *A direct `$skill-name` in a user prompt is documented explicit invocation; the same name inside `AGENTS.md` is an interpreted routing instruction, not a parser-level dispatch guarantee.* See [Build skills](https://learn.chatgpt.com/docs/build-skills).
[^agents-discovery]: See [AGENTS.md discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md) for the product behavior.
[^readme-discovery]: GitHub recognizes and automatically surfaces README files at conventional repository locations. See [About the repository README file](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes). Agentic Tend's root-to-target traversal is its own routing convention.
