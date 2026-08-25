# Context ownership

Context ownership governs the slow loop in which a need survives the current task and becomes durable context. It decides whether persistence is justified, who owns the meaning, how broadly and how long it applies, when it loads, and what it costs to retrieve.

## Persistence loop

Most task pressure should disappear when the task resolves. Persistence becomes a live intervention only when future work cannot reliably reconstruct a material distinction or repeated evidence shows that its absence changes behavior.

```text
durable reconstruction gap
    -> identify validity owner, scope, lifetime, activation, and retrieval cost
    -> apply the minimum sufficient context
    -> observe later work
    -> retain, move, compress, or delete
```

This slow loop consumes evidence from current and later tasks. It does not duplicate the [fast task-data loop](capability-model.md#task-data-feedback-loop), and a valid audit may end with no file change.

## Placement and cache view

Place a durable item first by its validity owner and semantic scope, then choose an activation mechanism that makes it available at acceptable retrieval cost. Lifetime distinguishes a durable contract from transient state; activation distinguishes ambient loading from conditional retrieval.

L0, L1, L2, and transient are cache and retrieval views, not a hierarchy of truth. An L0 rule is broader and loaded earlier than a repository fact, but it is not more valid. Every item remains answerable to its actual source.

| Cache view | Use when | Typical context and activation |
| --- | --- | --- |
| Model capability | General intelligence is sufficient and no non-inferable preference or contract changes the result | Do not persist |
| L0 ambient contract | A cross-domain task-grounding, presentation, or authority boundary applies unconditionally | User-level `AGENTS.md`, loaded by scope |
| L1 conditional capability | Reusable judgment applies only when task traits match | User-level skill, loaded through dispatch |
| L2 repository context | A fact, public contract, local workflow, or rationale is true or required for one repository | Repository `AGENTS.md`, local skill, or decision record according to activation need |
| Transient state | A constraint, observation, hypothesis, or question belongs only to current work | Prompt, plan, issue, or another temporary surface |

These views do not classify an entire task or file and do not prescribe execution order. One task may use repository facts, several conditional capabilities, and an ambient authority boundary at the same time.

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

## Conditional capabilities

Skills use progressive disclosure. Agents initially see skill names and descriptions, then load full instructions when a trait matches[^skill-invocation]. These descriptions are predicates over task traits. They are not membership rules for exclusive task classes.

Each selected capability encapsulates reusable judgment for its concern. Activation does not make it authoritative for task facts, contracts, evidence, or user-owned decisions; it only makes its logic available. The [capability model](capability-model.md) owns composition over shared task data and contracts.

The [multi-agent evidence model](multi-agent.md) owns the public effective theory for separating execution contexts, the [presentation model](presentation.md#multi-agent-plan-and-delivery) owns the human-visible plan and delivery, and `$multi-agent-evidence` owns conditional realization. Separate contexts and feedback edges do not merge semantic owners or prescribe an internal trajectory.

## One canonical source

Define each durable fact, rule, preference, or rationale in one canonical source. Other files route to it instead of restating behavior-changing details. An activation mechanism may carry the minimum executable projection needed when it loads without carrying the public rationale or a backlink. That projection does not become another semantic owner and must not invent a second rationale.

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
