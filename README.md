# SaaS Security Checklist

Ten control areas every SaaS should cover, each mapped to **OWASP**, **SOC 2**, and India's **DPDP Act**. Use it to find gaps before an auditor — or an attacker — does, and to scope a pentest that targets what actually matters.

Maintained by [DebugSol](https://debugsol.com) — fixed-price, human-led penetration testing for Indian SaaS and startups.

> Mappings are a practical guide, not a certification. SOC 2 criteria and DPDP section references follow common commentary; verify against the primary standards and the Act before relying on them for compliance purposes. Not legal advice.

| Control area | What good looks like | OWASP | SOC 2 | DPDP |
|---|---|---|---|---|
| Access control | Every object checks ownership; roles enforced server-side; no IDOR | A01 / ASVS V4 | CC6.1 | 8(5) |
| Authentication | Strong password + MFA, secure reset, session timeout, lockout | A07 / ASVS V2 | CC6.1 | 8(5) |
| Data protection | TLS everywhere; encryption at rest; minimise and segregate personal data | A02 / ASVS V6 | CC6.7 | 8(5), 8(4) |
| Input handling | Parameterised queries, output encoding, SSRF and upload controls | A03 / ASVS V5 | CC7.1 | 8(5) |
| Secrets & config | No secrets in code/repos; hardened headers; least-privilege keys | A05 / ASVS V14 | CC6.1 | 8(5) |
| Dependencies | Track and patch third-party libraries; monitor for known CVEs | A06 / ASVS V1 | CC7.1 | 8(5) |
| Logging & monitoring | Security logs kept, alerting on anomalies, no secrets in logs | A09 / ASVS V7 | CC7.2 | 8(5) |
| Backups & recovery | Tested, access-controlled backups; a recovery you have practised | ASVS V1 | CC7.5 / A1.2 | 8(5) |
| Breach readiness | An incident plan, named owners, and breach-notification steps ready | — | CC7.3 | 8(6) |
| Independent testing | A recent human-led pentest with a retest and attestation | WSTG | CC4.1 / CC7.1 | 8(5) |

## How to use it

Work top to bottom and mark each area red / amber / green. The amber and red rows are your pentest scope. When you're ready for independent proof, the last row — a human-led test with a retest and attestation — is what auditors and enterprise buyers ask to see.

## License

MIT — copy it, fork it, adapt it to your stack.

---

Want a free, passive exposure snapshot of your own domain, or a fixed-price pentest with a retest included? See [debugsol.com](https://debugsol.com).
