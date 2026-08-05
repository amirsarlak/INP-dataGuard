# Security Policy

Security is the highest-priority release gate for INP DataGuard.

## Reporting a vulnerability

Do not disclose suspected vulnerabilities through public GitHub issues.

Use the approved private security contact channel for the project owner. Include:

- affected version and component;
- reproduction steps;
- expected and actual behavior;
- impact assessment;
- logs or evidence with secrets removed;
- proposed mitigation, when available.

## Prohibited public content

Never commit or publish:

- credentials, tokens, private keys or license signing keys;
- customer names or identifying infrastructure details;
- domain names, server names, IP addresses or storage paths from real deployments;
- raw event logs or access-control exports from customers;
- unredacted vulnerability evidence;
- support bundles containing personal or operational data.

## Security baseline

The project uses:

- NIST SSDF 1.1;
- OWASP ASVS 5.0 Level 2 and selected Level 3 controls;
- OWASP API Security and WSTG;
- CIS Ubuntu Linux 24.04 LTS Level 1 with selected Level 2 controls;
- Microsoft Security Baselines and matching CIS Windows Server guidance;
- signed artifacts, SBOM, mTLS and tamper-evident audit.

See [`docs/security/SECURITY-PROGRAM.md`](docs/security/SECURITY-PROGRAM.md).

## Release rule

A release is blocked by:

- any unresolved Critical security finding;
- any unaccepted High security finding;
- an unsigned production artifact;
- missing SBOM or provenance;
- failed backup/restore validation;
- failed ACL rollback validation;
- failed authentication or authorization acceptance tests.
