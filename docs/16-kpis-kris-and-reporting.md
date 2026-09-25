# KPIs, KRIs, and Reporting

## Measurement principles

Measures should help PLG make a decision. Each requires a defined population, calculation, owner, reporting period, and data source. Targets below are **proposed thresholds for discussion**, not achieved performance.

| Measure | Calculation | Proposed review | Owner |
|---|---|---|---|
| Privileged access review completion | Reviewed privileged identities ÷ in-scope privileged identities × 100 | Monthly | IT Director |
| Courier removal timeliness | Removed within approved time target ÷ couriers whose eligibility ended × 100 | Monthly | Courier Program Owner |
| Negative authorization test pass rate | Denied cross-assignment tests ÷ executed cross-assignment tests × 100 | Each release | Application Owner |
| Required log coverage | Sources producing expected test events ÷ required sources × 100 | Monthly | Security/GRC Lead |
| High finding triage timeliness | High findings triaged within approved target ÷ High findings received × 100 | Monthly | Security/GRC Lead |
| Backup job success rate | Successful scheduled jobs ÷ scheduled jobs × 100 | Monthly | Cloud Platform Lead |
| Recovery objective test result | Measured restoration time and measured data loss against approved RTO/RPO | Each exercise | CIO/IT Director |
| Overdue High risk actions | Count of High risk actions past their approved due dates | Monthly | Security/GRC Lead |

The first, third, fourth, fifth, and sixth measures are primarily **KPIs** for control execution. Delayed removals, missed recovery targets, and overdue High risk actions also act as **KRIs** when they signal increasing exposure.

## Reporting cadence

- **Operational owners:** Review failures and exceptions as they arise.
- **Security/GRC Lead:** Produce a monthly summary with trends, denominators, failed tests, and action owners.
- **CIO/IT Director and COO:** Review material risks, recovery gaps, and overdue decisions at least quarterly.

A reported percentage must include its denominator. For example, “100% of one tested event source” must not be described as complete coverage of all required sources.

The first reporting cycle establishes a baseline; targets are revised after PLG measures actual workload behavior.
