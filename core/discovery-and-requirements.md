# Discovery and Requirements Standard

## Discovery questions
- Who has the problem, and how is it handled today?
- What measurable outcome changes if the project succeeds?
- Who owns product decisions, content, data, operations, and release approval?
- What is explicitly out of scope for this release?
- What legal, contractual, platform, hosting, language, accessibility, budget, and deadline constraints exist?
- Which assumptions are most likely to invalidate the plan?
- Is the product public and discoverable, authenticated/private, internal-only, or hybrid?

## Requirement quality
A requirement should be atomic, unambiguous, testable, prioritized, and traceable to a stakeholder or rationale. Distinguish:
- **Functional:** behavior the system provides.
- **Quality attribute:** security, performance, accessibility, availability, maintainability, privacy, scalability, and discoverability.
- **Constraint:** a boundary the design must obey.
- **Business rule:** domain logic that must remain consistent.

Avoid requirements such as “fast,” “secure,” “SEO-friendly,” or “user-friendly” without a measurable or reviewable criterion.

## Acceptance criteria
Use observable examples and edge cases. Include permission-denied, invalid-input, empty-state, failure, concurrency, and recovery cases where relevant. For public web pages, criteria can include response status, rendered primary content, canonical URL, language alternates, robots directives, schema validity, performance budget, and accessibility checks.

## Traceability
Maintain links from requirement → design/decision → implementation work → test/evidence → release. Do not force artificial one-to-one mapping; record meaningful coverage and gaps.

## Scope control
Every change to scope must include impact on value, cost, timeline, risks, migrations, tests, content, and SEO/URL behavior where relevant. Redirect requirements are part of a URL-changing migration, not optional post-release work.
