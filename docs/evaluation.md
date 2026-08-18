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

[^scenario-evaluations]: The [Tessl documentation](https://docs.tessl.io/) describes [scenario evaluations](https://docs.tessl.io/improving-your-skills/evaluate-skill-quality-using-scenarios). It is a practical reference, not a project dependency or adopted benchmark.
