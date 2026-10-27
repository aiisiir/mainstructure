# Quality Gate: Security and Privacy

- [ ] Threat model covers assets, actors, entry points and trust boundaries.
- [ ] Protected operations enforce authorization server-side.
- [ ] Object/tenant isolation is tested where applicable.
- [ ] Inputs, uploads, callbacks/webhooks, rate-sensitive endpoints, and external responses are validated.
- [ ] Secrets are not committed or logged; environment secrets are managed appropriately.
- [ ] Sessions/tokens/OTP/CSRF protections are reviewed as applicable.
- [ ] Error responses do not disclose internals or sensitive data.
- [ ] Dependencies and known vulnerabilities are reviewed.
- [ ] Data retention, deletion, exports, logging, backups, and access policies are defined.
- [ ] Critical/high risks have resolved mitigations or accountable formal acceptance.
