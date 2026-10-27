# Working Instructions for Claude Code

## At the start of a task
1. Read `README.md` and `FRAMEWORK.md` if not already present in context.
2. Read the active project's `project-profile.md`, relevant requirements, and relevant quality gates.
3. Identify the task's acceptance criteria, risk, expected files, and verification commands before changing code.
4. Check repository status and existing conventions before modifying files.

## Engineering rules
- Do not assume a technology stack. Follow the approved project profile and ADRs; flag conflicts instead of silently overriding them.
- Do not invent requirements, API behavior, dependency versions, test results, credentials, or deployment facts.
- Prefer small, reversible changes and tests that prove the intended behavior.
- For material architectural decisions, create/update an ADR with context, options, trade-offs, decision, and consequences.
- Use least privilege, server-side authorization, input validation, safe error handling, secret hygiene, and privacy-conscious logging.
- Never claim a command passed unless you executed it and observed the result. State unrun checks explicitly.
- Do not add a dependency without checking that it is necessary, maintained, compatible, and allowed by project constraints.
- Use current primary documentation for version-sensitive APIs and configuration. Context7 may be used when available; verify its availability and the actual library/version rather than assuming setup succeeded.

## SEO-critical web projects
- Read `core/seo-and-discoverability.md`, the web profile, the project SEO requirements, and `quality-gates/seo-gate.md` before choosing or changing frontend rendering, routes, metadata, or content delivery.
- Do not assume a client-rendered SPA is sufficient for SEO-critical public pages.
- Decide SSR/SSG/ISR/prerender/CSR per route family based on content freshness, personalization, crawl requirements, hosting, complexity, and measured performance. Record the decision in an ADR.
- Verify source HTML or rendered HTML, status codes, canonical URLs, language alternates, robots directives, internal links, sitemap/robots behavior, structured data where justified, mobile usability, and Core Web Vitals.
- Do not promise search rankings. Optimize technical accessibility and content quality; ranking depends on factors outside the codebase.

## Before finishing
- Run relevant tests, linters, type checks, and validators available in the repository.
- Inspect the diff for unrelated changes, secrets, accidental data exposure, and missing tests.
- Update documentation and traceability when behavior or requirements change.
- Report: summary, changed files, verification actually run, known gaps, and next decision required.
