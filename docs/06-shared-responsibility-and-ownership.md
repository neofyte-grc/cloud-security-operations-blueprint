# Shared Responsibility and Ownership

## Operating principle

AWS manages security **of** its cloud infrastructure. PLG remains responsible for the workload configuration, identities, application behavior, data decisions, and its own operating processes, subject to the services selected. The exact division must be confirmed against AWS documentation for each selected service.

A managed AWS service reduces some infrastructure tasks; it does not perform PLG's assignment-level authorization, access approvals, incident decisions, or recovery validation.

## PLG responsibility matrix

| Activity | Accountable PLG role | Supporting roles | Required record |
|---|---|---|---|
| Approve workload and recovery requirements | CIO/IT Director | COO, Dispatch Manager | Approved requirements |
| Maintain AWS account baseline | Cloud Platform Lead | Security/GRC Lead | Baseline review |
| Provision workforce access | IT Director | HR Manager, Cloud Platform Lead | Access request and approval |
| Enroll/remove courier access | Courier Program Owner | Application Owner | Enrollment/removal record |
| Enforce application authorization | Application Owner | Development team | Role tests and release record |
| Classify data and approve retention | Application Owner | Privacy/Legal Adviser | Data inventory and decision |
| Review alerts and coordinate triage | Security/GRC Lead | Platform and application owners | Finding record |
| Declare and coordinate incidents | Incident Lead | Relevant owners | Incident record |
| Execute backup and restore tests | Cloud Platform Lead | Application Owner, Dispatch Manager | Restore-test record |
| Approve material residual risk | COO | CIO/IT Director, Security/GRC Lead | Time-bound acceptance |

The Security/GRC Lead may coordinate and challenge decisions, but the operational owner executes the control and supplies evidence.

## Third-party responsibilities

For each connected vendor or service, record the contracted service, available security documentation, incident notification terms, data handling, logging capabilities, and PLG's fallback procedure. A vendor assurance review does not replace PLG's responsibility for its own integration settings.

## Decision gate

Before deployment, `controls/responsibility-matrix.md` must assign a named accountable person, an operator, and an escalation contact to every `CLD` control. Unassigned controls remain open implementation risks.
