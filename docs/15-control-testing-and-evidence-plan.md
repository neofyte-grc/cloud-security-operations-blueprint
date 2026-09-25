# Control Testing and Evidence Plan

## Assurance approach

Every control needs a test of its intended outcome and a record that can be traced to the correct environment and review period. Planned evidence is not actual evidence. Simulated examples in this repository must be labeled as such.

| Control | Representative test | Expected evidence |
|---|---|---|
| CLD-01 | Inspect account boundaries and approved baseline. | Account inventory and baseline approval. |
| CLD-02 | Sample privileged identities and effective permissions. | Role export, approvals, access-review record. |
| CLD-03 | Attempt assigned and unassigned delivery access. | Test cases and results, including denied requests. |
| CLD-04 | Compare allowed traffic with approved flows. | Rule export and reviewed flow list. |
| CLD-05 | Inspect data classification, storage protection, and retention. | Data inventory and configuration evidence. |
| CLD-06 | Sample key and secret access and rotation. | Access settings and rotation record. |
| CLD-07 | Generate a representative event and confirm delivery to protected logs. | Event, destination record, coverage review. |
| CLD-08 | Walk a finding through assignment and escalation. | Finding record and tabletop results. |
| CLD-09 | Sample a departed user and courier; check removal timing. | Status trigger and removal evidence. |
| CLD-10 | Test integration authentication, failure, and reconciliation. | Interface tests and exception record. |
| CLD-11 | Restore data and application into an isolated environment. | Timed restore-test record and validation. |
| CLD-12 | Inspect risk decisions, exceptions, and overdue actions. | Approved register and review minutes. |

## Evidence attributes

For each item record: control ID, environment, account or system, source, collection date, review period, collector, reviewer, outcome, and any sensitive-data handling restriction. A screenshot without context or an owner is weak evidence.

## Test outcome rules

Mark a test **Pass**, **Fail**, or **Not performed**. Record deviations and corrective actions; do not mark a proposed configuration as Pass. The Security/GRC Lead checks completeness, while the operating owner supplies the underlying records.

`evidence/sample-control-evidence-index.md` will show the format using fictional, clearly labeled entries.
