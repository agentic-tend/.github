# Agentic tooling

Agentic Tend preserves objectives and preferences that general model capability cannot reliably infer, then places each one at the narrowest justified owner and activation boundary.

## Motivation

Richard Sutton's *The Bitter Lesson*[^bitter-lesson] argues that scalable learning and search ultimately outperform attempts to hand-code human domain knowledge into intelligent systems.

Agentic Tend derives a tooling maxim from that lesson:

> Do not encode intelligence that can be learned; encode objectives and preferences that cannot be inferred.

It does not imply deleting every `AGENTS.md` or skill as models improve. Cross-domain epistemology, personal taste, authority boundaries, local facts, and public contracts remain justified when stronger general capability still cannot infer them.

`Tend` means caring for a growing system: let useful instances expose pressure, introduce only the structure that pressure requires, and preserve the distinctions needed for later judgment.

## Pressure before structure

The governing sequence is:

> observed need -> minimal persistent structure

Minimal means minimum sufficient and lossless, not the fewest files or shortest prose. Apply the same counterfactual discipline to addition and subtraction: persist a distinction only when its absence would change future judgment, move it when its owner or activation boundary is wrong, and compress or delete it only when meaning, rationale, and sources remain recoverable. The [context ownership model](context-ownership.md) owns the operational tests for each migration action.

Generated structure and smaller diffs are evidence only when they improve an observable contract or remove a demonstrated cost.

## Knowledge and evidence flow

```text
model capability
    -> L0 cross-domain epistemology
    -> L1 conditional domain realization
    -> L2 repository facts and contracts
    -> mechanical oracle
```

- Model capability supplies general intelligence that should not be copied into project policy.
- L0 records unconditional cross-domain reasoning preferences and the smallest authority and routing appendix.
- L1 skills realize those preferences for a domain or workflow, such as [software engineering](https://github.com/agentic-tend/skills/tree/main/software-engineering) or [persistent prose](https://github.com/agentic-tend/skills/tree/main/structure-documentation).
- L2 repository context records what is true or required specifically in one project.
- Tests, CI, and hooks verify mechanically observable conditions without asking the model to remember them.

Semantic ownership ends at L2. The mechanical oracle closes the flow as an executable projection of the observable contract; it is not another semantic owner. This flow answers what deserves encoding and how it becomes evidence, without replacing the activation mechanisms below.

## Intellectual influences

The L0 reasoning principles distill several compatible but non-identical traditions:

- Yang Chen-Ning's preference for plain, substantial work, summarized by "宁拙毋巧, 宁朴毋华", supports derivation and robustness over display or tricks. Tsinghua's account of his [permeative learning](https://www.tsinghua.edu.cn/info/3225/121939.htm) also motivates gradual immersion: continue through partial understanding while increasingly constraining observations connect points into a whole. See also Tsinghua's account of his [plain research style](https://www.tsinghua.edu.cn/info/3225/121987.htm).
- Grothendieck's rising-sea image describes problems becoming natural as a surrounding conceptual world develops. McLarty's [The Rising Sea](https://ncatlab.org/nlab/files/McLartyRisingSea.pdf) documents that method. Agentic Tend inherits the preference for structural derivation and gradual immersion, but not unconditional generalization: a larger theory must still answer concrete pressure and state its cost.

For **algorithms**, the shared route starts with exhaustive enumeration or the simplest complete baseline, identifies redundant computation, and derives the minimum structure that removes it. For **data structures**, it begins with primitive storage and derives a new representation from expensive operations. For **mathematics and physics**, it names the obstruction or insufficiency before introducing the concept that resolves it. These are domain realizations of the same epistemology, not separate ambient rules.

## Mechanisms

| Mechanism               | Activation                                            | Primary role                                                       | Enforcement               |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------ | ------------------------- |
| Rules                   | Loaded from the applicable user or repository scope   | Declare unconditional epistemology or local ambient context        | Interpreted by the agent  |
| Skills                  | Discovered by metadata and loaded when a task matches | Package reusable workflows, domain taste, expertise, and resources | Interpreted by the agent  |
| Human docs or decisions | Retrieved when their question or rationale matters    | Preserve motivation, public theory, and durable rationale          | Interpreted by the reader |
| Hooks, tests, or CI     | Triggered by a defined event                          | Observe, automate, or block mechanically testable behavior         | Executed by tooling       |
| Generators              | Invoked explicitly                                    | Materialize repeated deterministic structure                       | Executed by tooling       |

These mechanisms differ by activation and enforcement rather than importance. A generator is not a policy owner: its output must still belong to a user, repository, skill, decision, or mechanical boundary.

## Navigation

- The [development routing model](development.md) routes contract, planning, durable-work, and execution uncertainty.
- The [organization roadmap](roadmap.md) tracks changes that coordinate more than one semantic owner or activation mechanism.

The retired [`copier-coding-harness`](https://github.com/agentic-tend/copier-coding-harness) remains historical. [`bootstrap-project-context`](https://github.com/agentic-tend/skills/tree/main/bootstrap-project-context) replaces its generic repository scaffold with inspection, pressure testing, and the minimum sufficient local result.

## Evaluation

Evaluate observable outcomes rather than file presence. Compare representative tasks before and after a context change against an explicit oracle, and attribute the result to the mechanism under test.

Use model compliance for semantic judgment and hooks or CI for conditions that are mechanically observable. Add enforcement only after repeated misses justify its maintenance and false-positive cost.

The [Tessl documentation](https://docs.tessl.io/) is a practical reference for reviewing agent context and using [scenario evaluations](https://docs.tessl.io/improving-your-skills/evaluate-skill-quality-using-scenarios) to test whether a skill changes output. It is a reference, not a project dependency or adopted benchmark.

[^bitter-lesson]: Richard Sutton, [*The Bitter Lesson*](http://www.incompleteideas.net/IncIdeas/BitterLesson.html).
