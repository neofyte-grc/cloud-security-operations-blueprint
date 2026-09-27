# Sample Control Evidence Index

**Status: SIMULATED PORTFOLIO EXAMPLE — not evidence from a live AWS environment.**

This index demonstrates how PLG would organize control evidence after implementation. Entries marked **Example** refer to invented records. Entries marked **Planned** have no test result.

| Control | Evidence item | Period/environment | Status | Result | Owner/reviewer |
|---|---|---|---|---|---|
| CLD-02, CLD-09 | `sample-access-review.md` | Simulated quarterly dispatch-application review | Example | Incomplete: one removal remains open | IT Director / Security/GRC Lead |
| CLD-07, CLD-08 | `sample-security-finding.md` | Simulated nonproduction event | Example | Escalated for authorization investigation | Security/GRC Lead / Application Owner |
| CLD-11 | `sample-restore-test.md` | Simulated isolated restore exercise | Example | Fail: proposed RTO missed | Cloud Platform Lead / CIO/IT Director |
| CLD-01 | Account inventory and baseline approval | Future production/nonproduction accounts | Planned | Not performed | Cloud Platform Lead |
| CLD-03 | Assigned/unassigned delivery authorization test | Future application test environment | Planned | Not performed | Application Owner |
| CLD-04 | Network-rule review | Future AWS implementation | Planned | Not performed | Cloud Platform Lead |
| CLD-05, CLD-06 | Data, key, and secret configuration review | Future AWS implementation | Planned | Not performed | Application Owner / Cloud Platform Lead |
| CLD-10 | Integration failure and reconciliation test | Future integration test environment | Planned | Not performed | Application Owner |
| CLD-12 | Approved risk and exception review | Future operating period | Planned | Not performed | CIO/IT Director |

## Minimum real-evidence metadata

When PLG implements a control, each evidence item should include its control ID, source system, account or environment, collection date, review period, collector, reviewer, test method, outcome, and corrective-action reference. Sensitive records require restricted storage and redaction before any portfolio use.

**Interpretation:** The three example records illustrate documentation quality and decision handling. None establishes a production control outcome.
