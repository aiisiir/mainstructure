# Project Lifecycle and Phase Gates

## Phase 0 — Intake
**Inputs:** request, sponsor, known deadlines and constraints.  
**Outputs:** one-page brief, owner, initial unknowns.  
**Exit:** the problem and decision authority are clear enough to investigate.

## Phase 1 — Discovery
Identify users, jobs-to-be-done, current alternatives, business rules, success metrics, non-goals, user journeys, and evidence for demand. For public web projects, identify search intent, audiences, language/locale needs, public versus private routes, content ownership, and conversion goals.

## Phase 2 — Feasibility and risk
Assess technical feasibility, operating model, total cost, timeline, skills, data migration, compliance, vendor dependencies, security, and SEO constraints. Build a risk register. Run spikes only where a result can change a decision.

## Phase 3 — Specification
Create prioritized functional and non-functional requirements. Each high-priority requirement has observable acceptance criteria. Resolve contradictions and flag unresolved questions. Map requirements to tests or verification methods.

## Phase 4 — Architecture and stack
Choose the project profile; compare viable stacks against hard constraints and weighted criteria. Define boundaries, deployment, data ownership, failure behavior, security controls, observability, SEO rendering/crawl strategy, and migration/rollback. Record material decisions in ADRs.

## Phase 5 — Delivery plan
Break work into demonstrable vertical slices. Sequence risky integrations early. Include test automation, content/model setup, performance budget, security work, SEO validation, deployment readiness, and documentation as delivery tasks—not end-of-project cleanup.

## Phase 6 — Build
Use small changes; tests should fail for the intended reason before the fix where feasible. Code review checks correctness, security, maintainability, observability, accessibility, and applicable SEO effects.

## Phase 7 — Release readiness
Run applicable quality gates, migration rehearsal, backup/restore or rollback checks, critical user journeys, security review, and SEO checks. Explicitly accept only residual risks within the named decision owner's authority.

## Phase 8 — Operate and learn
Monitor user and system outcomes, errors, latency, cost, search/indexation signals where relevant, support issues, and security events. Create follow-up work and review whether the project met its original success criteria.

## Stop-the-line conditions
Pause implementation or release when the product goal is materially unclear, a critical assumption remains untested, data access boundaries are unsafe, a destructive migration has no credible recovery path, or an SEO-critical public site has an unresolved rendering/indexability blocker.
