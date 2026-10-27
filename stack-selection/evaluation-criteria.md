# Stack Evaluation Criteria

## Hard constraints (pass/fail first)
- Required platform/device/browser support.
- Hosting, data residency, network, and deployment constraints.
- Required integrations, protocols, and interoperability.
- Team skill and realistic learning time.
- Delivery deadline and available budget.
- Security, privacy, licensing, and contractual constraints.
- SEO/crawl/render requirements for public surfaces.
- Existing systems/data that must be reused or migrated.

A candidate failing a true hard constraint is eliminated unless the constraint itself is formally revisited.

## Suggested weighted criteria
Score surviving candidates 1–5 and provide evidence. Start with these weights, but adjust before scoring when project needs justify it; weights must total 100.

| Criterion | Starter weight | What to examine |
|---|---:|---|
| Fit to functional/workload requirements | 15 | Data shapes, workflows, integrations, concurrency |
| Security and maintainability | 15 | Patch cadence, ecosystem health, secure defaults, testability |
| Delivery fit and team capability | 12 | Learning curve, hiring/skills, prototyping evidence |
| Operational simplicity and reliability | 12 | Deploy, monitor, backup, recovery, support burden |
| Performance and scalability fit | 10 | Evidence from relevant workloads, not generic benchmarks |
| SEO/rendering/discoverability | 10 | Only score according to real public web requirements; redistribute if inapplicable |
| Total cost of ownership | 10 | Build, run, licensing, maintenance, migration, exit cost |
| Ecosystem maturity and integrations | 6 | Support, packages, compatibility, community/maintainer risk |
| Portability and lock-in | 5 | Data export, standard protocols, replaceability |
| Accessibility/tooling/quality automation | 5 | Automated tests, linting, observability, accessible UI support |

Weighted score = sum(weight × score) / sum(weights), optionally normalized to 100. Do not use a numeric total to hide a critical weakness. Include confidence (low/medium/high) for each score and links/evidence for uncertain claims.
