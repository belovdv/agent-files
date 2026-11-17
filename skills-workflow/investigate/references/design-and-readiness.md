# Design evaluation and readiness

Recover the proposal's goals, current decisions, and constraints before critiquing it. Distinguish unresolved choices from requirements already settled by the user. Evaluate the proposal they actually made, including less familiar mechanisms or ownership boundaries.

Compare required behavior against available interfaces, implementations, tests, inputs, and dependencies. Verify the relevant branch/revision rather than assuming the default branch represents current work. Separate evidence of implementation from a document's claim that a capability exists.

Inspect interactions: data ownership, invariants, failure behavior, compatibility, and boundaries between generic libraries and consumers. Consider whether complexity solves a present requirement or only an imagined future need. Review naming and local details after consequential design issues.

Classify findings by their effect on the decision:
- Blocker: prevents the required outcome or invalidates a core assumption.
- Uncertainty: needs evidence before committing to a choice.
- Improvement: useful but not required to start.
- Optional polish: can wait without changing feasibility.

For each consequential finding, give the requirement, evidence, impact, and a practical resolution or smallest discriminating experiment. Do not prescribe a redesign when a narrow clarification suffices.

Deliver a readiness assessment with dependencies, unresolved decisions, and a sensible next step. Distinguish missing implementation from missing design. If continued work becomes collaborative design rather than assessment, use the planning workflow; an assessment does not authorize implementing recommendations.

Methodological basis: [Google's code-review guidance](https://google.github.io/eng-practices/review/reviewer/looking-for.html) emphasizes overall design, integration, functionality, and unnecessary complexity. Apply these principles to the relevant proposal rather than mechanically applying every code-review check.
