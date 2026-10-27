# Release Checklist — [Version/date]

Mark each item `PASS`, `FAIL`, `BLOCKED`, `N/A` (with rationale), or `NOT RUN` and attach evidence.

## Build and correctness
- [ ] Build/package succeeds in the intended environment.
- [ ] Required automated tests pass; skipped tests have documented rationale.
- [ ] Critical user journeys and failure paths are verified.
- [ ] Configuration and migrations are reviewed.

## Security and privacy
- [ ] Authorization boundaries and sensitive flows are tested.
- [ ] No secret or sensitive data leakage in code, logs, responses, or artifacts.
- [ ] Dependency/security checks are reviewed.
- [ ] Open critical risks are resolved or explicitly blocked pending authorized decision.

## Operations
- [ ] Monitoring, alerting, ownership, and runbook are ready.
- [ ] Backup/restore or rollback path has evidence.
- [ ] Migration and rollback/forward-fix procedure is understood.

## Accessibility and performance
- [ ] Applicable accessibility checks pass.
- [ ] Performance budgets and representative journeys are checked.

## SEO (for public/indexable web surfaces)
- [ ] SEO gate completed with production/staging evidence.
- [ ] Rendering, status, canonical/hreflang, robots, sitemap, redirects, content and metadata verified.
- [ ] Structured data validated if used; no fabricated claims.
- [ ] Post-release monitoring owner assigned.

## Decision
- Release owner:
- Decision: GO / NO-GO / GO WITH DOCUMENTED RISK
- Accepted risks and approver:
- Rollback trigger and owner:
