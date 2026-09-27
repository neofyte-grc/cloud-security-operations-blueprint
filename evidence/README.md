# Sample Evidence

This folder contains **fictional, simulated examples** showing what evidence for the proposed PLG controls might look like. PLG does not exist as an operating company in this case study, and these records are not exports from a live AWS environment.

## Files

| File | Illustrative purpose |
|---|---|
| `sample-control-evidence-index.md` | Connect selected controls to evidence requirements and example records. |
| `sample-access-review.md` | Show review decisions and an unresolved removal action. |
| `sample-security-finding.md` | Show finding intake, triage, assignment, and escalation. |
| `sample-restore-test.md` | Show measured recovery results and an objective that was missed. |

## Rules for interpreting examples

- **Simulated** means the event, account, identity, test, and result were invented for this portfolio case study.
- A filled template is not proof that an AWS control was implemented.
- A proposed configuration or diagram is design evidence, not operating evidence.
- A failed example must remain marked **Fail** until remediation and retesting occur.
- Real evidence would need a verifiable source, account/environment, collection date, period, reviewer, and access restrictions.

The test plan is in `docs/15-control-testing-and-evidence-plan.md`. Control ownership and expected evidence are in `controls/cloud-control-matrix.md`.
