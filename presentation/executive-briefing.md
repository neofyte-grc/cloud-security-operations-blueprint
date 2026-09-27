# Executive Briefing: Cloud Security Operations Blueprint

**Prepared by:** Tommy Marshall  
**Organization:** Peachtree Logistics Group (PLG), fictional  
**Decision context:** Proposed migration of the dispatch and delivery platform to AWS  
**Status:** Design and assurance plan; no production implementation is claimed

---

## 1. Business decision

PLG needs dispatchers, employee drivers, and independent couriers to exchange delivery information quickly. The proposed AWS workload must support time-sensitive operations while limiting access to customer and potentially sensitive medical-delivery details.

**Executive decision requested:** Approve discovery and detailed implementation planning, name accountable owners, and validate the business recovery and data-handling requirements.

---

## 2. What the assessment found

The scenario-based assessment identifies eight risks. The leading concerns are:

| Risk | Business consequence |
|---|---|
| R-02: Cross-courier record access | Exposure of customer or medical-delivery details |
| R-01: Compromised workforce identity | Unauthorized dispatch or cloud action |
| R-04: Incomplete or alterable logs | Delayed or inconclusive investigation |
| R-06: Data loss or prolonged outage | Interrupted delivery operations |

These are assessed scenarios, not observed incidents at a real PLG.

---

## 3. Proposed design

- Separate production and nonproduction account boundaries.
- Give AWS administrators and dispatch users distinct roles.
- Check each courier's current assignment for every relevant record request.
- Restrict application, data-store, WMS, and billing paths.
- Protect sensitive data, keys, secrets, logs, and backups.
- Assign people to review findings, coordinate incidents, and test recovery.

Twelve proposed controls, CLD-01 through CLD-12, connect this design to owners and tests.

---

## 4. Ownership and verification

The CIO/IT Director owns the cloud program decision. The Cloud Platform Lead owns the account baseline, network settings, logs, and restore execution. The Application Owner owns application authorization and interfaces. The Security/GRC Lead coordinates risk, testing, finding review, and evidence. The Dispatch Manager judges operational usability. The COO decides whether to accept material residual risk.

For each priority control, PLG must collect dated configuration or process records and test the intended outcome. A policy, diagram, or filled sample template does not establish that a control operates.

---

## 5. Recovery decision

The case study uses a hypothetical **four-hour RTO** and **one-hour RPO** to demonstrate planning. PLG leadership must approve achievable targets based on actual delivery needs and test results.

The simulated restore example misses the proposed RTO by 25 minutes. It illustrates how a failed objective should be documented and escalated; no real AWS restore occurred.

---

## 6. Recommended implementation order

1. Approve scope, data classification, recovery needs, account ownership, and risk owners.
2. Establish account boundaries and identity processes.
3. Implement application authorization, restricted paths, data protection, and integrations.
4. Enable and verify required logging and finding response.
5. Exercise incident and recovery procedures; resolve failed tests.
6. Review evidence and residual risk before any production launch decision.

---

## 7. Decisions and next steps

| Decision | Proposed owner |
|---|---|
| Confirm whether medical-delivery fields create specific legal or contractual obligations. | Application Owner with Privacy/Legal Adviser |
| Approve courier enrollment, removal, and assignment rules. | Courier Program Owner and Application Owner |
| Select architecture and fund implementation and testing. | CIO/IT Director |
| Approve RTO/RPO and dispatch outage procedure. | CIO/IT Director and Dispatch Manager |
| Resolve or formally address material open risks. | COO |

**Portfolio conclusion:** This project demonstrates the path from a business requirement to an owned, testable cloud control. Implementation, operating evidence, and any compliance determination remain future work.
