# Project 4 Diagrams

These Mermaid diagrams show a **proposed logical architecture** for PLG's AWS-hosted dispatch and delivery workload. They do not establish that accounts, services, integrations, or controls have been deployed.

| Diagram | Question it answers |
|---|---|
| `context-diagram.md` | Who interacts with the dispatch workload? |
| `aws-reference-architecture.md` | What are the proposed account and workload boundaries? |
| `data-flow-and-trust-boundaries.md` | Which information crosses which trust boundary? |
| `identity-and-access-flow.md` | How do identities become authorized for AWS or application actions? |
| `security-event-workflow.md` | How does a security event become an assigned and resolved finding? |

## Diagram rules

- Lines represent intended logical flows, not confirmed network connections.
- “Security boundary” represents a separately governed destination; its final account and service design remain implementation decisions.
- A courier's application access is separate from AWS administrative access.
- Customer and medical-delivery fields are limited according to the approved workflow.
- Each diagram should be revised if the data inventory, interfaces, or account design changes.

Read `docs/04-data-flows-and-trust-boundaries.md` and `docs/07-aws-account-and-architecture-design.md` alongside these diagrams. Validate Mermaid rendering in GitHub after upload.
