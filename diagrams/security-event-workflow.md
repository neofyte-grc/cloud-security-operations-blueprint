# Security Event Workflow

**Status:** Proposed operating workflow, not an executed incident history.

```mermaid
flowchart TB
    Source["AWS, application, or integration event"]
    Queue["Protected monitoring and finding queue"]
    Triage["Security operator triages"]
    Decision{"Suspected incident?"}
    Incident["Incident Lead coordinates response"]
    Owner["Control owner corrects and verifies"]
    Record["Reviewed closure and risk update"]

    Source --> Queue
    Queue --> Triage
    Triage --> Decision
    Decision -->|"Yes"| Incident
    Decision -->|"No: assigned finding"| Owner
    Incident --> Owner
    Owner --> Record
```

## Operating notes

The operator records source, time, affected environment, severity, owner, and validation steps. A suspected active compromise or material disruption is escalated under `procedures/cloud-incident-response.md`. Other findings remain assigned and tracked under `procedures/security-finding-triage.md`.

Closing a finding requires a documented disposition and verification. Missing expected logs are themselves a control gap under CLD-07. A queue or detection service does not replace staffed review and business decisions.

Control connections: CLD-07, CLD-08, and CLD-12.
