# Logging, Detection, and Monitoring

## Monitoring objective

PLG must be able to identify material access, configuration, application, and availability events and assign findings to an owner who can act on them.

## Proposed sources

| Source | Events to consider | Primary reviewer |
|---|---|---|
| AWS activity logging | Administrative and selected resource actions | Security/GRC Lead |
| AWS configuration recording | Changes to covered resources and rules | Cloud Platform Lead |
| Threat detection findings | Supported suspicious activity | Security/GRC Lead |
| Application audit log | Sign-ins, assignment changes, denied access, and sensitive record access where appropriate | Application Owner |
| Integration monitoring | Failures, retries, rejected messages, and reconciliation gaps | Application Owner |
| Availability and backup monitoring | Service health, backup failures, and restore-test outcomes | Cloud Platform Lead |

An AWS activity trail must be configured for the intended account and Region coverage. **CloudTrail data events require deliberate selection; they are not automatically captured by a new trail.** Log design must also consider cost, sensitive content, retention, and access.

## Alert workflow

1. A source generates an event or finding.
2. The monitoring process records severity, affected resource, and time.
3. Security or the designated operator checks validity and business impact.
4. The operator assigns the finding and records action and escalation.
5. The owner verifies resolution and closes the record.
6. A recurring issue feeds risk review or a design change.

A finding aggregator is not a substitute for assigning people to review and respond. Coverage checks should detect disabled sources or missing expected events.

## Proposed operating targets

PLG proposes daily review of high-severity findings during defined support coverage, immediate escalation of suspected active compromise, and a monthly check of log coverage and access. These are **design targets**, not measured performance commitments.

The detailed workflow belongs in `procedures/security-finding-triage.md`. This design addresses R-04 through `CLD-07` and `CLD-08`.
