# Licensing and Entitlement Baseline

**Target:** `v0.3.5`  
**Status:** `DESIGNED`

## Capacity metrics

### Managed Server Units — MSU

A unique server or storage endpoint that is registered and actively inventoried. Renaming a server must not consume a new unit. Clones and duplicated Collector identities must be detected.

### Active Governed Users — AGU

A unique canonical identity that has effective access to a managed resource or generated governed activity during the approved rolling period. Counting uses `provider_id + immutable_id/SID`, not username.

Separate identities remain separate unless explicitly mapped:

- AD/LDAP identity
- Windows Local SAM identity
- Application-Local identity
- future external identity

## Entitlement model

Capacity and feature entitlement are independent:

- server limit
- governed-user limit
- enabled features
- edition
- issue/expiry dates
- grace period
- customer and deployment binding

## Required security properties

- offline-capable signed license
- product contains verification key only; signing key is never distributed
- controlled rehost
- clock rollback and clone detection
- validation and capacity-change audit
- signed, bounded cache for temporary offline validation

## Safe over-capacity behavior

`Warning → Administrator Notification → Grace Period → Restrict New Enrollment → Renew/Upgrade`

The system must not destructively stop monitoring, delete events or block backup/export when license capacity is exceeded. Existing governed resources remain monitored while new enrollment may be restricted.

## Initial commercial draft

| Edition | Managed Servers | Governed Users | Notes |
|---|---:|---:|---|
| Pilot | 1–3 | up to 100 | controlled, time-limited deployment |
| Professional-S | 5 | 250 | draft only |
| Professional-M | 10 | 500 | draft only |
| Professional-L | 25 | 1,500 | draft only |
| Enterprise | contractual | contractual | multi-site and enterprise features |

These numbers are not final pricing or contractual limits. They must be validated through Pilot usage and commercial review.

## Acceptance requirements

- accurate MSU/AGU calculation
- no double counting caused by renaming
- correct provider/SID identity separation
- signed offline import and tamper rejection
- grace-period and over-capacity behavior
- rehost flow
- license usage dashboard and report
- complete audit trail
