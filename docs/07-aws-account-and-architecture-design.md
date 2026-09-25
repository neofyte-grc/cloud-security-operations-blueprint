# AWS Account and Architecture Design

## Design status

This is a **proposed logical architecture**, not a deployed AWS environment. Final service selection requires workload requirements, cost estimates, implementation design, and testing.

## Account model

| Boundary | Proposed purpose | Governance decision |
|---|---|---|
| Management/billing account | Organization administration only | Restrict daily workload use and tightly control privileged access. |
| Production workload account | Customer-facing dispatch application and data | Separate from development and testing. |
| Nonproduction workload account | Development and validation | Use synthetic or approved de-identified test data. |
| Security/logging boundary | Protected log storage and security administration | Separate administration from ordinary workload operators; select account layout during landing-zone design. |

AWS Organizations and an appropriate landing-zone approach can support these boundaries. PLG should document the chosen organizational units, account owners, approved Regions, budget alerts, and baseline settings before provisioning.

## Proposed workload path

External users connect to an approved application entry point. Application components process authenticated requests and access a protected data tier. Approved integrations exchange minimum necessary information with the WMS and billing processes. Logs and findings flow to the designated security destination. Backups are governed separately from routine application access.

The exact compute, database, API, and connectivity services are implementation choices; the logical boundaries and control objectives are the baseline.

## Design decisions

| ID | Decision | Risk/control link |
|---|---|---|
| AD-01 | Separate production and nonproduction accounts. | R-03, R-05; CLD-01 |
| AD-02 | Restrict administrative access to approved roles and review it. | R-01, R-08; CLD-02 |
| AD-03 | Permit only documented traffic and integration paths. | R-03, R-07; CLD-04 |
| AD-04 | Protect sensitive data and secrets under assigned owners. | R-02, R-05; CLD-05, CLD-06 |
| AD-05 | Route required events to a protected security destination. | R-04; CLD-07, CLD-08 |
| AD-06 | Design and test recovery against approved objectives. | R-06; CLD-11 |

## Architecture review questions

Confirm who provisions accounts, who can alter logging, where data is stored, which systems are exposed to the internet, how on-premises integration authenticates, and what happens when an integration or AWS component is unavailable.

See `diagrams/aws-reference-architecture.md` for the corresponding logical diagram.
