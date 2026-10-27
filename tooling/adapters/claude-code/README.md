# Claude Code Adapter

The repository root `CLAUDE.md` is the instruction entry point. Canonical task skills live under `skills/<skill-name>/SKILL.md`. When using Claude Code, copy the relevant skill folders into the product repository's `.claude/skills/` folder if the client requires that location. Treat the copies as derived files: the canonical source remains this framework repository. No synchronization script is required or included.

## Optional integrations

- **Superpowers:** optional structured workflows for brainstorming, planning, implementation, TDD, debugging and review. Install only through its current official instructions, and keep this framework's quality gates authoritative.
- **Context7:** optional version-sensitive library/API documentation retrieval. Verify package and version against primary documentation; it does not replace tests or architecture decisions.

Do not assume these integrations are installed, enabled, or available in every environment.
