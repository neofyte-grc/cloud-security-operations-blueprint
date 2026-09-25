# Data Protection and Key Management

## Data handling decisions

The Application Owner and Privacy/Legal Adviser must confirm whether any medical-delivery field is protected health information and which contracts or laws apply. Until confirmed, the design treats these fields as sensitive and minimizes their use. Payment card data is not included in the dispatch workload.

| Data | Proposed protection |
|---|---|
| Customer and recipient details | Restrict by business role and assignment; minimize fields shown to couriers. |
| Medical-delivery details | Restrict to the minimum necessary workflow and review retention and disclosure rules. |
| Proof of delivery | Limit access, define retention, and protect stored records. |
| Identity and audit records | Restrict administrative access and avoid unnecessary sensitive payloads in logs. |
| Nonproduction data | Use synthetic or approved de-identified data unless an exception is approved. |

## Proposed technical requirements

- Encrypt approved data in transit and at rest using service-appropriate mechanisms.
- Record which keys protect each data store, who administers them, and who may use them.
- Separate key administration from ordinary application data access where feasible.
- Store integration secrets in an approved secret-management mechanism; define rotation and emergency replacement.
- Block unintended public access to sensitive storage.
- Define retention, deletion, and legal-hold decisions before production use.
- Review backups, exported reports, logs, and support artifacts for sensitive data exposure.

Encryption does not correct excessive application permissions: assignment-level authorization remains necessary.

## Key and secret lifecycle

The Cloud Platform Lead maintains the key/secret inventory and technical settings. The Application Owner identifies dependencies and validates that rotation does not interrupt dispatch. Security/GRC reviews access and change evidence.

A key or secret rotation record should include owner, affected components, approval, execution time, validation, and rollback decision. Emergency replacement follows the incident process.

This design addresses R-02 and R-05 through `CLD-03`, `CLD-05`, and `CLD-06`. Configurations and rotation results become evidence only after implementation and verification.
