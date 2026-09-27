# Cloud Incident Response Procedure

**Control links:** CLD-08, CLD-12  
**Applies to:** Suspected compromise, unauthorized disclosure, or material disruption of the proposed dispatch workload  
**Status:** Proposed procedure; contacts, decision rights, and exercise results require PLG approval

## 1. Activate

The person discovering the event contacts the Incident Lead and Security/GRC Lead through the approved channel. The Incident Lead opens an incident record with the detection time, reporter, affected environment, known impact, and response participants.

If dispatch operations are affected, notify the Dispatch Manager promptly so delivery continuity can be addressed.

## 2. Triage and declare

1. Confirm what is known and what remains uncertain.
2. Determine whether identities, customer or medical-delivery details, integrations, or backups may be affected.
3. Assess whether suspicious activity is ongoing and whether production service is impaired.
4. Set an incident severity and name a response lead.
5. Notify the CIO/IT Director and other decision-makers according to severity.

The Privacy/Legal Adviser determines which contractual or legal notification questions require review. Response staff do not make an unreviewed compliance or notification claim.

## 3. Contain and preserve

The Cloud Platform Lead and Application Owner propose containment actions. The Incident Lead approves actions that could interrupt dispatch, consulting the Dispatch Manager and CIO/IT Director when time permits.

Possible actions include restricting a role, revoking application access, isolating a component, suspending an integration, or blocking a harmful path. Record who approved and performed each action and its time.

Preserve relevant log references, configuration state, affected identifiers, and collection details. Limit access to investigative records.

## 4. Investigate and recover

1. Build a timeline and identify the likely entry point, affected records, and scope.
2. Remove the cause and validate that the threat is contained.
3. Restore affected functions using approved changes or the recovery procedure.
4. Test authorized and denied application access and confirm monitoring resumes.
5. Have the Dispatch Manager verify operational usability before normal dispatch resumes.

## 5. Communicate and close

The Incident Lead keeps a decision log and coordinates approved updates. The COO/CIO and Privacy/Legal Adviser approve external communications as applicable.

After containment, hold a review covering root cause, customer and operational impact, control failures, corrective actions, owners, due dates, and risk-register changes. Close only after action ownership and follow-up dates are recorded.

## 6. Exercise

Test at least one cross-courier access scenario and one dispatch outage scenario in a tabletop. Label exercise records as simulated; do not present them as actual incidents.
