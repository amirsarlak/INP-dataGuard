# Contributing to INP DataGuard

## Change discipline

Every production-relevant change must be traceable:

`Requirement → Work Package → ADR/Issue → Pull Request → Test → Evidence → Release Notes → Checkpoint`

## Before implementation

- identify or create the Work Package;
- document architecture/security decisions in an ADR when material;
- define acceptance and rollback criteria;
- assess installation, migration, licensing and documentation impact;
- keep customer-sensitive information out of this public repository.

## Pull requests

A pull request must state:

- target release and Work Package;
- functional and security impact;
- database/API/Collector compatibility impact;
- install/upgrade/rollback impact;
- tests and evidence;
- documentation and release-note updates;
- known limitations and pending work.

## Security

Never use public issues or pull requests for unredacted vulnerabilities, credentials, keys, customer data or infrastructure details. Follow [`SECURITY.md`](SECURITY.md).

## Baseline rule

Implementation alone is not PASS. A change enters an operational checkpoint only after its acceptance criteria and evidence have been reviewed and accepted.
