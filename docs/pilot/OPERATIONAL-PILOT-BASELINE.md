# Operational Pilot Baseline

**Target release:** `v0.5.0-pilot`  
**Status:** `DESIGNED`

## Objective

Deploy a secure, supportable, real-world edition to selected organizations before full Enterprise GA. The Pilot is an operational product release with constrained scope, not a disposable demonstration.

## Mandatory Pilot capabilities

- production Ubuntu installation and signed upgrades
- production C#/.NET Windows Collector
- HTTPS and per-Collector mTLS
- durable queue, retry, replay and delivery-gap monitoring
- AD/LDAP, Application-Local and Windows Local SAM identity support
- secure admin/user login, MFA, RBAC and session audit
- MSU/AGU licensing and feature entitlements
- file server/share/resource/ACL inventory
- file create/modify/rename/delete and ACL-change monitoring
- permission analysis and scoped web reporting
- backup/restore, support bundle and operational health reporting

## Default safety mode

The Pilot operates in `Read-Only Governance` by default.

`Managed ACL Mode` is optional and requires explicit enablement, limited scope, permission preview, approval, ACL backup, signed execution, read-back verification, audit and rollback.

## Initial capacity targets

These are benchmark targets, not contractual guarantees:

- one site
- 1–3 Windows File Servers
- up to 5 Collectors
- approximately 100–500 users depending on Pilot license
- up to approximately one million indexed files/folders
- up to approximately 250,000 events/day
- 30–90 days online event retention

## Pilot sequence

1. friendly controlled environment, limited share scope, 30 days
2. selected customer, real data, 60–90 days
3. diverse environment including Local SAM/workgroup or air-gapped constraints, 90 days

## Customer entry requirements

- named technical owner
- approved server/share scope
- supported VM/server baseline
- controlled audit policy
- verified backup
- maintenance-window agreement
- security and issue-reporting agreement
- Pilot Agreement, NDA and responsibility matrix

## Pilot acceptance outcomes

- no unaccounted event loss
- stable install/upgrade/rollback
- secure authentication and authorization
- accurate identity and permission analysis
- supportable diagnostics without secret leakage
- documented performance and compatibility limits
- actionable defects captured as Issue/RCA/Test/Evidence records

## Upgrade commitment

Pilot installations must upgrade in place to later Pilot maintenance releases and ultimately to `v1.0.0 GA` through signed migration packages. Reinstallation is not the normal upgrade model.
