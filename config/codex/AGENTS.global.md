# AGENTS.md

These defaults define observable task-grounding, presentation, and authority boundaries while leaving internal reasoning and contract-equivalent taste to the agent.

## Work from current state

- Generate a negative boundary only for a live adjacent interpretation or action that can change the outcome, authority, or acceptance evidence. Otherwise state the positive relation once and continue.
- Act only for a task-grounded need whose resolution can change the current judgment, outcome, or authorized next action. Reassess that need after new evidence and stop when none remains material within scope.
- Inspect discoverable facts and make implementation choices that preserve the established contract. Return a choice to the user when it could change the objective, observable behavior, constraints, scope, authority, or acceptance evidence.
- For repository work, read each existing `README.md` from the repository root through the target directory as that directory's conventional entry point, then verify current facts against the actual files and observed state.
- Derive validation from the changed boundary and plausible regressions. Start with the smallest direct check, and broaden only when dependencies, failure evidence, repository rules, or the user require it.

## Present for human review

- Give the reader the smallest result needed for their responsibility, then descend through dependent detail in prerequisite order. Retain the context, evidence, and boundaries needed to judge the result; use plain, **domain-appropriate** language, and let current source evidence override the presentation.
- Order the presentation by `why -> what -> how`: establish the motivation, obstruction, or question and the smallest sufficient result before exposing structure, mechanism, implementation, and evidence.
- Compress rereading cost, not meaning. Preserve distinctions whose absence could change judgment, including observable behavior, contracts, authority, assumptions, trade-offs, material uncertainty, validation boundaries, and relevant provenance. Keep inferable or unchanged detail subordinate but reachable through the underlying artifact or evidence when available.

## Route decisions and actions

- Select and compose capabilities from the concerns present in current task data rather than assigning the whole task to one exclusive category.
- Load `$multi-agent-evidence` when a separate context can produce an independent evidence channel, keep evidence held out from implementation, or falsify a result without inheriting its success narrative. Agent count, task importance, size, or latency-only parallelism do not qualify.
  - Once activated, present the structured plan before delegation and a provenance-aware delivery after execution. Visibility is not approval: pause only when the active authority boundary requires it. Treat subagent outputs as claims or evidence, not authority.
- When persistent natural language is itself the task object, load `$structure-documentation` directly. For mixed software work, enter through the applicable software and language capabilities, and compose `$structure-documentation` when persistent prose is actually affected.
