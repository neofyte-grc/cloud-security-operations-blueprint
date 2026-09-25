# Executive Summary and Reflection

## Executive summary

Peachtree Logistics Group (PLG), a fictional regional logistics company, proposes moving its dispatch and delivery platform into AWS. The workload must support time-sensitive assignments to employees and independent couriers while protecting customer and potentially sensitive medical-delivery information.

This blueprint identifies eight scenario-based risks, led by cross-courier access, compromised identities, weak investigation coverage, and dispatch disruption. It proposes twelve controls covering account governance, identity, application authorization, network paths, data protection, logging, incident response, access lifecycle, integrations, and recovery.

The design connects each business requirement to a risk, architecture decision, owner, proposed test, and evidence source. Separate production and nonproduction boundaries, assignment-level authorization, protected logging, and tested restoration are the main design decisions.

## Decisions required before implementation

1. Approve data classification, retention, and any applicable contractual obligations.
2. Approve the identity source and courier enrollment/removal process.
3. Select implementation services and approve the account and integration architecture.
4. Approve operating coverage and escalation responsibilities.
5. Approve an RTO and RPO supported by business needs.
6. Fund implementation, testing, and remediation of failed controls.

## Project outcome

The deliverable is a **governed reference design and assurance plan**. It is not a deployed AWS environment, certification, compliance determination, or proof that controls operated effectively. Implementation would require configuration, representative tests, dated evidence, owner review, and reassessment of residual risk.

## Reflection

The central lesson is that a cloud control becomes useful when somebody can operate it and demonstrate its result. Separating AWS administration from application authorization is especially important: a secure account baseline does not prevent one courier from seeing another courier's delivery if application rules are wrong.

A future hands-on extension could deploy a small environment with synthetic data, test assigned versus unassigned access, generate a traceable security event, and perform an isolated restore. Those results should be added as new, dated evidence rather than retroactively described as part of this design-only case study.

**Prepared by:** Tommy Marshall  
**Portfolio focus:** Cloud Security · AWS · GRC
