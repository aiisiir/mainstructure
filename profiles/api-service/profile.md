# Profile: API Service

## Required design decisions
- Consumers, trust boundaries, authentication, authorization, and API versioning policy.
- Contract format, error schema, pagination, filtering, idempotency, rate limits, timeouts, retries, and consistency guarantees.
- Data ownership, schema migrations, retention, audit needs, and backup/restore.
- Availability/latency goals, capacity assumptions, observability, alerting, and incident ownership.
- Compatibility, deprecation, integration tests, and consumer contract tests.

## Security
Validate every input at the boundary, authorize every operation and object access, prevent mass assignment/over-posting, constrain query/resource cost, protect secrets, and avoid exposing internals in errors. Authentication is not authorization.

## Discoverability
Public APIs generally need developer documentation and perhaps an API catalog more than search-engine indexing of raw endpoints. Decide whether docs, product pages, or schema pages are intended to be indexed. Keep private APIs out of public catalogs.

## Quality checks
Schema/contract validation, authorization matrix tests, rate-limit/abuse tests, integration tests, compatibility checks, migration/restore tests, dependency review, and latency/error SLO checks.
