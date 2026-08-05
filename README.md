# INP DataGuard

**Enterprise Data Access Governance, File Activity Monitoring and Secure File Access Platform**

This repository is the canonical public documentation and source-control home for the INP DataGuard project.

## Current baselines

- Operational baseline: **CP-006** — Real Data Only & Event Enrichment Operational Baseline
- Architecture and security baseline: **CP-007** — Security, Unified Identity & Production Technology Baseline
- Product delivery baseline: **CP-008** — Two-Track Delivery, Licensing, Security-First Web Experience & Continuous Documentation Baseline

> The public checkpoint records are sanitized. Customer identifiers, domain names, server names, storage paths, credentials, logs and security evidence must be stored only in approved private repositories or evidence stores.

## Product delivery model

INP DataGuard follows one codebase with two release tracks:

- **Stable Pilot Track** — controlled operational deployments and maintenance releases
- **Enterprise Development Track** — continued development toward `v1.0.0 GA`

Primary target milestones:

1. `v0.2.2-dev` — Production Foundation & Hardening
2. `v0.3.0` — Unified Identity & Secure Authentication
3. `v0.3.5` — Licensing Foundation
4. `v0.4.0` — Permission Analysis & Web Reporting Foundation
5. `v0.5.0-pilot` — Operational Pilot Release
6. `v0.6.0` — Secure Data Portal & Advanced Reporting
7. `v0.7.0` — Multi-Site, HA & Enterprise Scale
8. `v0.8.0` — Connectors & Recovery
9. `v0.9.0-rc` — Release Candidate & Security Validation
10. `v1.0.0 GA` — Commercial General Availability

## Documentation system

The project uses continuous, evidence-based documentation modeled on the INPSan documentation workflow. Every approved change must update the relevant:

- Official Checkpoint
- Work Package
- ADR
- Issue / RCA
- Test & Evidence
- Release Notes
- Baseline Register
- Security and Hardening Register
- License and Entitlement Register
- API and Schema Migration Notes
- Known Limitations
- Pending Items
- Continuation Point

Only items that have been verified and marked **PASS** may enter an operational baseline.

Start here: [`docs/README.md`](docs/README.md)

## Security

Security is the highest-priority release gate. See [`SECURITY.md`](SECURITY.md) and [`docs/security/SECURITY-PROGRAM.md`](docs/security/SECURITY-PROGRAM.md).

## Status

The project currently has a validated working prototype and is entering the Production Foundation phase. The immediate target is `v0.5.0-pilot` for controlled real-world deployments.
