# INP DataGuard Documentation Control Center

This directory is the controlled documentation system for INP DataGuard.

## Documentation principles

1. Documentation is updated continuously with implementation.
2. Design decisions and operational evidence are separate.
3. Only verified items marked `PASS` enter an operational baseline.
4. Every release must be installable, upgradeable, testable and rollback-capable.
5. Public documentation must not contain customer-sensitive infrastructure data.

## Status vocabulary

- `DRAFT` — under preparation
- `DESIGNED` — approved design, not yet implemented
- `IMPLEMENTED` — code/configuration exists, validation incomplete
- `TESTED` — testing performed, result not yet accepted
- `PASS` — accepted and eligible for operational baseline
- `FAILED` — acceptance criteria not met
- `DEFERRED` — intentionally postponed
- `DEPRECATED` — no longer approved for new use

## Directory map

- [`checkpoints/`](checkpoints/) — official project baselines
- [`roadmap/`](roadmap/) — final product and release roadmap
- [`governance/`](governance/) — documentation rules and traceability
- [`work-packages/`](work-packages/) — planned and active execution packages
- [`adr/`](adr/) — architecture decision records
- [`issues/`](issues/) — issue and root-cause records
- [`tests/`](tests/) — acceptance tests and evidence indexes
- [`registers/`](registers/) — baseline and control registers
- [`security/`](security/) — security program and hardening matrix
- [`licensing/`](licensing/) — licensing model and entitlement controls
- [`release/`](release/) — installation, upgrade and rollback engineering
- [`pilot/`](pilot/) — operational pilot definition
- [`templates/`](templates/) — controlled document templates
- [`continuation/`](continuation/) — current state, pending work and next action

## Current official records

- [`CP-006`](checkpoints/CP-006-OPERATIONAL-BASELINE.md)
- [`CP-007`](checkpoints/CP-007-SECURITY-TECHNOLOGY-BASELINE.md)
- [`CP-008`](checkpoints/CP-008-TWO-TRACK-DELIVERY-BASELINE.md)
- [`Final Roadmap`](roadmap/PRODUCT-ROADMAP.md)
- [`Current Status and Next Action`](continuation/CURRENT-STATUS-AND-NEXT-ACTION.md)
