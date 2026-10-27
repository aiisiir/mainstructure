# Framework Contract

## 1. Mission

Provide a repeatable, auditable process for producing fit-for-purpose software while allowing each project to select its own technologies and delivery approach.

## 2. Scope

The framework governs project discovery, feasibility, requirements, architecture, stack selection, implementation workflow, security, quality, testing, SEO/discoverability, release, maintenance, and continuous improvement. It does not replace domain expertise, legal advice, product ownership, or operational responsibility.

## 3. Normative language

- **MUST**: required unless an approved, documented exception exists.
- **SHOULD**: expected unless a rationale supports another choice.
- **MAY**: optional.
- Every exception must name an owner, rationale, risk, mitigation, and review/expiry condition where relevant.

## 4. Required project artifacts

Before meaningful implementation, each project MUST have:
1. Project brief and named decision owner.
2. Goals, non-goals, users, constraints, and measurable success criteria.
3. Requirements with priorities and acceptance criteria.
4. Risk/feasibility review and unresolved-assumptions register.
5. Project profile describing workload, deployment, data sensitivity, accessibility, and SEO/discoverability needs.
6. Stack-selection record and architecture decisions for material choices.
7. Initial security/threat model proportionate to risk.
8. Test strategy and applicable quality gates.
9. A delivery plan with milestones and explicit release criteria.

For a low-risk prototype, artifacts may be concise, but omitted artifacts and the reason must be recorded. “Small project” is not by itself a valid rationale for ignoring security, backups, or data loss risk.

## 5. Project lifecycle

1. Discover the problem.
2. Assess feasibility and risk.
3. Specify requirements and acceptance criteria.
4. Choose project profile, architecture, and stack based on evidence.
5. Plan vertical slices and quality evidence.
6. Implement in small reviewable increments.
7. Verify functionality, security, accessibility, performance, and discoverability as applicable.
8. Release with rollback/restore arrangements.
9. Observe real outcomes and feed lessons into the project and framework.

A phase is not complete because a document exists. Its required decisions and evidence must be reviewed.

## 6. Technology independence

The core expresses outcomes and engineering constraints, not framework-specific recipes. Profiles and adapters may define technical implementation details. Every technology-specific recommendation must be located in a profile, adapter, or project decision—not silently embedded in core rules.

## 7. Stack selection

The chosen stack MUST satisfy hard constraints first (platform, skills, hosting, compliance, interoperability, budget, deadline). Remaining candidates are compared with explicit weighted criteria. Scores guide discussion; they do not replace judgment. Include operational ownership, migration cost, ecosystem maturity, security maintenance, vendor lock-in, and total cost of ownership.

## 8. Security and data protection

Security and privacy are designed from the beginning. Define trust boundaries, assets, actors, authorization, secrets handling, logging boundaries, retention, backups, recovery, and incident responsibilities. Apply least privilege and deny-by-default access. Never log credentials, OTPs, session tokens, full sensitive payloads, or other secrets.

## 9. SEO and public discoverability

For any public, indexable web surface, SEO/discoverability is a first-class architecture concern. The team MUST decide rendering and crawl strategy before implementation, define canonical URLs and language/locale behavior, ensure important content is available to crawlers, provide appropriate metadata and sitemaps, and test indexability/performance before release. Do not equate “uses React” or “has a sitemap” with being search-ready. See `core/seo-and-discoverability.md` and `quality-gates/seo-gate.md`.

For non-public systems, document that public SEO does not apply and still assess accessibility, internal search, link previews, or app-store discoverability as relevant.

## 10. Quality evidence

Quality gates are risk-based but never ceremonial. Critical requirements require tests or explicit manual verification. A release MUST NOT proceed with unresolved critical security defects, unbounded data-loss risk, broken core user journeys, or a failed mandatory SEO gate for an SEO-critical site without explicit accountable risk acceptance.

## 11. AI-assisted development

AI output is untrusted until reviewed and tested. The agent must inspect repository conventions, avoid inventing dependencies/APIs, cite or link to verified documentation for version-sensitive choices, minimize unrelated edits, and report actual commands/results honestly. Humans retain responsibility for product, security, legal, and release decisions.

## 12. Framework evolution

The reference project can reveal gaps, but a project-specific need does not automatically become a core rule. Promote a pattern only when it is broadly reusable, explainable, testable, and not better handled by a profile. Record breaking changes and migration paths.
