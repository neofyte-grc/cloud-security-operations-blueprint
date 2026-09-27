# Cloud Logging and Monitoring Standard

**Organization:** Peachtree Logistics Group (PLG), fictional  
**Applies to:** Proposed AWS dispatch workload and its approved integrations  
**Control links:** CLD-07, CLD-08, CLD-10  
**Status:** Proposed standard requiring PLG approval

## 1. Purpose

Make material activity and failures discoverable, reviewable, and available for authorized investigation.

## 2. Required logging decisions

Before launch, the Cloud Platform Lead and Application Owner must document:

- AWS accounts and Regions in scope.
- Administrative and resource events required for investigation.
- Any selected CloudTrail data events, with a cost and privacy review.
- Application sign-ins, authorization denials, assignment changes, and relevant sensitive-record access.
- Integration errors, retries, rejected transactions, and reconciliation gaps.
- Backup failures, monitoring failures, and significant availability events.
- Destination, access restrictions, retention period, and deletion authority for each log source.

CloudTrail data events require deliberate selection; enabling a trail alone does not capture them by default. If AWS Security Hub CSPM controls that depend on AWS Config are selected, PLG must configure the necessary resource recording and verify coverage.

## 3. Protection and review

1. Required logs must flow to a designated security destination with access separated from ordinary workload operation.
2. Changes that disable logging or alter retention must be authorized, recorded, and reviewed.
3. Logs must avoid unnecessary customer or medical-delivery payloads.
4. The owner must test delivery of a representative event from each required source.
5. Security/GRC must maintain a finding queue with severity, assignment, action, and closure records.
6. Missing sources, failed deliveries, and disabled detections must create an operational issue.

PLG proposes a monthly source-coverage review and daily review of High findings during defined support coverage. Active suspected compromise requires immediate escalation under the incident procedure. Actual support hours and response targets need approval.

## 4. Retention and evidence

The Privacy/Legal Adviser and business owner must approve retention based on applicable obligations and investigation needs. Do not invent a universal retention period. Evidence of operation includes dated event tests, configuration records, coverage checks, and reviewed finding records.

**Related procedure:** `procedures/security-finding-triage.md`.
