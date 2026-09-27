# Cloud Access Standard

**Organization:** Peachtree Logistics Group (PLG), fictional  
**Applies to:** Proposed AWS dispatch workload, supporting administrators, employees, drivers, independent couriers, and integrations  
**Control links:** CLD-02, CLD-03, CLD-09  
**Status:** Proposed standard requiring PLG approval

## 1. Purpose

Ensure that each person and integration receives only the access needed for an approved task and that access ends when the need ends.

## 2. Requirements

### Workforce and AWS administration

1. AWS administrative access must use individual identities, approved roles, and strong authentication.
2. PLG should use workforce federation and temporary AWS credentials for routine human access.
3. Privileged roles must be limited to named duties; routine dispatch users must not receive AWS administrator access.
4. Production access requires an owner-approved request, stated business purpose, and recorded grant.
5. Emergency elevation must be time-limited, logged, and reviewed after use.
6. Shared human accounts are prohibited for routine administration.

### Application users

1. The application must authorize access on the server for each requested delivery or action.
2. Drivers and couriers may access only deliveries currently assigned to them and the minimum data needed to perform their tasks.
3. Dispatcher permissions must be limited to approved operational scope.
4. A change in assignment must cause authorization to be reevaluated; a previously issued link or known record identifier must not grant continuing access.

### Integrations

1. Each integration must have a dedicated nonhuman identity with only necessary permissions.
2. Credentials and secrets must be stored and replaced under the data-protection standard.
3. Integration access must be removed when the interface is retired.

## 3. Lifecycle and reviews

HR supplies employee status changes; the Courier Program Owner supplies courier eligibility changes. The designated administrator records grants, changes, and removals. Access removal targets must be approved before launch.

As proposed PLG frequencies, privileged access is reviewed monthly and other active access at least quarterly. Reviewers must record the population, decisions, removals, and completion date.

## 4. Exceptions and verification

An exception requires the process in `templates/exception-request-template.md`, approval, an expiry date, and compensating measures. Security/GRC verifies review records and samples effective access. Authorization changes require positive and negative tests before release.

**Related procedure:** `procedures/access-provisioning-and-review.md`.
