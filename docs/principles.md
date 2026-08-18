# Agentic Tend principles

Agentic Tend preserves objectives and preferences that general model capability cannot reliably infer, while leaving learnable intelligence and contract-equivalent taste to the agent.

## Why preserve context

Richard Sutton's *The Bitter Lesson*[^bitter-lesson] argues that scalable learning and search ultimately outperform attempts to hand-code human domain knowledge into intelligent systems.

Agentic Tend derives a tooling maxim from that lesson:

> Do not encode intelligence that can be learned; encode objectives and preferences that cannot be inferred.

It does not imply deleting every `AGENTS.md` or skill as models improve. Cross-domain interaction contracts, user-specific taste, authority boundaries, local facts, and public contracts remain justified when stronger general capability still cannot infer them.

`Tend` means caring for a growing system: let useful instances expose pressure, introduce only the structure that pressure requires, and preserve the distinctions needed for later judgment.

## Pressure before structure

The governing sequence is:

> observed need -> minimal persistent structure

Minimal means minimum sufficient and lossless, not the fewest files or shortest prose. Apply the same counterfactual discipline to addition and subtraction: persist a distinction only when its absence would change future judgment, move it when its owner or activation boundary is wrong, and compress or delete it only when meaning, rationale, and sources remain recoverable. The [context ownership model](context-ownership.md) owns the operational tests for each migration action.

Generated structure and smaller diffs are evidence only when they improve an observable contract or remove a demonstrated cost.

## Intellectual influences

Agentic Tend's documented taste draws from several compatible but non-identical traditions:

- Yang Chen-Ning's preference for plain, substantial work, summarized by "宁拙毋巧, 宁朴毋华", supports derivation and robustness over display or tricks. His permeative learning also motivates gradual immersion: continue through partial understanding while increasingly constraining observations connect points into a whole.[^yang-style]
- Grothendieck's rising-sea image describes problems becoming natural as a surrounding conceptual world develops.[^rising-sea] Agentic Tend inherits the preference for structural derivation and gradual immersion, but not unconditional generalization: a larger theory must still answer concrete pressure and state its cost.

<details>
<summary>Examples across domains</summary>

- For **algorithms**, the shared route starts with exhaustive enumeration or the simplest complete baseline, identifies redundant computation, and derives the minimum structure that removes it.
- For **data structures**, it begins with primitive storage and derives a new representation from expensive operations.
- For **mathematics and physics**, it names the obstruction or insufficiency before introducing the concept that resolves it.

These examples illustrate one taste; they do not define an exhaustive task taxonomy or a required internal reasoning procedure.
</details>

[^bitter-lesson]: Richard Sutton, [*The Bitter Lesson*](http://www.incompleteideas.net/IncIdeas/BitterLesson.html).
[^yang-style]: Tsinghua documents Yang's [permeative learning](https://www.tsinghua.edu.cn/info/3225/121939.htm) and [plain research style](https://www.tsinghua.edu.cn/info/3225/121987.htm).
[^rising-sea]: McLarty's [*The Rising Sea*](https://ncatlab.org/nlab/files/McLartyRisingSea.pdf) documents Grothendieck's method.
