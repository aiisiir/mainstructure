# Quality Gate: SEO and Public Discoverability

**Applies to:** public/indexable web route families. If not applicable, record why and review internal/app-store discoverability separately.

## Architecture and rendered content
- [ ] Rendering strategy is approved per route family and recorded in an ADR.
- [ ] Representative production-equivalent URLs return expected status codes.
- [ ] Primary text, headings and important links are present and discoverable in actual HTML/rendered output without relying on a user-only state.
- [ ] Redirects, canonical destinations, and trailing-slash/case rules are consistent.

## Metadata and localization
- [ ] Unique, accurate titles; useful descriptions where appropriate; correct language attributes.
- [ ] Canonicals point to intended canonical URLs and do not collapse distinct content.
- [ ] hreflang alternates are correct, reciprocal, and only connect equivalent language versions.
- [ ] Open Graph/social metadata is valid where needed.

## Crawl/index controls
- [ ] robots.txt permits intended crawling and does not expose secrets or pretend to be access control.
- [ ] noindex/private routes behave as intended.
- [ ] Sitemap includes canonical indexable URLs only and is reachable.
- [ ] 404/410/301/308 behavior is correct; no redirect loops/chains in critical paths.
- [ ] Filters, query parameters, pagination and duplicate variants have an explicit policy.

## Content, links and structured data
- [ ] Each landing page has a useful distinct purpose and satisfies user intent.
- [ ] Important pages are connected by crawlable internal links.
- [ ] Structured data, if used, matches visible content and validates; no invented reviews/offers/facts.
- [ ] Images/media have appropriate alternatives, dimensions, loading behavior and accessible context.

## UX, speed and monitoring
- [ ] Mobile layout and keyboard/accessibility checks are completed.
- [ ] Performance budgets are measured with a documented method; real-user data plan exists where feasible.
- [ ] Search/analytics monitoring respects privacy and has an owner.
- [ ] Post-release checks include indexing/canonical issues, sitemap processing, 404s/redirects, search performance and Core Web Vitals where available.

**Evidence links:** [URL test reports, source HTML, sitemap, structured-data validation, performance reports]  
**Decision:** PASS / FAIL / BLOCKED / EXCEPTION  
**Owner and residual risk:** [ ... ]
