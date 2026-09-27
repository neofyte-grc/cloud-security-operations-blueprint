# Sample Restore Test

> **SIMULATED PORTFOLIO EXAMPLE.** The times, results, and environment below are invented to show how to document a failed recovery objective. No AWS backup or restore was performed.

**Test ID:** SIM-RT-001  
**Control:** CLD-11  
**Risk:** R-06 — dispatch data loss or prolonged outage  
**Scenario:** Hypothetical isolated restoration of synthetic dispatch records  
**Planning targets:** Four-hour RTO and one-hour RPO; these targets have not been approved by a real PLG business owner

| Measurement | Simulated result |
|---|---|
| Disruption time | 09:00 |
| Selected recovery point | 08:30 |
| Restore started | 09:20 |
| Data technically restored | 12:45 |
| Application operationally usable | 13:25 |
| Measured recovery time | 4 hours 25 minutes from disruption |
| Measured data loss | 30 minutes |
| Dispatch function validation | Synthetic assignment and status update worked in the exercise scenario |
| Authorization validation | Assigned and unassigned synthetic delivery tests included |
| Overall result | **Fail:** proposed four-hour RTO missed by 25 minutes |

## Finding and action

The fictional test indicates that data loss would fall within the proposed one-hour RPO, but operational recovery would miss the proposed four-hour RTO. A restored database alone was not counted as an operationally usable service.

**SIM-ACT-003:** Cloud Platform Lead and Application Owner to investigate the application-startup delay, revise the runbook, and plan a retest. The CIO/IT Director and Dispatch Manager would review the operational impact before relying on the proposed target.

This record is an illustration of honest test reporting. It must not be described as a completed AWS restore exercise.
