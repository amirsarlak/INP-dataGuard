# INP DataGuard CP-008

**Title:** Two-Track Delivery, Licensing, Security-First Web Experience & Continuous Documentation Baseline  
**Timestamp:** 2026-08-05 23:42 +03:30  
**Type:** Product Strategy / Roadmap / Commercial & Documentation Baseline  
**Implementation status:** `DESIGNED`

CP-008 retains CP-006 as the operational PASS baseline and CP-007 as the architecture and technology baseline.

## 1. Two-track delivery model

A single codebase and migration path support:

- **Stable Pilot Track** — `v0.5.x-pilot`, limited to security, bug, compatibility and safe performance fixes
- **Enterprise Development Track** — continued capability delivery through `v1.0.0 GA`

The Pilot must be production-grade for security, installation, update, backup/restore, event durability and audit. It is not a disposable demo.

## 2. Pilot operating mode

- default mode: Read-Only Governance
- optional mode: Managed ACL Mode
- ACL write requires preview, approval, current-state backup, signed execution, read-back verification, audit and rollback

## 3. Licensing baseline

Licensing uses two independent capacity metrics:

- `Managed Server Units (MSU)` — unique actively managed file/storage servers
- `Active Governed Users (AGU)` — unique canonical identities in governance scope or active during the approved rolling period

Identity counting uses provider plus immutable ID/SID, not username. Feature entitlements are separate from server/user capacity.

Required license characteristics:

- offline-capable and digitally signed
- controlled rehost
- grace period
- clone and clock-tampering detection
- license usage audit
- no destructive shutdown of monitoring when capacity is exceeded

## 4. Security-first web experience

Administrator and user login must include:

- MFA policy, mandatory for administrators
- rate limiting and progressive delay
- account lock and session revocation
- generic authentication errors
- secure, HttpOnly and SameSite cookies
- CSRF protection, CSP and HSTS
- session rotation and expiry
- login and failed-login audit
- object-level authorization for every API and report
- route and authorization separation between Admin Portal and User Portal

## 5. Web reporting

Pilot reporting includes:

- user activity
- file changes, delete and rename
- permission exposure and effective access
- login history
- collector health and delivery gaps
- license usage
- scoped web viewing, filtering and search
- CSV/PDF export with export audit

Users only see records authorized by RBAC, ownership and resource scope.

## 6. Continuous documentation

Every approved change updates the applicable:

- checkpoint
- work package
- ADR
- issue/RCA
- test/evidence
- release notes
- baseline register
- security and threat-model register
- license and entitlement register
- API/schema migration notes
- known limitations
- pending items and continuation point

## 7. Hardening and release-engineering addendum

Permanent workstreams:

- Hardening, Compliance & Security Assurance
- Release Engineering, Installation & Upgrade

Each release provides Fresh Install and signed In-Place Upgrade, preflight checks, backups, versioned database migrations, post-upgrade validation and rollback.

## 8. Approved roadmap

1. `v0.2.2-dev` — Production Foundation, OS/Service/Collector Hardening
2. `v0.3.0` — Unified Identity, Secure Login, MFA and RBAC
3. `v0.3.5` — Licensing Foundation
4. `v0.4.0` — Permission Analysis and Web Reporting Foundation
5. `v0.5.0-pilot` — Operational Pilot Release
6. `v0.5.x-pilot` — Stable Maintenance Track
7. `v0.6.0` — Secure Data Portal and Advanced Reporting
8. `v0.7.0` — Multi-Site, HA and Enterprise Scale
9. `v0.8.0` — Connectors and Recovery
10. `v0.9.0-rc` — Independent Security and Release Validation
11. `v1.0.0 GA` — Commercial General Availability and Pilot-to-GA Upgrade

## 9. Target schedule

- Operational Pilot target: approximately 12–16 weeks under regular development
- first controlled deployment: approximately 3–4 months
- stabilization across multiple organizations: approximately 5–7 months
- `v1.0.0 GA`: approximately 10–14 months

These are planning estimates, not contractual delivery commitments.
