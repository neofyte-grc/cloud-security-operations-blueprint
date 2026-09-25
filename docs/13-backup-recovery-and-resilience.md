# Backup, Recovery, and Resilience

## Business decision required

The CIO/IT Director and Dispatch Manager must approve a **recovery time objective (RTO)** and **recovery point objective (RPO)** for dispatch. An RTO is the maximum targeted time to restore the service; an RPO is the maximum targeted amount of data loss measured in time.

For design exercises, PLG proposes **RTO: 4 hours** and **RPO: 1 hour**. These are hypothetical targets pending business approval and feasibility testing. They are not achieved results.

## Proposed recovery design

| Area | Requirement |
|---|---|
| Backup scope | Identify application data, configuration, dependencies, and required records. |
| Frequency | Choose schedules capable of supporting the approved RPO. |
| Protection | Restrict deletion and access; document encryption and retention. |
| Separation | Consider a backup boundary that a compromised workload operator cannot readily alter. |
| Restore | Document the order for restoring data, application, identities, integrations, and validation. |
| Dispatch fallback | Define how assignments are handled during an outage and reconciled afterward. |
| Testing | Restore into an isolated test environment and measure elapsed time and data completeness. |

A successful backup job is not a successful recovery test. PLG must verify that restored data is usable and that the end-to-end workflow works.

## Proposed exercise

At least twice yearly, the Cloud Platform Lead initiates a controlled restore test; the Application Owner validates functions; the Dispatch Manager validates operational usefulness. Record test conditions, start/end times, estimated data loss, defects, and corrective actions. Frequency is a proposed PLG policy decision.

If testing misses the approved target, the owner records a gap under [residual risk and exceptions](17-residual-risk-and-exceptions.md). This work addresses R-06 through `CLD-11` and is detailed in `procedures/backup-restore-test.md`.
