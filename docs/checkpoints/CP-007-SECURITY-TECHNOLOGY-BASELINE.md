# INP DataGuard CP-007

**Title:** Security, Unified Identity & Production Technology Baseline  
**Timestamp:** 2026-08-04 21:48 +03:30  
**Type:** Design / Architecture / Roadmap Baseline  
**Implementation status:** `DESIGNED`

CP-007 does not replace the CP-006 operational PASS baseline. It locks the production architecture and security direction.

## Production technology baseline

- OS: Ubuntu Server `24.04.4 LTS` Minimal amd64
- Kernel track: GA `6.8`
- Linux deployment: signed native DEB packages, systemd and AppArmor
- Development/lab deployment: Docker Compose only
- Management Core: Go `1.26.x`
- Windows Production Collector: C# / `.NET 10 LTS`
- Web frontend: TypeScript `5.9.x` and React `19.2.x`
- Frontend build runtime: Node.js `24 LTS`, build/test only
- Database target: PostgreSQL `18`, current approved minor at release time
- Operational scripting: PowerShell and Bash only for installation, bootstrap, diagnostics, backup/restore, migration and repair

## Security baseline

- NIST SSDF 1.1
- OWASP ASVS 5.0 Level 2
- selected ASVS Level 3 controls for login, administration, ACL changes and licensing
- OWASP API Security
- CIS Ubuntu Server 24.04 Level 1 plus selected Level 2 controls
- default-deny networking
- key-only SSH and administrative network restriction
- AppArmor enforcing and systemd sandboxing
- dedicated service identities
- mandatory collector mTLS and per-collector certificates
- signed packages, commands, configuration and updates
- SBOM and release provenance
- opaque server-side sessions and mandatory administrator MFA
- tamper-evident audit
- no generic remote shell or arbitrary PowerShell execution

## Unified identity baseline

Supported identity domains:

- Active Directory / LDAP
- Application-Local Users and Groups
- Windows Local SAM Users and Groups

Canonical identity must be based on provider plus immutable identifier or SID, not username. Application Identity and Storage Principal remain separate concepts unless an explicit mapping is approved.

## Safe ACL operation

`Request → Preview → Impact Analysis → Approval → State Hash Check → Signed Command → Execute → Read-back Verify → Audit → Rollback`

## Release scope sequence

- `v0.2.2-dev` — Service, OS and Collector Hardening
- `v0.3.0` — Unified Identity, Authentication, MFA and RBAC
- `v0.4.0` — Effective Permission and Safe ACL Governance
- `v0.5.0` — Event Platform and Detection
- `v0.6.0` — Secure Data Portal
- `v0.7.0` — Multi-Site and Enterprise Scale
- `v0.8.0` — Connector and Recovery Expansion
- `v0.9.0` — Release Candidate
- `v1.0.0` — General Availability

This sequence is refined by CP-008 into the two-track Pilot and Enterprise delivery model.
