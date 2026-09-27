# Restore Test Record Template

**Control links:** CLD-11, CLD-12  
**Use:** Record an isolated restoration of the dispatch workload or a defined component.

## Test authorization

| Field | Entry |
|---|---|
| Test ID and date | |
| Test environment and isolation method | |
| Cloud Platform Lead | |
| Application Owner | |
| Dispatch Manager | |
| Test approver | |
| Resources and dependencies in scope | |
| Selected backup/recovery point | |
| Approved RTO and RPO | |
| Cleanup and rollback plan | |

## Timing and validation

| Field | Entry |
|---|---|
| Simulated disruption time | |
| Restore start time | |
| Technically restored time | |
| Operationally usable time | |
| Measured recovery time | |
| Latest transaction expected | |
| Latest transaction recovered | |
| Measured data loss in time | |
| Data integrity check and result | |
| Authentication and authorization check | |
| Dispatch function check | |
| Integration or safe substitute check | |
| Logging and monitoring check | |

## Result

| Field | Entry |
|---|---|
| RTO met? | |
| RPO met? | |
| Overall result: Pass, Fail, Not performed | |
| Defects and business impact | |
| Corrective action owner and due date | |
| Retest date | |
| Evidence references | |
| Application Owner sign-off | |
| Dispatch Manager sign-off | |
| CIO/IT Director review | |

A backup job marked successful does not establish that the application is usable or that recovery objectives were met. Do not connect test systems to live dispatch or billing workflows without an approved isolation design.
