# Quality and Reliability Standard

Quality is judged across correctness, usability, accessibility, performance, security, maintainability, compatibility, observability, and operational resilience.

Define budgets only after understanding users and constraints. Avoid arbitrary numbers without a measurement plan. Where targets are needed, name the metric, measurement method, percentile/window, environment, and owner.

Every production service should have proportionate health checks, useful structured logs, actionable alerts, error tracking, deployment visibility, and an owner. Do not add noisy monitoring that nobody operates.

Define expected failure modes for dependencies: timeout, bounded retry with backoff, idempotency where retry can duplicate effects, circuit breaking only where justified, graceful degradation, and clear user-facing errors.

Reliability planning includes backup frequency, recovery point objective (RPO), recovery time objective (RTO), restore rehearsal, rollback strategy, and escalation responsibility. “We have backups” is insufficient without evidence of restoration.
