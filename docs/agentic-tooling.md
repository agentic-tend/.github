# Agentic tooling

This file defines Agentic Tend's public model for growing agentic software-development tooling without confusing ambient guidance, reusable workflows, and mechanical enforcement.

## Philosophy

`Tend` means caring for a growing system: add structure when evidence calls for it, keep each layer composable, and let projects retain their own shape.

- Establish contracts before implementation.
- Grow structure from observed needs and recurring failures.
- Give agents maps and boundaries instead of loading an entire system indiscriminately.
- Prefer small, composable layers over monolithic agent configurations.
- Evaluate observable outcomes rather than treating generated structure as proof of better behavior.

## Mechanisms

| Mechanism | Activation | Primary role | Enforcement |
| --- | --- | --- | --- |
| Rules | Loaded from the applicable scope, as with `AGENTS.md` | Declare ambient constraints and project context | Interpreted by the agent |
| Skills | Discovered by metadata and loaded when a task calls for them | Package specialized knowledge, workflows, and resources | Interpreted by the agent |
| Hooks | Triggered by a defined event | Observe, automate, block, or transform an operation | May execute mechanically, call external systems, or delegate back to an agent |

Rules, skills, and hooks often become more specialized and mechanically constrained in that order, but this tendency does not define them.
A repository rule can be highly specific, a skill can be portable, and a hook may lose determinism when it delegates judgment to a model or relies on nondeterministic external state.

## Ownership

- The [rules layer](https://github.com/agentic-tend/copier-coding-harness) distributes a language-independent, contract-first repository harness.
- The [skills layer](https://github.com/agentic-tend/skills) packages reusable, on-demand workflows outside any one repository's ambient rules.
- Hooks remain an unshipped extension point until concrete events and enforcement requirements justify an interface and repository.

Each layer owns its implementation, user documentation, and delivery roadmap.
This organization documentation owns only the model and decisions that coordinate or compare layers.

## Evaluation

Rendered files prove structure, not improved agent behavior.
Evaluation should compare observable agent outcomes before and after a context change against an explicit oracle, then attribute the result to the relevant rule, skill, or hook.

The [Tessl documentation](https://docs.tessl.io/) is a practical reference for reviewing agent context and using [scenario evaluations](https://docs.tessl.io/improving-your-skills/evaluate-skill-quality-using-scenarios) to test whether a skill changes agent output.
It is a reference rather than a project dependency, adopted evaluation platform, or general-purpose agent benchmark.

## See also

- [Organization roadmap](roadmap.md) tracks evidence and extension work spanning multiple layers.
