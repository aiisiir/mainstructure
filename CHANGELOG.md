# Changelog

## 0.1.1 - Removed unapproved Python tooling and separated product repositories

- Removed Python scripts and Python installation as a prerequisite.
- Removed the Iran Build Expo project-specific materials from the technology-independent framework repository; Expo now has its own repository.
- Replaced the Python validator workflow with lightweight shell/Node-based repository checks in GitHub Actions.
- Clarified that existing products do not automatically depend on or upgrade with this framework.
- Updated the contribution, skill-adapter and usage instructions.

## 0.1.0 - Initial baseline

- Added technology-independent framework contract and lifecycle.
- Added stack selection method and project profile schema.
- Added web, mobile, API, and data-platform profiles.
- Added SEO/discoverability requirements and an explicit SEO quality gate.
- Added workflows, reusable agent skills, templates, and quality gates.

## Release policy

Use semantic versioning once the framework has downstream products. Breaking changes to required artifacts, profile schema, or quality gates require migration notes.
