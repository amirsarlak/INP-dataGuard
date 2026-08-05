# Installation, Upgrade and Rollback Baseline

**Work Packages:** `WP-008-10`, `WP-008-11`  
**Status:** `DESIGNED`

## Release bundle

Each release must provide:

- signed Linux DEB packages
- signed Windows Collector MSI
- offline installation bundle
- manifest, checksums and signatures
- SBOM and provenance
- versioned database migrations
- preflight and post-install validation
- backup/restore tools
- installation, upgrade and rollback guides
- release notes, compatibility matrix and known limitations

## Fresh installation

`Preflight → Bundle Signature Verification → Package Installation → Service Identity and Hardening → Database Initialization/Migration → PKI/TLS Setup → License Import → Collector Enrollment → Acceptance Validation`

Production Linux uses Ubuntu Server 24.04.4 LTS Minimal, native DEB packages, systemd and AppArmor. Docker Compose remains a development/lab method.

## In-place upgrade

`Preflight → Signature Verification → Compatibility Check → Health Check → Backup → Package Staging → Maintenance Mode → Schema Migration → Service Upgrade → Post-Upgrade Validation → Commit or Rollback`

The Collector must continue collecting into its durable queue while the Management Server is unavailable and replay events after reconnection with deduplication, sequence validation and gap detection.

## Compatibility policy

Management Server version `N` supports Collector `N` and `N-1` at minimum. Upgrade order:

1. Management Server
2. health and compatibility validation
3. staged Collector upgrade
4. final evidence and checkpoint update

## Automatic pre-upgrade backup

- database
- configuration
- certificate metadata
- license state
- package manifest
- schema version
- rollback point

## Rollback modes

### Package rollback

Used when the database schema remains backward compatible. Restore previous packages, web assets, configuration and service definitions.

### Full restore rollback

Used when a migration is not backward compatible. Stop services, restore the pre-upgrade database/configuration and previous packages, validate, then replay queued Collector events.

Every migration must declare:

- source and target schema version;
- reversibility;
- rollback method;
- preconditions;
- maximum expected downtime;
- expected data impact;
- verification and evidence requirements.

## Mandatory test matrix per release

- clean install
- upgrade from supported N-1
- failed signature
- insufficient disk / failed preflight
- migration failure injection
- service-start failure
- post-upgrade validation failure
- package rollback
- full restore rollback
- Collector queue preservation
- Pilot-to-GA upgrade where applicable

No release is accepted without PASS evidence for applicable scenarios.
