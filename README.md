# Cloud Security Operations Blueprint

### Building a Governed Cloud Environment

**Portfolio Project 04 | Cloud Security · AWS · GRC**

> **Case study status:** This is a fictional reference design for Peachtree Logistics Group (PLG). It does not represent a deployed AWS environment, a compliance certification, or evidence that the proposed controls operate in production.

## Project at a Glance

Peachtree Logistics Group (PLG) is a fictional Atlanta-based regional logistics company with approximately 225 employees. PLG is considering a move of its dispatch and delivery platform to AWS. Dispatchers need to assign time-sensitive deliveries, while employees and independent couriers need access to the information required for their own work.

The challenge is to protect customer and potentially sensitive medical-delivery information, keep dispatch available, and make cloud security responsibilities clear.

This project follows one trace throughout the design:

**Business requirement → risk → architecture decision → control → owner → test → evidence → monitoring**

## Objectives

- Design a governed AWS environment for the proposed dispatch workload.
- Separate production and nonproduction activity and define administrative ownership.
- Limit workforce, driver, and courier access to approved functions and assignments.
- Protect sensitive data, application interfaces, keys, and secrets.
- Define logging, finding triage, incident response, backup, and recovery workflows.
- Map priority risks to controls, tests, evidence sources, and accountable owners.
- Explain what would need to be implemented and verified before making a claim about control effectiveness.

## Business Scenario and Scope

The proposed workload supports delivery assignments, status updates, and proof of delivery. It exchanges selected information with PLG's existing warehouse management and billing processes.

| In scope | Outside this case study |
|---|---|
| Proposed AWS accounts and dispatch workload | A production AWS deployment |
| Employee and independent-courier access | Vehicle systems and warehouse building security |
| Customer and delivery information | Internal networks operated by vendors |
| Approved WMS and billing integrations | Full penetration testing |
| Cloud logging, response, and recovery design | A company-wide migration of every PLG system |

Whether particular medical-delivery information is PHI/ePHI, and which legal or contractual obligations apply, would require validation before implementation. Payment card data is outside the proposed dispatch workload.

## Frameworks and Design References

- **NIST Cybersecurity Framework 2.0:** Organizes governance and security outcomes across Govern, Identify, Protect, Detect, Respond, and Recover.
- **AWS Well-Architected Framework, Security Pillar:** Guides workload security design and review.
- **AWS Security Reference Architecture:** Informs account boundaries, guardrails, and security visibility.
- **AWS shared responsibility model:** Helps identify what AWS manages and what PLG must configure, operate, and verify.

These references guide the case study. A framework mapping does not establish compliance.

## Key Design Decisions

| Decision | Business or security reason |
|---|---|
| Separate production and nonproduction AWS accounts | Reduce the chance that development activity affects live dispatch operations. |
| Distinguish AWS administrative roles from application user roles | A dispatcher needs dispatch functions, not AWS administrator permissions. |
| Enforce assignment-level authorization | A courier must not retrieve another courier's delivery by changing a record identifier. |
| Restrict documented application and integration paths | Limit unnecessary exposure of the data store, WMS, and billing processes. |
| Route required events to a protected security destination | Support investigation and detect missing monitoring coverage. |
| Define and test recovery objectives | Establish whether dispatch can resume within approved business limits. |

The repository uses risk IDs `R-01` through `R-08` and proposed control IDs `CLD-01` through `CLD-12` to connect these decisions to testing and evidence.

## Documentation

| File | Contents |
|---|---|
| [00 — Project Overview and Methodology](docs/00-project-overview-and-methodology.md) | Purpose, method, document map, and evidence rule |
| [01 — Business Context and Requirements](docs/01-business-context-and-requirements.md) | PLG scenario, requirements, constraints, and success condition |
| [02 — Scope, Assumptions, and Stakeholders](docs/02-scope-assumptions-and-stakeholders.md) | Workload boundary, assumptions, and decision-makers |
| [03 — System and Data Inventory](docs/03-system-and-data-inventory.md) | Proposed components, data types, and owners |
| [04 — Data Flows and Trust Boundaries](docs/04-data-flows-and-trust-boundaries.md) | Operational flows, interfaces, and trust boundaries |
| [05 — Cloud Risk Assessment](docs/05-cloud-risk-assessment.md) | Scoring method and eight scenario-based risks |
| [06 — Shared Responsibility and Ownership](docs/06-shared-responsibility-and-ownership.md) | AWS/PLG responsibilities and operating owners |
| [07 — AWS Account and Architecture Design](docs/07-aws-account-and-architecture-design.md) | Proposed account model and logical architecture |
| [08 — Identity and Access Model](docs/08-identity-and-access-model.md) | Workforce, courier, application, and integration access |
| [09 — Network and Application Protection](docs/09-network-and-application-protection.md) | Entry points, allowed paths, application controls, and failure handling |
| [10 — Data Protection and Key Management](docs/10-data-protection-and-key-management.md) | Data handling, encryption, keys, secrets, and retention |
| [11 — Logging, Detection, and Monitoring](docs/11-logging-detection-and-monitoring.md) | Event sources, coverage, review, and alert workflow |
| [12 — Incident Response and Escalation](docs/12-incident-response-and-escalation.md) | Scenarios, roles, response stages, and decisions |
| [13 — Backup, Recovery, and Resilience](docs/13-backup-recovery-and-resilience.md) | Proposed recovery targets, backup design, and restore exercise |
| [14 — Control Implementation Roadmap](docs/14-control-implementation-roadmap.md) | Control catalogue, sequencing, and launch gate |
| [15 — Control Testing and Evidence Plan](docs/15-control-testing-and-evidence-plan.md) | Representative tests and expected evidence |
| [16 — KPIs, KRIs, and Reporting](docs/16-kpis-kris-and-reporting.md) | Measures, calculations, owners, and reporting cadence |
| [17 — Residual Risk and Exceptions](docs/17-residual-risk-and-exceptions.md) | Time-bound exceptions, approval, and closure |
| [18 — Executive Summary and Reflection](docs/18-executive-summary-and-reflection.md) | Executive decisions, project outcome, and lessons learned |

## Additional Repository Artifacts

The repository structure also provides for these sections as they are completed:

- `controls/` — cloud control matrix, framework crosswalk, and responsibility matrix
- `policies/` — cloud access, logging, and data-protection standards
- `procedures/` — access reviews, finding triage, incident response, and restore testing
- `templates/` — reusable risk, review, finding, exception, and restore-test records
- `evidence/` — a sample evidence index and clearly labeled simulated records
- `diagrams/` — context, architecture, data-flow, identity, and event-workflow diagrams
- `presentation/` — executive briefing

Sample records are fictional. They must not be represented as records from a live PLG or AWS environment.

## What This Project Demonstrates

The portfolio case study demonstrates how I approach cloud security as an operational responsibility: understand the delivery workflow, assess risk, design practical controls, assign people to operate them, and define how their results would be checked.

Its completion standard is traceability. A reader should be able to start with a PLG business requirement, follow it to a risk and architecture choice, identify the control owner, and find the planned test and evidence source.

## Author

**Tommy Marshall**  
GRC and Cloud Security Portfolio  
**NeoFyte — Cybersecurity Made Human**
