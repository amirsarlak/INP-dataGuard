# Continuous Documentation Standard

**Document ID:** `INP-DG-DOC-STD-001`  
**Baseline:** CP-008

## Purpose

This standard applies the continuous documentation method used for INPSan to INP DataGuard. Documentation is part of implementation, acceptance and release—not an activity postponed until project completion.

## Mandatory update set

After every approved implementation, defect correction or design decision, update all applicable records:

1. Official Checkpoint
2. Work Package
3. ADR
4. Issue / RCA
5. Test & Evidence
6. Release Notes
7. Baseline Register
8. Security / Threat Model Register
9. License & Entitlement Register
10. API and Database Migration Notes
11. Known Limitations
12. Pending Items
13. Current Continuation Point
14. Installation, Upgrade, Rollback, Backup/Restore and Hardening Guides

## Traceability chain

`Requirement → Work Package → ADR → Commit/PR → Test → Evidence → Release → Checkpoint`

Every production-relevant change must be traceable across this chain.

## Approval states

| State | Meaning |
|---|---|
| DRAFT | incomplete record |
| DESIGNED | approved design, not implemented |
| IMPLEMENTED | code/configuration exists |
| TESTED | test run completed, acceptance pending |
| PASS | accepted and baseline-eligible |
| FAILED | acceptance criteria not met |
| DEFERRED | intentionally postponed |
| DEPRECATED | no longer approved |

Only `PASS` items may be copied into an operational checkpoint.

## Naming scheme

- Checkpoint: `INP-DG-CP-XXX`
- Work Package: `INP-DG-WP-XXX`
- ADR: `INP-DG-ADR-XXX`
- Issue: `INP-DG-ISSUE-XXX`
- RCA: `INP-DG-RCA-XXX`
- Test: `INP-DG-TEST-XXX`
- Evidence: `INP-DG-EVIDENCE-XXX`
- Release: `INP-DG-REL-vX.Y.Z`

## Evidence requirements

Evidence may include sanitized logs, API output, service status, database query results, screenshots, hashes, performance results, restore output and security-scan reports. Each evidence record must identify:

- component and version;
- environment classification;
- test date;
- operator/reviewer;
- expected and actual result;
- result status;
- source artifact hash or protected location.

## Public/private boundary

This repository is public. Public records must be sanitized. Store customer names, infrastructure identifiers, real paths, IP addresses, logs, ACL exports, certificates and unredacted evidence only in approved private storage. Public documents may reference private evidence IDs without copying the sensitive artifact.

## Completion rule

A phase is not complete until:

- implementation is versioned;
- tests and evidence exist;
- security impacts are reviewed;
- install/upgrade/rollback impacts are documented;
- registers and continuation point are updated;
- the checkpoint accurately separates PASS from pending work.
