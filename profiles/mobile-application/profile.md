# Profile: Mobile Application

## Required design decisions
- Target platforms, minimum OS versions, distribution channels, signing and release ownership.
- Native versus cross-platform choice and the evidence behind it.
- Offline behavior, synchronization/conflict rules, cache and local data protection.
- Authentication/session lifecycle, deep links, permissions, device capabilities, and notification consent.
- Accessibility, localization, supported screen sizes, and performance budgets.
- API compatibility, telemetry/privacy, crash reporting, staged rollout, rollback/kill switch, and support.

## Security and privacy
Minimize sensitive local data, protect secrets using platform facilities, avoid embedding privileged credentials, define logout/revocation behavior, and assess rooted/jailbroken-device assumptions in proportion to risk. Do not treat client-side checks as the only authorization control.

## Discoverability
SEO may not apply to private app screens. Assess app-store listing metadata, deep-link behavior, web landing pages, and public content discoverability separately.

## Quality checks
Automated unit/integration tests, critical journey device tests, supported OS/device matrix, accessibility, offline and recovery scenarios, secure storage, release signing, and staged rollout verification.
