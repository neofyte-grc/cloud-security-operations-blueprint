# Identity and Access Model

## Identity groups

| Group | Intended access | Boundary |
|---|---|---|
| AWS platform administrators | Approved account and infrastructure operations | AWS administrative roles |
| Security reviewers | Findings, logs, and approved investigation access | Security roles |
| Application operators | Approved application support functions | Application operations |
| Dispatchers | Assign and manage deliveries within their business scope | Application roles |
| Employee drivers | View and update assigned work | Application roles |
| Independent couriers | View and update only their assigned work | Separate courier identity lifecycle |
| Integration identities | Specific WMS or billing functions | Nonhuman identities with narrow permissions |

AWS administrative access and dispatch application access are **different authorization systems**. An application dispatcher does not receive AWS administrator permissions.

## Proposed rules

- Use individual identities and strong authentication for workforce access.
- Prefer federated, role-based AWS workforce access with temporary credentials.
- Grant only the permissions required for the task; separate privileged duties.
- Enforce assignment-level authorization on the server for drivers and couriers. Hiding a record in the user interface alone is insufficient.
- Use dedicated integration identities; do not reuse an administrator or human account.
- Define joiner, mover, and leaver triggers for employees and a separate eligibility/removal process for couriers.
- Review privileged access at least monthly and other active access at least quarterly as **proposed PLG frequencies**, subject to approval.

## Access decision examples

| Action | Dispatcher | Assigned courier | Other courier | Platform administrator |
|---|---|---|---|---|
| Create or change assignment | Allowed within scope | Denied | Denied | Denied unless separately authorized in application |
| View assigned delivery | Allowed within scope | Allowed | Denied | Denied unless separately authorized in application |
| Submit delivery update | Allowed for approved operational correction | Allowed | Denied | Denied |
| Change AWS infrastructure | Denied | Denied | Denied | Allowed within approved role and change process |

## Verification

Test positive and negative access cases, including changed assignments, expired courier eligibility, removed employees, and attempts to request records by altered identifiers. Retain approval, review, and test records. These measures address R-01, R-02, and R-08 through `CLD-02`, `CLD-03`, and `CLD-09`.
