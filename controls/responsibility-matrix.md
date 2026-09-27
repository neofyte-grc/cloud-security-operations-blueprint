# Cloud Responsibility Matrix

**Workload:** Proposed PLG dispatch and delivery platform in AWS  
**Status:** Proposed role assignments; PLG must name individuals before implementation

## Role definitions

- **A — Accountable:** Approves the result and owns the decision. One accountable role is assigned per activity.
- **R — Responsible:** Performs the activity and produces the record.
- **C — Consulted:** Provides input before a material decision.
- **I — Informed:** Receives the outcome.

One person may fill multiple roles, but the accountable role must remain explicit. AWS responsibilities depend on the services selected and are assessed separately under the AWS shared responsibility model.

| Activity / control | A | R | C | I |
|---|---|---|---|---|
| Account baseline and separation — CLD-01 | CIO/IT Director | Cloud Platform Lead | Security/GRC Lead | COO |
| Workforce and privileged access — CLD-02 | IT Director | Cloud Platform Lead | HR Manager, Security/GRC Lead | Application Owner |
| Application role and assignment access — CLD-03 | Application Owner | Application team | Dispatch Manager, Courier Program Owner | Security/GRC Lead |
| Network paths and entry points — CLD-04 | Cloud Platform Lead | Platform team | Application Owner, Security/GRC Lead | CIO/IT Director |
| Data classification and handling — CLD-05 | Application Owner | Application team | Privacy/Legal Adviser, Dispatch Manager | Security/GRC Lead |
| Keys and secrets — CLD-06 | Cloud Platform Lead | Platform team | Application Owner | Security/GRC Lead |
| Required logs and coverage — CLD-07 | Cloud Platform Lead | Platform and application teams | Security/GRC Lead | CIO/IT Director |
| Finding triage and incident coordination — CLD-08 | Security/GRC Lead | Designated security operator or Incident Lead | Platform and application owners | CIO/IT Director |
| Employee access removal and review — CLD-09 | IT Director | Identity administrator | HR Manager | Security/GRC Lead |
| Courier access removal and review — CLD-09 | Courier Program Owner | Courier access administrator | Application Owner | Security/GRC Lead |
| WMS and billing integrations — CLD-10 | Application Owner | Application team | Warehouse Operations Manager, Finance Owner | Security/GRC Lead |
| Backup and restore testing — CLD-11 | CIO/IT Director | Cloud Platform Lead | Application Owner, Dispatch Manager | COO |
| Risk, evidence, and exception oversight — CLD-12 | CIO/IT Director | Security/GRC Lead | Control owners | COO |
| Acceptance of material residual risk | COO | CIO/IT Director | Security/GRC Lead, affected business owner | Relevant control owners |

## Escalation

- A suspected active compromise goes to the Incident Lead and Security/GRC Lead immediately under the incident procedure.
- A failed control test goes to its accountable owner and Security/GRC Lead for correction and retesting.
- A recovery test that misses an approved objective goes to the CIO/IT Director and Dispatch Manager for an operational impact decision.
- A material residual risk requiring acceptance goes to the COO with an expiry date and remediation plan.

## Prelaunch check

For each activity, record the named individual, backup contact, and communication channel. An unfilled role is an open implementation gap, not an implied assignment to Security/GRC.
