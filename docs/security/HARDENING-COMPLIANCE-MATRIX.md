# Hardening & Compliance Matrix

**Work Package:** `WP-008-09`  
**Status:** `DESIGNED`

Use one row per applicable control. The matrix must be populated and evidenced during implementation.

| Control ID | Source / Version | Component | Profile | Applicability | Implementation | Verification | Evidence ID | Exception / Compensating Control | Risk Owner | Status | Last Review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| TBD | CIS Ubuntu 24.04 | Linux OS | Standard | TBD | TBD | TBD | TBD | — | TBD | DRAFT | — |
| TBD | Ubuntu STIG | Linux OS | High Security | TBD | TBD | TBD | TBD | TBD | TBD | DRAFT | — |
| TBD | Microsoft Baseline | Windows Collector Host | Standard | TBD | TBD | TBD | TBD | — | TBD | DRAFT | — |
| TBD | CIS Windows Server | Windows Collector Host | Standard | TBD | TBD | TBD | TBD | TBD | TBD | DRAFT | — |
| TBD | OWASP ASVS 5.0 | Admin/User Web | Application | TBD | TBD | TBD | TBD | — | TBD | DRAFT | — |
| TBD | OWASP API Security | REST/gRPC API | Application | TBD | TBD | TBD | TBD | — | TBD | DRAFT | — |

## Required profile sets

- `Standard`: CIS Ubuntu Level 1 plus tested selected Level 2 controls
- `High Security`: Standard plus tailored STIG controls
- `Regulated`: High Security plus customer-specific regulatory requirements and optional FIPS profile

## Audit lifecycle

`Installation Audit → Post-Install Audit → Monthly Drift Audit → Pre-Upgrade Audit → Post-Upgrade Audit → Incident Audit`

## Exception rule

An exception is invalid unless it records:

- incompatibility or operational reason;
- security impact;
- compensating control;
- approving risk owner;
- expiry/review date;
- validation evidence.

The matrix becomes operational only after all mandatory Standard-profile controls are implemented, tested and marked `PASS` or have approved exceptions.
