# Sample Security Finding

> **SIMULATED PORTFOLIO EXAMPLE.** This is an invented application event in a hypothetical nonproduction environment. It is not an AWS finding or an actual incident.

**Finding ID:** SIM-FND-001  
**Control links:** CLD-03, CLD-08  
**Risk:** R-02 — cross-courier access  
**Source:** Simulated dispatch-application authorization test  
**Environment:** Hypothetical nonproduction environment using synthetic deliveries  
**Initial severity:** High for exercise purposes  
**Status:** Escalated for investigation; not closed

## Event

During an invented test, courier identity COU-202 requested delivery TEST-900, which was assigned to courier COU-204. The simulated response appeared to include delivery details.

This observation would require immediate validation. The record does not establish that a production data disclosure occurred.

## Triage record

| Field | Simulated entry |
|---|---|
| Detection | Authorization test identified an unexpected response. |
| Verification needed | Confirm response contents, role, assignment state, and whether the test environment had the expected code version. |
| Potential impact | Unauthorized view of another courier's synthetic delivery record. |
| Assigned owner | Application Owner. |
| Escalation | Security/GRC Lead and Incident Lead for a scenario exercise. |
| Immediate proposed action | Stop the test path, preserve logs, and prevent release until authorization is corrected and retested. |
| Related action | SIM-ACT-002 — inspect server-side assignment check and add a negative regression test. |

## Closure requirements

The Application Owner would document the cause, correct the rule, rerun both allowed and denied access tests, and have Security/GRC review the result. The finding remains **Open** in this sample because no remediation or retest is represented.

Do not copy personal, medical, or customer data into a real finding record when a restricted evidence reference will suffice.
