# Engineering Framework

**Version:** 0.1.1 · **Maturity:** initial working baseline, not yet production-validated

A technology-independent framework for discovering, designing, building, verifying, releasing, and improving software projects. It contains a stable engineering core, project-type profiles, stack-selection records, repeatable workflows, agent skills, templates, and quality gates.

The framework does **not** assume Laravel, React, a cloud provider, a database, or a specific AI coding assistant. Technology-specific decisions belong in each project's approved profile and architecture decision records (ADRs).

## Start using it

1. Copy this repository or use it as a Git template.
2. Create a separate repository for the product; do not put product code in this repository.
3. Copy the relevant templates from `templates/` into the product repository's `docs/` folder.
4. Complete discovery, feasibility, requirements, stack decision, threat model and test strategy before substantial implementation.
5. Tailor the relevant quality gates. For public websites, SEO/discoverability is an architecture-stage gate—not a post-launch add-on.
6. Keep the product's exact code, credentials, customer data and product-specific decisions in its own repository.

This framework intentionally has no mandatory local command-line tool and no Python dependency. Use its templates and procedures manually; add automation only when a real recurring need has been demonstrated and the tool is agreed.

## Repository map

- `FRAMEWORK.md`: governing contract and lifecycle.
- `CLAUDE.md`, `AGENTS.md`: instructions for AI-assisted work.
- `core/`: principles and cross-project standards.
- `workflows/`: repeatable operating procedures.
- `stack-selection/`: criteria, decision method, and project-profile schema.
- `profiles/`: project-type-specific requirements.
- `skills/`: reusable task instructions for compatible agent skill systems.
- `templates/`: project artifacts to copy into a product repository.
- `quality-gates/`: evidence-based release and phase gates.
- `tooling/`: optional integration guidance only; no custom scripts are required.

## How framework updates affect existing products

**Product repositories are not automatically upgraded when this repository changes.** The framework is a reference standard, not a runtime dependency. When a framework rule changes, classify its impact:

- `informational`: no product action required;
- `recommended`: adopt during suitable maintenance work;
- `required/security`: assess affected products and create explicit product-level tasks;
- `breaking`: document migration steps and apply them deliberately per product.

Each product pins or records the framework version it adopted. Do not bulk-update all existing products just because a newer framework version exists. Update only where the change is relevant, justified, and planned. See `core/governance-and-change.md`.

## Quality validation

The GitHub Action performs lightweight repository-structure checks and validates the JSON project-profile schema. It does not claim to prove architecture quality or product correctness. Actual product quality gates belong in each product repository and must run against its real code.

## Publish to GitHub

Create an empty repository on GitHub. After extracting this folder, run from its root:

```bash
git init
git add .
git commit -m "feat: initial engineering framework v0.1.1"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

Replace the remote URL with your repository URL. No remote repository has been created or pushed by this package. Decide whether the repository should be private or public and choose an appropriate license before public distribution.

## Versioning and governance

Changes should include rationale, impact, action required by existing products, and migration notes where relevant. The initial baseline is intentionally small enough to critique; it is not proof that the process has improved delivery outcomes.
