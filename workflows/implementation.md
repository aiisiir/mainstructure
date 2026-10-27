# Workflow: Implementation

1. Select a small requirement or vertical slice with explicit acceptance criteria.
2. Inspect the affected code, tests, conventions, and ADRs.
3. State intended change, likely risks, and verification plan.
4. Implement the smallest coherent change. Add regression tests for changed behavior and relevant failure paths.
5. Run targeted tests, format/lint/type checks, then broader checks when appropriate.
6. Review auth boundaries, error handling, data leakage, performance, accessibility, and SEO implications based on the change.
7. Inspect the diff and update requirements/docs/ADRs if behavior or decisions changed.
8. Report what changed, what was tested, what was not tested, and any remaining risk.

Never claim a tool, test, deployment, documentation lookup, or review occurred if it did not.
