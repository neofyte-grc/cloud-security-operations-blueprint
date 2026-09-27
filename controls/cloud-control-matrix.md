# Cloud Control Matrix

**Organization:** Peachtree Logistics Group (PLG), fictional  
**Workload:** Proposed AWS-hosted dispatch and delivery platform  
**Status:** Proposed controls; implementation and operating effectiveness have not been verified

## How to use this matrix

The control owner approves the design and remains accountable for operation. The operator performs the work. Security/GRC reviews test results and evidence. An implementation status of **Proposed** must not be reported as **Operating**.

| ID | Control objective and proposed activity | Risks | Accountable owner | Proposed frequency or trigger | Test and expected evidence |
|---|---|---|---|---|---|
| CLD-01 | Maintain approved AWS account boundaries, owners, Regions, and baseline settings; separate production from nonproduction. | R-03, R-05 | Cloud Platform Lead | At account creation; quarterly review; material change | Compare account inventory and settings with approved design; retain inventory, baseline approval, and change record. |
| CLD-02 | Use individual, role-based workforce access with strong authentication and temporary AWS credentials; limit and review privileged permissions. | R-01, R-08 | IT Director | At grant/change/removal; privileged review monthly | Sample approved grants and effective permissions; retain role/assignment export, approvals, and review record. |
| CLD-03 | Enforce application roles and assignment-level authorization for dispatchers, drivers, and couriers. | R-02 | Application Owner | Every relevant release; after authorization change | Run allowed and denied access tests, including altered delivery identifiers; retain test results and release approval. |
| CLD-04 | Restrict public entry, component communication, and network paths to documented business flows. | R-03, R-07 | Cloud Platform Lead | At change; quarterly rule review | Compare deployed rules and exposed endpoints with approved flows; retain configuration export and review. |
| CLD-05 | Classify, minimize, encrypt, retain, and restrict customer and delivery information according to approved decisions. | R-02, R-05 | Application Owner | At new data flow; annual classification review | Inspect data inventory, role access, encryption settings, and retention decisions; retain approved records. |
| CLD-06 | Inventory keys and secrets; limit their administration and use; rotate or replace them under an approved process. | R-05 | Cloud Platform Lead | At creation/change; periodic access review; compromise response | Sample key/secret permissions and a rotation or replacement record; retain configuration and validation evidence. |
| CLD-07 | Capture required AWS and application events, protect their destination, and verify source coverage. | R-04 | Cloud Platform Lead | Continuous capture; monthly coverage check | Generate representative events and confirm receipt, access restrictions, and retention settings; retain event and coverage records. |
| CLD-08 | Assign, triage, escalate, and resolve security findings and suspected incidents. | R-01, R-03, R-04 | Security/GRC Lead | On finding; monthly trend review; scheduled exercise | Walk a representative finding through the workflow; retain finding record and exercise results. |
| CLD-09 | Remove employee and courier access when eligibility ends and review remaining access. | R-08 | IT Director and Courier Program Owner for their respective populations | On status change; quarterly nonprivileged review | Sample departure triggers against access removal and review records. |
| CLD-10 | Authenticate and limit WMS and billing integrations; detect failures and reconcile retried or missing transactions. | R-03, R-07 | Application Owner | At release/change; daily operational exception review | Test allowed/denied exchanges, failures, retries, and reconciliation; retain test and exception records. |
| CLD-11 | Protect required backups and validate recovery against business-approved RTO/RPO. | R-06 | Cloud Platform Lead | Scheduled backups; restore exercise at least twice yearly | Restore into an isolated environment; record elapsed time, data completeness, application validation, and defects. |
| CLD-12 | Maintain risk decisions, ownership, control tests, exceptions, corrective actions, and management reporting. | R-01–R-08 | CIO/IT Director | Monthly action review; quarterly risk review; material change | Sample register entries and overdue actions; retain approvals, test index, minutes, and exception records. |

## Status and result fields

For each control, track these fields in the working register:

- **Implementation status:** Proposed, In progress, Implemented, or Retired.
- **Test result:** Pass, Fail, or Not performed.
- **Last test and next review:** Dates and test period.
- **Evidence reference:** Location, collector, reviewer, and collection date.
- **Gap:** Finding, remediation owner, due date, and exception ID if applicable.

`Implemented` describes a configuration or process being put in place. `Pass` requires a completed test with reviewable evidence. One does not imply the other.

## Launch review

Before launch, the CIO/IT Director reviews failed tests and open High risks with the Application Owner, Cloud Platform Lead, Dispatch Manager, and Security/GRC Lead. A material unresolved risk needs remediation or a documented, time-bound decision by the COO. An accepted risk is still recorded as an open exposure.
