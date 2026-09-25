# System and Data Inventory

## Proposed system inventory

| ID | Component | Purpose | Proposed owner | Boundary |
|---|---|---|---|---|
| S-01 | AWS production account | Hosts the dispatch workload | Cloud Platform Lead | AWS production |
| S-02 | AWS nonproduction account | Development and testing | Cloud Platform Lead | AWS nonproduction |
| S-03 | Dispatch application and API | Assignments, status, proof of delivery | Application Owner | Production workload |
| S-04 | Application data store | Operational records | Application Owner | Production data tier |
| S-05 | Employee identity source | Employee lifecycle and sign-in | IT Director/HR Manager | PLG corporate |
| S-06 | Courier identity process | Individual courier enrollment and removal | Courier Program Owner | PLG/application |
| S-07 | On-premises WMS | Warehouse fulfillment information | Warehouse Operations Manager | PLG on-premises |
| S-08 | Billing/accounting system | Approved billing inputs | Finance Owner | PLG corporate/vendor |
| S-09 | Central security log destination | Protected copies of selected logs | Cloud Platform Lead | Separate security boundary |
| S-10 | Monitoring and finding workflow | Alert review, assignment, and tracking | Security/GRC Lead | Security operations |

These are **proposed logical components**. Selecting a particular compute, database, or integration service requires a subsequent implementation design.

## Data inventory

| ID | Data | Sensitivity and handling decision to validate | Primary users |
|---|---|---|---|
| D-01 | Delivery assignment and route details | Internal; restrict to assigned work | Dispatchers, assigned drivers/couriers |
| D-02 | Customer and recipient contact details | Sensitive personal information; minimize display and retention | Dispatchers, assigned drivers/couriers |
| D-03 | Medical-delivery details | Potentially sensitive; confirm whether any data is PHI/ePHI and apply resulting requirements | Authorized dispatchers and assigned couriers |
| D-04 | Proof-of-delivery records | Sensitive operational/customer records | Dispatch, customer service, authorized billing |
| D-05 | Workforce and courier identities | Sensitive identity and access records | Authorized administrators |
| D-06 | Security and application logs | May contain identifiers; prohibit unnecessary sensitive payloads | Security and platform personnel |
| D-07 | Billing references | Restrict to minimum fields needed for billing | Finance and authorized integration |

**Payment card data is outside the proposed dispatch workload.** A discovery finding that cardholder data enters S-03 would require a revised scope and architecture review.

## Inventory maintenance

The Application Owner updates application and data entries when functionality changes. The Cloud Platform Lead maintains AWS resource inventory. Security/GRC reviews ownership and classification at least quarterly and when a material new data flow is proposed.
