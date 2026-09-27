# Backup and Restore Test Procedure

**Control links:** CLD-11, CLD-12  
**Applies to:** Required data and dependencies of the proposed AWS dispatch workload  
**Status:** Proposed procedure; run only after architecture, targets, and safe test environment are approved

## 1. Preconditions

The CIO/IT Director and Dispatch Manager approve the workload's recovery time objective (RTO) and recovery point objective (RPO). The Project 4 design uses **four hours RTO** and **one hour RPO** only as hypothetical planning targets until approved.

The Cloud Platform Lead identifies the backup source, selected recovery point, isolated destination, dependencies, authorized testers, and rollback/cleanup plan. The Application Owner defines functional checks; the Dispatch Manager defines operational checks.

A successful backup job is a prerequisite, not proof of recoverability.

## 2. Execute the test

1. Record the test ID, date, environment, participants, approved targets, and selected recovery point.
2. Record the simulated disruption time and test start time.
3. Restore the required data and application components into an isolated environment.
4. Validate integrity, access restrictions, critical dispatch functions, and approved integrations or safe substitutes.
5. Confirm that logging and monitoring function in the restored environment.
6. Measure time to an operationally usable service and the age of the restored data.
7. Record failures, manual workarounds, security issues, and cleanup.

Do not connect a test restoration to live customer or billing workflows without an approved isolation design.

## 3. Evaluate

The Application Owner and Dispatch Manager sign off on functional and operational results. The Cloud Platform Lead compares measured time and data loss with the **approved** RTO/RPO. Record **Pass**, **Fail**, or **Not performed**, with reasons.

A completed restore job is not a Pass if the application cannot safely process deliveries or if the approved objective was missed.

## 4. Follow-up

Assign each defect an owner and due date. If an approved recovery target is missed, escalate to the CIO/IT Director and Dispatch Manager, update R-06, and follow the exception process if operations will proceed before remediation. Retest the failed capability after correction.

Use `templates/restore-test-record-template.md`. The proposed cadence is at least twice yearly and after a material recovery-design change.
