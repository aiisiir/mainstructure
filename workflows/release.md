# Workflow: Release

1. Confirm release scope, version, owner, and known limitations.
2. Verify build, tests, static analysis, dependency/security checks, configuration, and migration plan.
3. Confirm secrets and environment configuration are managed safely.
4. Verify backup/restore or rollback for changes that can affect data or availability.
5. Run end-to-end smoke tests for critical user journeys.
6. For public websites, complete `quality-gates/seo-gate.md`, including production URL checks, robots/sitemap, canonical/language alternates, redirects, rendered content, and performance.
7. Review open defects and obtain explicit risk acceptance for any permitted residual risk.
8. Deploy with a rollback/mitigation plan and monitor pre-agreed signals.
9. Record outcome, incidents, and follow-up work.

**Abort/rollback** if a critical journey fails, data integrity is at risk, a critical security defect appears, or a mandatory indexability/redirect failure materially harms an SEO-critical release.
