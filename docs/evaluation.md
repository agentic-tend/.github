# Context evaluation

Agentic Tend evaluates persistent context as an intervention against representative work rather than treating file presence or structural conformance as success.

## Define the observable outcome

State the intended task distribution, success condition, and stopping evidence before inspecting outputs. Generated structure and smaller diffs matter only when they improve an observable contract or remove a demonstrated cost.

## Compare the smallest candidate

- Form a working hypothesis and compare the smallest context candidate with a baseline using the cheapest evidence that distinguishes the live alternatives.
- Use model or human judgment for semantic outcomes and executable checks for mechanical conditions; calibrate automated proxies against human judgment.
- Preserve enough evidence to distinguish a wrong implementation from an invalid check, environment drift, or noise, then retain confirmed failures as regression cases.
- Distill a new instruction or add enforcement only after repeated misses justify its maintenance and no material regression appears on adjacent tasks.

Scenario evaluations are one practical implementation of this method.[^scenario-evaluations]

## Compare evidence separation

Evaluate the observable effective boundary rather than hidden micro-orchestration. A successful multi-agent intervention presents its plan before delegation, activates only ports with a stated evidence motivation, preserves intended information boundaries, and returns a provenance-aware delivery without inventing an approval gate.

Compare it with both a single-agent baseline and naive agents that share the same narrative. Include negative controls where task size, importance, or latency-only parallelism must not activate evidence separation. Include positive cases where prior evidence remains independent of implementation, a task without a legitimate mechanical oracle does not fabricate one, and posterior review grows only when a failure hypothesis justifies another layer.

Inspect available port inputs and outputs to distinguish genuine information separation from fresh contexts that repeat the same method. Check whether disagreement, common-mode specification failure, unvalidated claims, and unavailable raw evidence remain visible rather than being hidden by agreement or a polished summary. The useful outcome is not agent count or agreement rate, but whether separation exposes a plausible failure and lowers the human effort needed to locate judgment-changing distinctions.

[^scenario-evaluations]: The [Tessl documentation](https://docs.tessl.io/) describes [scenario evaluations](https://docs.tessl.io/improving-your-skills/evaluate-skill-quality-using-scenarios). It is a practical reference, not a project dependency or adopted benchmark.
