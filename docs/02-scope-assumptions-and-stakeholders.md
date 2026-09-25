# Scope, Assumptions, and Stakeholders

## Scope boundary

This case study covers the proposed AWS-hosted dispatch and delivery workload and its interfaces with PLG users, independent couriers, the WMS, and billing. It covers workload governance, not a company-wide migration of every PLG system.

**Included:** AWS accounts, identity, application access, network paths, data stores, logging, detection, incident response, backup, recovery, control ownership, and evidence planning.

**Excluded:** Vehicle systems, warehouse building security, internal networks operated by vendors, full penetration testing, and a production AWS deployment.

## Working assumptions

| ID | Assumption | Validation needed before implementation |
|---|---|---|
| A-01 | PLG can establish separate production and nonproduction AWS accounts. | Confirm account ownership, budget, and landing-zone approach. |
| A-02 | An approved identity source exists for employees. | Confirm federation and joiner/mover/leaver integration. |
| A-03 | Independent couriers can be identified individually. | Confirm contracting, identity verification, and offboarding processes. |
| A-04 | Existing systems can exchange a minimum necessary data set through approved interfaces. | Confirm APIs, formats, availability, and vendor limits. |
| A-05 | PLG can define data retention and recovery targets with business owners. | Obtain approvals and applicable contractual requirements. |
| A-06 | No active incident is underway at project start. | Verify during real kickoff. |

An invalid assumption triggers a design review; it is not silently treated as a completed control.

## Stakeholders

| Role | Decision or operating responsibility |
|---|---|
| COO, executive sponsor | Approves priorities, resources, and material residual risk. |
| CIO/IT Director | Owns the cloud program and approves technical design and staffing. |
| Dispatch Manager | Defines dispatch workflow, outage impact, and user needs. |
| Warehouse Operations Manager | Defines WMS integration and operational dependencies. |
| HR Manager | Owns employee status inputs for provisioning and removal. |
| Courier Program Owner | Owns courier eligibility and timely removal of access. |
| Cloud Platform Lead | Owns account baseline, infrastructure, and technical implementation. |
| Application Owner | Owns application functions, authorization rules, and release decisions. |
| Security/GRC Lead | Coordinates risk, control review, testing, exceptions, and reporting. |
| Incident Lead | Coordinates security event response and escalation. |
| Privacy/Legal Adviser | Validates data and contractual obligations when applicable. |

An individual may hold multiple roles in a small team, but each control still needs one named accountable owner before launch.
