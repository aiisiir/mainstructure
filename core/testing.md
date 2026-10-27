# Testing Standard

Choose tests according to risk and cost:
- Unit tests for deterministic business rules and edge cases.
- Component/module tests for meaningful boundaries.
- Integration tests for persistence, messaging, third-party interfaces, and transactions.
- Contract tests for independently deployed or externally owned APIs.
- End-to-end tests for a small set of critical user journeys.
- Security, accessibility, performance, migration, and recovery tests where the risk profile requires them.

Do not maximize test count as a proxy for confidence. Tests should assert meaningful behavior, fail when regressions occur, be deterministic where practical, and be maintained with production code.

For critical workflows, test authorization failure, malformed input, duplicates/retries, concurrency, downstream failure, and recovery—not just the happy path.

For public websites, add tests for route status, rendered primary content, title/description, canonical and hreflang behavior, robots rules, sitemap membership, structured data, internal links, and performance budgets where applicable.

A skipped test must have a reason and risk owner. Test output must be reported accurately; never represent static inspection as an executed test.
