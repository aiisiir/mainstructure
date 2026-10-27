# Workflow: Code Review

Review in this order:
1. Correctness against requirement and acceptance criteria.
2. Security, authorization, data isolation, validation, secrets, privacy, and abuse cases.
3. Data integrity, transactions, idempotency, concurrency, migrations, and recovery.
4. Error paths, observability, performance, and resource use.
5. Accessibility, UX, compatibility, and SEO effects where relevant.
6. Maintainability, dependency direction, complexity, naming, and duplication.
7. Test quality and documentation/traceability.

For each finding, include severity, location, consequence, and a practical fix. Separate blockers from suggestions. Do not report speculative style preferences as defects.
