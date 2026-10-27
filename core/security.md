# Security Standard

Apply a risk-based threat-modeling process and current recognized guidance appropriate to the technology. Do not claim compliance with a standard unless scope and evidence support the claim.

## Minimum expectations
- Identify assets, trust boundaries, threat actors, abuse cases, and security objectives.
- Authenticate where identity is required; authorize every protected operation server-side.
- Apply least privilege and default-deny access, including object/tenant-level isolation.
- Validate input at trust boundaries; use context-appropriate output encoding and safe query APIs.
- Protect sessions, CSRF-sensitive actions, password/OTP flows, secrets, and rate-limited endpoints.
- Use maintained dependencies, inspect advisories, pin/lock versions appropriately, and review supply-chain risks.
- Use secure transport and secure configuration; never commit secrets.
- Handle errors without leaking internal details or sensitive records.
- Minimize logs; define retention and access. Never log passwords, OTPs, bearer tokens, private keys, or session cookies.
- Define data deletion/export, retention, backup encryption/access, restore, and incident response as appropriate.
- Test critical authorization, validation, concurrency, and abuse cases.

## Release blockers
Unresolved critical vulnerabilities, broken tenant isolation, exposed credentials, unauthorized access to sensitive data, and a destructive data change without a credible recovery path block release unless a formally authorized emergency exception is documented with mitigations and expiry.
