# Profile: Data Platform

## Required design decisions
- Data sources, owners, lineage, freshness, volume, quality expectations, and consumers.
- Batch/streaming needs, scheduling, backfills, late/duplicate events, schema evolution, and idempotency.
- Data classification, access controls, encryption, retention, deletion propagation, and safe development datasets.
- Data contracts, validation rules, quarantine/dead-letter behavior, recovery/replay, and reconciliation.
- Cost controls, observability, dataset SLAs, and incident ownership.

## Quality checks
Schema checks, freshness/completeness/uniqueness/validity checks, lineage review, reproducibility, backfill and recovery tests, access/privacy review, cost guardrails, and data deletion/retention validation.

## Discoverability
Search-engine SEO is typically not applicable to private datasets. Assess internal catalog/search discoverability, access policy, dataset metadata, and documentation instead.
