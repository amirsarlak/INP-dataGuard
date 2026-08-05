# Security, Hardening & Assurance Program

**Program ID:** `INP-DG-SEC-001`  
**Baseline:** CP-007 + CP-008

## Security objective

Security is the primary product quality attribute and a mandatory release gate for every phase. Security work is continuous across design, implementation, installation, upgrade, operation and incident response.

## Authoritative frameworks

### Linux Management Platform

- current approved CIS Ubuntu Linux 24.04 LTS Benchmark
- default profile: Level 1 Server
- selected Level 2 controls after compatibility testing
- optional tailored Ubuntu STIG controls for High-Security deployments
- FIPS only as an optional regulatory profile

### Windows Collector Host

- Microsoft Security Baseline and Security Compliance Toolkit
- matching CIS Windows Server Benchmark
- no requirement to disable UAC, firewall, Defender or modern authentication controls

### Application and API

- NIST SSDF 1.1
- OWASP ASVS 5.0 Level 2
- selected Level 3 controls for authentication, administration, ACL changes and licensing
- OWASP API Security Top 10
- OWASP WSTG
- OWASP SAMM maturity review

## Mandatory security domains

1. threat modeling and abuse cases
2. identity, MFA, session and recovery security
3. RBAC plus function- and object-level authorization
4. collector trust, mTLS and certificate lifecycle
5. secrets, key management and license signing separation
6. safe ACL command model with no generic remote shell
7. web, API, upload and report-export security
8. database, backup and tamper-evident audit integrity
9. supply-chain security, SBOM, signing and provenance
10. hardening compliance and configuration drift detection
11. vulnerability management and secure update
12. privacy, retention and support-bundle redaction

## Release gate

A production or Pilot release is blocked by:

- unresolved Critical findings;
- unaccepted High findings;
- failed authentication/authorization tests;
- failed backup, restore or ACL rollback validation;
- unsigned artifacts or missing SBOM;
- missing security evidence;
- undocumented hardening exceptions;
- capability requiring arbitrary shell or PowerShell execution.

## Login baseline

Admin MFA is mandatory. User MFA is policy-controlled. Both portals require rate limits, generic errors, secure cookies, CSRF protection, CSP, HSTS, session rotation, idle/absolute timeout, revocation and login audit.

## Hardening rule

CIS Level 2, STIG and regulatory controls are never applied blindly. Every control is tailored, tested and recorded in the Hardening & Compliance Matrix. Exceptions require risk owner, rationale, compensating control and review date.

## Evidence

Security test results and sensitive evidence are retained in approved private storage. Public records reference evidence IDs without exposing environment identifiers or vulnerability details.
