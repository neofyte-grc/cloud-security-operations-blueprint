# Control Implementation Roadmap

## Purpose

Sequence the proposed controls so prerequisites are in place before PLG relies on the dispatch workload. This is a planning sequence, not a claim that any milestone has been completed.

| Stage | Controls | Work | Exit criterion |
|---|---|---|---|
| 1. Decisions and baseline | CLD-01, CLD-12 | Approve requirements, scope, account owners, data decisions, and risk ownership. | Design and owners approved. |
| 2. Identity and boundaries | CLD-02, CLD-03, CLD-04 | Establish privileged access, courier authorization, and permitted network paths. | Positive and negative access tests pass. |
| 3. Data and integrations | CLD-05, CLD-06, CLD-10 | Protect data, keys, secrets, and WMS/billing interfaces. | Configuration and integration tests pass. |
| 4. Visibility and response | CLD-07, CLD-08, CLD-09 | Enable required logging, finding workflow, lifecycle reviews, and response path. | Coverage checks and tabletop are recorded. |
| 5. Recovery and assurance | CLD-11, CLD-12 | Test restore, inspect evidence, and resolve launch gaps. | Business owner reviews measured results and residual risk. |

## Control catalogue

| ID | Control objective |
|---|---|
| CLD-01 | Govern accounts and separate environments. |
| CLD-02 | Restrict and review privileged/workforce access. |
| CLD-03 | Enforce application role and assignment authorization. |
| CLD-04 | Restrict network and application entry paths. |
| CLD-05 | Classify, minimize, retain, and protect data. |
| CLD-06 | Govern keys and secrets. |
| CLD-07 | Capture and protect required logs. |
| CLD-08 | Triage findings and coordinate incidents. |
| CLD-09 | Remove and periodically review access. |
| CLD-10 | Secure and reconcile integrations. |
| CLD-11 | Back up and test recovery. |
| CLD-12 | Maintain governance, tests, evidence, and exceptions. |

## Launch gate

The CIO/IT Director determines readiness after the Application Owner, Cloud Platform Lead, Dispatch Manager, and Security/GRC Lead review failed tests and open High risks. A material unresolved risk needs a documented remediation plan or time-bound acceptance by the COO; acceptance cannot convert a failed test into a pass.

Detailed implementation owners, dates, dependencies, and statuses will be tracked in `controls/cloud-control-matrix.md`.
