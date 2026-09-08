---
name: idea-to-execution
description: Turn a product or engineering idea into a practical implementation plan with scope, milestones, dependencies, risks, and validation.
---

# Idea to Execution

Use this skill when the user has an idea, goal, feature request, or problem statement and needs a plan that can be implemented and validated.

## Workflow

1. Restate the desired outcome and identify the target users, constraints, and success criteria.
2. Inspect the existing project and related implementation surfaces when a repository is available. Follow local conventions and reuse existing abstractions.
3. Separate the minimum viable scope from valuable follow-up work. Explicitly list what is out of scope.
4. Decompose the work into vertical, independently verifiable slices rather than only technical layers.
5. For each slice, identify the owning files or modules, behavior changes, interfaces, data changes, dependencies, and tests.
6. Resolve important ambiguities with targeted questions. If the user prefers momentum, state assumptions and continue.
7. Define rollout, observability, migration, rollback, accessibility, security, and performance considerations where relevant.
8. Define a validation strategy with concrete commands, tests, acceptance criteria, and manual checks.

## Output

Return a Markdown implementation plan with:

- **Outcome**: the user or business result this work should achieve.
- **Assumptions and constraints**
- **Scope**: in scope, out of scope, and follow-up candidates.
- **Proposed approach**: a brief explanation of the design and important tradeoffs.
- **Implementation steps**: ordered, actionable steps. Each step should name the affected file or module when known, the behavior to implement, and how it will be verified.
- **Data and API changes**: schemas, contracts, compatibility, and migration details when applicable.
- **Testing and acceptance criteria**: unit, integration, end-to-end, accessibility, and manual checks appropriate to the risk.
- **Rollout and operations**: feature flags, deployment order, monitoring, rollback, and support notes when applicable.
- **Risks and open questions**

Prefer small deliverable slices that leave the project in a working state. Do not prescribe exact files or technologies without evidence from the repository or an explicit requirement. Call out decisions that need user input instead of hiding them in the plan.

## Quality checks

Before returning the plan, verify that:

- Every step contributes to the stated outcome.
- Dependencies and ordering are explicit.
- Each behavior has a validation path.
- Edge cases and failure handling are covered.
- The plan is specific enough for implementation but avoids speculative detail.
