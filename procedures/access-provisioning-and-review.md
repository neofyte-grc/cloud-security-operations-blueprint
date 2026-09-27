# Access Provisioning and Review Procedure

**Control links:** CLD-02, CLD-03, CLD-09  
**Applies to:** Proposed AWS administration and dispatch application access  
**Status:** Proposed procedure; test with the selected identity and application systems before use

## 1. Provision access

1. **Receive request.** Record requester, individual identity, employment or courier status, role sought, business reason, environment, and required start/end dates.
2. **Verify eligibility.** HR confirms employee status; the Courier Program Owner confirms courier eligibility. Integration owners confirm the system purpose for nonhuman access.
3. **Approve.** The relevant access owner approves the least-privilege role. The requester may not self-approve.
4. **Grant.** The designated administrator assigns the approved AWS role or application role. Record who made the change and when.
5. **Validate.** Confirm the user can perform the approved task and cannot perform a representative unapproved task.
6. **Notify and record.** Store the approval, effective permission, validation result, and expiry if applicable.

AWS administrative and dispatch application grants are recorded separately.

## 2. Change or remove access

1. HR or the Courier Program Owner sends a documented status or assignment change.
2. The administrator identifies all relevant AWS, application, and integration permissions.
3. The administrator changes or removes access under PLG's approved timing target.
4. A second reviewer verifies removal for privileged access or a material termination.
5. Record trigger time, action time, affected roles, reviewer, and unresolved access.
6. Escalate failed or delayed removal to the accountable owner and Security/GRC Lead.

A courier's completed assignment must no longer grant access to another or expired assignment. Test this behavior in the application.

## 3. Periodic review

1. Export the complete in-scope identity and role population, including inactive and privileged identities.
2. Give the population and last-use/context data to the designated reviewer.
3. Require a decision of **retain**, **modify**, or **remove** for each entry.
4. Apply approved changes and verify completion.
5. Record reviewer, period, population, decisions, completion date, and exceptions.

Proposed cadence: monthly for privileged access and quarterly for other active access. The review is incomplete if decisions are recorded but removals are not executed.

## 4. Evidence and escalation

Use `templates/access-review-template.md` for reviews. Send missing approval, unexpected privilege, or overdue removal to the IT Director or Courier Program Owner and Security/GRC Lead. Suspected misuse follows `procedures/cloud-incident-response.md`.
