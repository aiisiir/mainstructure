# Architecture Standard

## Required outputs
- Context diagram and system boundaries.
- Key components/responsibilities and data flows.
- Trust boundaries and authorization model.
- Data ownership, retention, backup, restore, and migration strategy.
- External integrations, timeouts, retries, idempotency, and failure behavior.
- Deployment topology and operational ownership.
- Quality-attribute decisions (security, latency, availability, maintainability, accessibility, SEO as relevant).
- Decisions, alternatives, trade-offs, and reversibility.

## Rules
- Prefer the least complex architecture that satisfies evidenced requirements and plausible near-term growth.
- Separate domain logic from transport, presentation, storage, and vendor-specific integrations where it improves changeability.
- Do not adopt microservices, event sourcing, CQRS, Kubernetes, or a framework merely because they are popular. State the concrete need and operational cost.
- Identify single points of failure and data consistency rules.
- Define authorization at the server or trusted service boundary; UI visibility is not authorization.
- For public web projects, rendering and URL architecture must be an explicit decision; see `core/seo-and-discoverability.md`.
- Design migrations and rollbacks before irreversible schema/data changes.

## Architecture fitness checks
Automate checks for dependency direction, forbidden imports, contract compatibility, configuration validity, and critical security invariants where practical. Human review covers context and trade-offs.
