# Security Finding Triage Procedure

**Control links:** CLD-07, CLD-08, CLD-10  
**Applies to:** Findings and material alerts affecting the proposed dispatch workload  
**Status:** Proposed procedure; response coverage and targets require approval

## 1. Intake

The designated security operator opens or updates a finding record with:

- Finding ID, source, detection time, review time, account/environment, and affected resource.
- Original severity and current triage severity.
- Related identity, delivery, integration, or data category, if known.
- Link to the underlying event without copying unnecessary sensitive data.

Use `templates/security-finding-record-template.md`.

## 2. Validate and assess

1. Confirm that the source and event are authentic and determine whether coverage is functioning.
2. Check for duplicates and related findings.
3. Determine whether activity is continuing, access is unauthorized, sensitive data may be involved, or dispatch is affected.
4. Assign **Critical**, **High**, **Moderate**, or **Low** under PLG's approved severity rules.
5. Record the reason for the classification and the immediate owner.

Do not close an alert as a false positive merely because its first explanation seems benign; document the checks performed.

## 3. Assign and act

- **Suspected active compromise, unauthorized data access, or material service disruption:** Contact the Incident Lead immediately and start `procedures/cloud-incident-response.md`.
- **High finding without confirmed incident:** Assign to the relevant owner during approved coverage and track investigation and remediation.
- **Moderate or Low finding:** Assign, set a due date under approved targets, and monitor for escalation.
- **Missing logging or detection coverage:** Open a control gap against CLD-07 even if there is no suspicious event.

The owner records containment or corrective steps, change approvals, and operational impact.

## 4. Verify and close

A finding closes only when the owner documents the cause and outcome, verifies the corrective action or approved disposition, and records the reviewer and date. Repeated findings feed the risk register and monthly trend report.

Preserve related evidence under the incident process if compromise is suspected. A finding queue entry alone does not prove an incident occurred.
