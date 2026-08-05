# Baseline Register

| Baseline | Type | Date | Status | Supersedes | Notes |
|---|---|---:|---|---|---|
| CP-003 | Design Foundation | historical | PASS/design | — | UX, event model, API and security design foundation |
| CP-004 | Operational Prototype | historical | PASS/prototype | CP-003 operational aspects | first runnable prototype |
| CP-005 | Platform & OS | historical | PASS/prototype | CP-004 platform aspects | Linux central platform and Windows/Linux collector direction |
| CP-006 | Operational Baseline | 2026-08-04 | PASS | prior operational baseline | real-data-only inventory and event enrichment baseline |
| CP-007 | Architecture/Security | 2026-08-04 | DESIGNED | no operational supersession | production OS, technology stack, security and identity design |
| CP-008 | Product Strategy | 2026-08-05 | DESIGNED | roadmap portions of CP-007 | two-track delivery, licensing, secure web reporting and continuous documentation |

## Current component baseline

| Component | Current accepted baseline | Status |
|---|---|---|
| Management Server | `v0.2.1-dev-r1` | PASS under CP-006 |
| Store Schema | `1.2` | PASS under CP-006 |
| Data Policy | `real_data_only` | PASS under CP-006 |
| Windows Collector | `v0.1.0-dev-r5-r1` | PASS prototype under CP-006 |
| API | `v1` | PASS prototype under CP-006 |
| Production OS target | Ubuntu Server `24.04.4 LTS` | DESIGNED under CP-007 |
| Production Collector target | C# / `.NET 10 LTS` | DESIGNED under CP-007 |
| Management technology | Go `1.26.x` | DESIGNED under CP-007 |
| Web technology | TypeScript `5.9.x` / React `19.2.x` | DESIGNED under CP-007 |
| Database target | PostgreSQL `18` | DESIGNED under CP-007 |
| Delivery target | `v0.5.0-pilot` | PLANNED under CP-008 |

## Baseline governance

- Design baselines do not claim implementation.
- Operational baselines require test evidence and PASS status.
- Sensitive environment-specific evidence is held in approved private storage.
- Every superseding checkpoint must explicitly state which prior baseline elements remain valid.
