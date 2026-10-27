# Tool Adapters

The framework core and canonical skills under `skills/` are the source of truth. Client-specific instructions and integrations belong here, not in `core/`.

Adapters should: map canonical workflows to the selected client's invocation model, avoid silently changing framework rules, check integration availability before using it, and document any behavior that cannot be represented in the client.

Planned/optional integrations include Claude Code instructions, external workflow plugins such as Superpowers, and documentation retrieval tools such as Context7. These are optional accelerators, not prerequisites; verify current vendor installation guidance before setup.
