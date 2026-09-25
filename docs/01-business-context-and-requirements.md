# Business Context and Requirements

## Organization and workload

Peachtree Logistics Group (PLG) is a fictional Atlanta-based company with approximately 225 employees. Its services include warehousing, last-mile delivery, medical courier work, and freight brokerage across the Southeast.

PLG proposes moving its dispatch and delivery platform into AWS. Dispatchers assign work; employees and independent couriers receive assignments and submit status and proof-of-delivery updates. The platform exchanges selected information with existing systems, including an on-premises warehouse management system (WMS) and billing processes.

The proposal must support time-sensitive deliveries while giving PLG clearer control over access, data, security events, and recovery.

## Business requirements

| ID | Requirement | Proposed acceptance measure |
|---|---|---|
| BR-01 | Dispatchers can assign and monitor deliveries during operating hours. | Approved availability target and documented outage procedure. |
| BR-02 | Drivers and independent couriers see only work assigned to them. | Role tests demonstrate assignment-scoped access. |
| BR-03 | Sensitive customer and medical-delivery details receive appropriate protection. | Data inventory, access rules, encryption design, and reviewed retention decisions. |
| BR-04 | PLG can investigate administrative actions and material security events. | Required log sources, retention settings, alert routing, and a completed investigation exercise. |
| BR-05 | The service can recover from data loss or disruption. | Approved recovery time objective (RTO), recovery point objective (RPO), and successful restore exercise. |
| BR-06 | Changes and access remain accountable to named owners. | Approved change records and periodic access reviews. |
| BR-07 | Integration with existing WMS and billing processes is controlled. | Documented interfaces, authentication, allowed flows, and failure handling. |

## Business constraints

- Dispatch work cannot depend on a lengthy manual security approval for routine assignments.
- PLG has limited security staffing and must prioritize controls by risk.
- Independent couriers may use approved personal devices; device and application requirements need explicit decisions.
- Vendor-managed systems cannot be assumed to expose every desired log or control.
- Healthcare and payment obligations require validation against actual contracts, data flows, and legal advice before PLG could assert applicability or compliance.

## Success condition

The design succeeds as a portfolio case study when each priority requirement has a linked risk, architecture decision, accountable owner, planned test, and evidence source. It does not claim that BR-01 through BR-07 have been met in production.
