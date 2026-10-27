# Engineering Principles

1. **Problem before solution.** Define the user problem and desired outcome before selecting tools.
2. **Evidence before confidence.** Label facts, assumptions, hypotheses, and unknowns separately.
3. **Fitness for purpose.** Avoid both under-engineering and unnecessary distributed-system complexity.
4. **Explicit trade-offs.** Every material choice optimizes some qualities at the expense of others.
5. **Security and privacy by design.** Identify assets and threats before sensitive paths are implemented.
6. **Accessible by default.** Accessibility is a user requirement and quality attribute, not optional polish.
7. **SEO by architecture for public sites.** Discoverability decisions must precede route and rendering implementation.
8. **Test the risk.** Test depth follows impact and likelihood, with critical flows covered first.
9. **Automate repeatable checks.** Human judgment is retained for context-sensitive decisions.
10. **Make operations part of design.** Ownership, observability, backups, restore, rollback, and maintenance are designed before release.
11. **Small, reversible increments.** Prefer changes whose failure can be detected and rolled back cheaply.
12. **Reuse proven abstractions.** Abstract only when a recurring pattern and its variation points are understood.
13. **No invisible exceptions.** Deviations are documented with owners, impact, mitigations, and review conditions.
14. **Measure outcomes, not artifacts.** More files, prompts, tests, or architecture diagrams do not automatically mean better software.
