# Framework Crosswalk

**Purpose:** Show how PLG's proposed cloud controls support selected cybersecurity outcomes and AWS security design areas.

This is a **design-level crosswalk**, not an assertion of framework certification, complete coverage, or regulatory compliance. NIST Cybersecurity Framework (CSF) 2.0 outcomes are organized under six functions. A detailed subcategory mapping would require a separate review against the official CSF 2.0 Core and the final implementation.

| NIST CSF 2.0 function | PLG outcome | Related controls | AWS design area | Planned verification |
|---|---|---|---|---|
| Govern | Assign decision authority, cloud responsibility, risk ownership, and exceptions. | CLD-01, CLD-12 | Account governance and shared responsibility | Approved ownership matrix, risk decisions, and exception records |
| Identify | Know the workload, data, integrations, accounts, and material risks. | CLD-01, CLD-05, CLD-10, CLD-12 | Resource and data inventory | Inventory review and risk-register sample |
| Protect | Restrict access, network paths, data use, keys, secrets, and integrations. | CLD-02, CLD-03, CLD-04, CLD-05, CLD-06, CLD-09, CLD-10 | Identity, infrastructure, application, and data protection | Effective-permission review, negative authorization tests, and configuration samples |
| Detect | Capture required events and identify suspicious activity or missing coverage. | CLD-07, CLD-08, CLD-10 | Logging, configuration visibility, and detection | Generated-event test, coverage check, and finding record |
| Respond | Triage, contain, investigate, communicate, and track corrective action. | CLD-08, CLD-12 | Incident response | Tabletop or representative finding exercise |
| Recover | Restore data and service, validate results, and address recovery gaps. | CLD-11, CLD-12 | Backup and recovery | Timed restore exercise and reviewed corrective actions |

## Applying AWS guidance

The AWS Well-Architected Security Pillar and AWS Security Reference Architecture inform the proposed account, identity, logging, and data-protection choices. They do not replace PLG's business requirements or assign PLG's application authorization decisions to AWS.

The AWS shared responsibility model must be checked for the **specific services eventually selected**. Until PLG selects those services, this crosswalk identifies logical responsibilities rather than a service-by-service implementation.

## Traceability rule

A mapped control must point to:

1. A PLG risk or business requirement.
2. A documented design decision.
3. An accountable owner.
4. A test of the intended outcome.
5. A dated evidence source after implementation.

A diagram or policy alone is design evidence. It is not proof that the control operates effectively.

## Primary references

- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [AWS Well-Architected Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Security Reference Architecture](https://docs.aws.amazon.com/prescriptive-guidance/latest/security-reference-architecture/welcome.html)
- [AWS shared responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/)
