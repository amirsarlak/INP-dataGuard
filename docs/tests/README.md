# Test and Evidence Register

Use [`../templates/TEST-EVIDENCE-TEMPLATE.md`](../templates/TEST-EVIDENCE-TEMPLATE.md).

## Evidence policy

Public records contain only sanitized test summaries. Raw logs, ACL exports, infrastructure identifiers, screenshots with sensitive data and security findings must be stored in approved private evidence storage and referenced by evidence ID and hash.

## Register

| Test ID | Component / Version | Scope | Result | Evidence ID | Checkpoint |
|---|---|---|---|---|---|
| Historical CP-006 suite | Management `v0.2.1-dev-r1`, Collector `v0.1.0-dev-r5-r1` | real-data inventory and event enrichment | PASS | private evidence register | CP-006 |
| WP-008-07 documentation review | Documentation repository | structure, links and status separation | Pending | TBD | future checkpoint |

## Minimum release evidence

- clean installation
- upgrade from supported prior version
- rollback / restore
- authentication and authorization
- Collector durability and event replay
- permission calculation accuracy
- hardening compliance
- license capacity and entitlement
- backup/restore
- security scan and SBOM verification
