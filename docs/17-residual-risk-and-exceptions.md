# Residual Risk and Exceptions

## Residual risk

Residual risk is the exposure remaining after a control has been implemented and its effectiveness assessed. In this design-only case study, **all residual ratings are provisional**. The initial scores are in [the risk assessment](05-cloud-risk-assessment.md).

## Exception process

1. The requester identifies the affected requirement and `CLD` control.
2. The operating owner describes the deviation and affected systems/data.
3. Security/GRC evaluates the associated `R` risks and proposed compensating measures.
4. The accountable business decision-maker approves or rejects a time-bound exception.
5. An owner tracks remediation and the expiry date.
6. The exception is rechecked at expiry or after a material change.

| Field | Required entry |
|---|---|
| Exception ID | Unique identifier |
| Control and risk | Applicable `CLD` and `R` IDs |
| Reason and scope | Exact deviation, accounts, users, and data |
| Exposure | Likelihood, impact, and operational consequences |
| Temporary measures | What reduces risk during the exception |
| Owner and approver | Named people and approval date |
| Expiry and action | Date, remediation step, and verification method |

## Illustrative decision

If the first restore exercise exceeds the proposed four-hour RTO, CLD-11 has **not passed**. The Cloud Platform Lead records the measured time and cause. The Dispatch Manager assesses delivery impact. The CIO proposes improvements and a retest date. The COO decides whether operations may proceed under a documented, time-bound risk acceptance.

An exception does not waive an applicable legal or contractual requirement. Privacy/Legal must review any such issue before a decision is represented as permissible.

## Closure

Close an exception only after the operating owner provides evidence that the deviation is resolved and Security/GRC verifies the result. Retain the original decision and the closure record.
