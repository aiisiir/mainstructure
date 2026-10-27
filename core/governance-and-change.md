# Governance and Framework Change

## Change types
- **Core change:** affects all products; requires a strong general rationale and impact analysis.
- **Profile change:** affects a project category.
- **Adapter change:** affects a tool/platform integration.
- **Product-specific decision:** intentionally applies to one product only.

## Review criteria
Every non-trivial change must state the problem, evidence, proposal, alternatives, affected files/versions, risks, migration path, and how success will be evaluated.

## Promote a pattern carefully
A solution discovered in one product does not automatically become a core rule. Promote it only if it is reusable across materially different products, can be explained and tested, and is not better handled in a profile.

## Impact classes for existing products
- **Informational:** no action needed.
- **Recommended:** consider adoption during planned maintenance.
- **Required/security:** assess affected products and create explicit remediation tasks.
- **Breaking:** publish migration steps and migrate products deliberately.

Products are not runtime-dependent on this repository and are not automatically updated when it changes. Each product should record the framework version it adopted and selectively apply relevant changes. Do not force every product to track the latest framework version.

## Versioning
Use semantic versioning after adoption by downstream products. Major version: incompatible requirements/schema/workflow change. Minor version: backward-compatible capability. Patch: clarification or compatible fix. Update `CHANGELOG.md` and the quality checks for structural changes.
