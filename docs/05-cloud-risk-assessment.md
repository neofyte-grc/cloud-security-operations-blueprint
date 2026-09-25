# Cloud Risk Assessment

## Method

This is a **scenario-based assessment**, not a claim about PLG's actual security posture. Likelihood and impact each use a 1–5 scale. The initial score is likelihood × impact. Scores of 1–5 are Low, 6–12 Moderate, and 15–25 High. A score of 13 or 14 is also treated as High for prioritization. The business owner validates ratings before implementation.

Residual ratings remain **provisional** until controls are implemented and tested.

## Risk register

| ID | Risk scenario | L | I | Initial | Proposed response | Owner |
|---|---|---:|---:|---:|---|---|
| R-01 | Stolen workforce credentials enable unauthorized dispatch or AWS access. | 4 | 4 | 16 High | Strong authentication, scoped roles, review, detection | IT Director |
| R-02 | A courier sees another courier's customer or medical-delivery details. | 4 | 5 | 20 High | Assignment-level authorization, negative tests, rapid offboarding | Application Owner |
| R-03 | An exposed application or integration leaks or alters delivery records. | 3 | 5 | 15 High | Controlled entry, input validation, restricted paths, testing | Application Owner |
| R-04 | Incomplete or changeable logs prevent timely investigation. | 4 | 4 | 16 High | Defined log coverage, protected destination, alert review | Security/GRC Lead |
| R-05 | Misconfigured data storage or keys disclose sensitive records. | 3 | 5 | 15 High | Classification, encryption, restricted access, configuration checks | Cloud Platform Lead |
| R-06 | Data loss or prolonged outage disrupts dispatch. | 4 | 4 | 16 High | Approved RTO/RPO, backups, restore tests, outage procedure | CIO/IT Director |
| R-07 | WMS or billing integration grants excessive access or fails silently. | 3 | 4 | 12 Moderate | Dedicated identities, minimum data, monitoring and reconciliation | Application Owner |
| R-08 | A departing employee or courier retains access. | 4 | 4 | 16 High | Lifecycle triggers, removal targets, access reviews | HR/Courier Program Owners |

## Prioritization

First address R-02, R-01, R-04, and R-06 because unauthorized access, poor investigation coverage, and service disruption directly affect delivery operations. R-03 and R-05 remain launch-critical even if their estimated likelihood is lower.

The mapped controls are `CLD-01` through `CLD-12`. The detailed control-to-risk mapping will be recorded in `controls/cloud-control-matrix.md`.

## Reassessment triggers

Reassess when PLG changes its data types, identity model, courier process, architecture, integration, incident history, or recovery targets. Do not lower a residual score solely because a control appears in a design document.
