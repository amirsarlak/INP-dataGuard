# INP DataGuard Final Product Roadmap

**Roadmap baseline:** CP-008  
**Delivery model:** One codebase, Stable Pilot Track plus Enterprise Development Track

## Current position

Validated working prototype with CP-006 operational PASS. CP-007 and CP-008 define the production architecture, security, licensing, documentation and two-track delivery model. The active execution point is Production Foundation.

## Roadmap

### `v0.2.2-dev` — Production Foundation & Hardening

- Ubuntu 24.04.4 LTS production baseline
- signed DEB packaging, systemd and AppArmor
- dedicated service identities and default-deny firewall
- HTTPS and collector mTLS
- persistent collector queue, retry, replay and gap detection
- backup/restore, upgrade and rollback foundation
- signed configuration and support diagnostics
- Hardening & Compliance Matrix foundation

**Exit:** reboot, outage, backup/restore, certificate revocation and event-durability tests PASS.

### `v0.3.0` — Unified Identity & Secure Authentication

- AD/LDAP authentication
- Application-Local Users and Groups
- Windows Local SAM Users and Groups
- canonical provider + immutable ID/SID identity model
- MFA, RBAC, session security and login audit
- admin/user authorization boundary
- secure Windows local credential validation through the server-local Collector

**Exit:** no identity collisions across providers; admin MFA and authorization tests PASS.

### `v0.3.5` — Licensing Foundation

- MSU and AGU metering
- offline signed license
- feature entitlements
- grace period, controlled rehost and license audit
- clone/clock-tampering detection
- license usage dashboard and report

**Exit:** capacity and entitlement tests PASS without destructive monitoring shutdown.

### `v0.4.0` — Permission Analysis & Web Reporting Foundation

- Share and NTFS effective permission
- direct/inherited access, allow/deny and permission path
- nested AD and Windows local group resolution
- unresolved SID and broken inheritance detection
- Read-Only Governance
- scoped user and administrator web reporting
- CSV/PDF export with export audit

**Exit:** effective-permission accuracy, object authorization and report-scope tests PASS.

### `v0.5.0-pilot` — Operational Pilot Release

- production C#/.NET Collector
- secure installation and signed update
- operational inventory and activity monitoring
- secure login, MFA, RBAC and licensing
- permission analysis and web reporting
- support bundle, backup/restore and controlled deployment package
- default Read-Only Governance; optional Managed ACL Mode under explicit control

**Exit:** full Pilot acceptance matrix PASS.

### `v0.5.x-pilot` — Stable Pilot Maintenance Track

Only security, bug, compatibility, performance and safe migration changes. Enterprise features enter only after release gates.

### `v0.6.0` — Secure Data Portal & Advanced Reporting

- secure browse, upload and download
- quarantine, antivirus/ICAP and transfer controls
- scheduled reports and subscriptions
- access requests and data-owner reporting

### `v0.7.0` — Multi-Site, HA & Enterprise Scale

- Site Gateway and store-and-forward
- multi-site routing and isolation
- PostgreSQL HA and event scale-out
- centralized licensing and reporting
- disaster recovery and zero-downtime upgrade targets

### `v0.8.0` — Connectors & Recovery

- Samba, NFS and NAS connector expansion
- INPSan, snapshot and backup integration
- recovery mapping and restore workflow
- signed connector modules and capability matrix

### `v0.9.0-rc` — Release Candidate & Security Validation

- independent architecture review and penetration test
- ASVS/CIS verification
- SAST, DAST, fuzzing and capacity testing
- SBOM, signed installer/update and provenance
- Pilot-to-GA upgrade and disaster-recovery validation
- final commercial and legal package

### `v1.0.0 GA` — Commercial General Availability

- production support policy
- commercial licensing
- official compatibility and capacity matrices
- complete installation, hardening, operations, upgrade and recovery documentation
- signed Pilot-to-GA update package

## Permanent cross-cutting workstreams

- Security, Threat Modeling and Hardening
- Release Engineering and Upgrade Safety
- Continuous Documentation and Evidence
- Licensing and Entitlement Integrity
- Compatibility and Capacity Engineering
- Legal, Privacy and Pilot Governance

## Planning estimates

- `v0.5.0-pilot`: 12–16 weeks under regular development
- first controlled installation: 3–4 months
- multi-organization stabilization: 5–7 months
- `v1.0.0 GA`: 10–14 months

Planning estimates must be revised after each checkpoint using actual throughput, defects and acceptance evidence.
