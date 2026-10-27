# Operations and Observability

Before production, identify service owner, support path, deployment method, environment configuration, secret management, monitoring, alert thresholds, incident process, backup policy, recovery objectives, and rollback strategy.

Telemetry should help answer: what failed, who was affected, since when, how severe it is, and what action is appropriate. Use correlation/request identifiers where useful, while avoiding secrets and unnecessary personal data.

Define health/readiness checks with care; a deep dependency check that causes cascading failures may be worse than a shallow check. Test the operational procedure, not only the application code.

Release notes should include migrations, configuration changes, feature flags, rollback caveats, and monitoring expectations.
