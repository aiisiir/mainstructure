# Profile: Web Application

Use for websites and browser-based applications. Tailor the SEO section based on whether any route is public and indexable.

## Required design decisions
- Route families and access: public/indexable, public/noindex, authenticated, administrative, API.
- Rendering per public route family: SSR, SSG, ISR, prerender, CSR, or hybrid; evidence and trade-offs are recorded in an ADR.
- URL structure, language/locale, canonical, redirects, cache behavior, and content lifecycle.
- Authentication/session model, CSRF strategy where relevant, authorization boundary, and tenant isolation if multi-tenant.
- API error contract, input validation, rate limits, idempotency for sensitive actions, and data consistency rules.
- Responsive behavior, accessibility target, browser support, and performance budgets.
- Deployment environments, environment config, asset caching, monitoring, backups, rollback, and migration approach.

## SEO requirements for public sites
Follow `core/seo-and-discoverability.md` and `quality-gates/seo-gate.md`. An approved rendering decision is required before building SEO-critical public route families. Ensure important links and content are crawlable in actual output, not just in client state. Add redirect coverage to URL-changing work.

## Security checkpoints
Test server-side authorization for every protected operation; do not trust route guards or hidden UI controls. For multi-tenant data, test cross-tenant reads/writes and exports. Check CSP and other security headers in context rather than copying a policy blindly.

## Quality checks
Build, tests, lint/type checks, critical journey E2E, accessibility checks, mobile/performance checks, dependency/security review, API contract checks, and SEO gate as applicable.
