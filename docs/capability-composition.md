# Capability composition examples

This document shows several existing operators acting on one object. Each scenario is a derived view of current task data, not a fixed workflow, taxonomy, or additional theory owner.

## Mixed Julia behavior and prose

- **Object:** a Julia API change and the persistent prose whose public contract must remain aligned with it.
- **Pressure:** the requested behavior cannot be completed correctly unless Julia semantics, software behavior, and the affected documentation agree.
- **Traits:** software topology, host-language dispatch and return behavior, durable natural language, Markdown or Documenter realization, observable evidence, and any unresolved user-owned choice.
- **Capabilities:** `$software-engineering` owns the software contract and validation; `$julia-development` realizes Julia-specific semantics; `$structure-documentation` organizes prose after its required meaning is known; `$markdown-authoring` realizes Markdown syntax and renderer constraints. `$clarifying-contracts` enters only if inspection leaves a behavior-changing choice to the user.
- **Seams:** the public software contract and task data connect the capabilities. The software owner decides whether prose is required; the prose and artifact capabilities do not redefine the API.
- **Evidence:** focused behavioral checks test the changed public boundary, source inspection tests Julia assumptions, and the relevant documentation build or rendering checks presentation.
- **Stop:** the requested behavior and required prose express one contract, the selected evidence passes or its limits are explicit, and no material user-owned choice remains.

## Scientific referee response

- **Object:** an exact referee comment, the current manuscript, established scientific evidence, and any promised manuscript change.
- **Pressure:** the reply must answer the stated objection while keeping every scientific claim within its actual evidence and the current manuscript.
- **Traits:** response-to-reviewers delivery, claim support, possible literature attribution or landscape evidence, journal practice, durable prose, and repository-specific build instructions.
- **Capabilities:** `$referee-response` owns the reply and change map; `$scientific-claim-audit` enters only for a contested claim or validity objection; `$scientific-literature-evidence` enters only when a corpus, attribution, priority, conflict, or bounded absence question remains. `$structure-documentation` can express the established content without deciding its scientific validity.
- **Seams:** the response consumes claim and literature evidence rather than replacing their owners. The manuscript repository owns its current claims and validation instructions; the exact referee comment fixes the reply's direct object.
- **Evidence:** a claim-to-evidence check supports each substantive sentence, promised revisions appear in the current manuscript, and the repository's bounded build or rendering check validates affected artifacts.
- **Stop:** the exact objection is answered, manuscript changes are mapped and present, unsupported boundaries remain explicit, and no additional corpus or scientific judgment is needed.

In either scenario, feedback may change the pressure, traits, or capability composition. The arrow sequence `object -> pressure -> traits -> capabilities -> seams -> evidence -> stop` is only a compact projection of these examples; the [capability model](capability-model.md) owns the underlying fast loop.
