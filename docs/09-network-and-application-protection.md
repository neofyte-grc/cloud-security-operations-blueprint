# Network and Application Protection

## Protection objective

Expose only the approved application entry point while limiting communication among application components, data stores, and PLG integrations.

## Proposed controls

| Area | Design requirement | Validation |
|---|---|---|
| Public entry | Accept only required protocols; use transport encryption and controlled request handling. | Review endpoint and transport configuration. |
| Application tier | Permit only documented inbound and outbound paths. | Compare deployed rules with approved flow list. |
| Data tier | Do not expose the data store directly to external users. | Check reachability and access rules. |
| WMS integration | Authenticate the interface and restrict destination, direction, and fields. | Exercise allowed and denied exchanges. |
| Billing integration | Send approved billing references without unnecessary customer or medical details. | Inspect schema and representative test messages. |
| Application input | Validate requests and reject unauthorized record identifiers. | Test malformed input and cross-user access. |
| Change control | Review network and application access changes before release. | Match change ticket to implemented settings. |

Network restrictions support application authorization; they do not replace it. The application must make the final decision about whether a dispatcher or courier may act on a specific delivery.

## Failure handling

An integration timeout must produce an identifiable error, retry or reconciliation decision, and operator notification. PLG must prevent duplicate assignments or billing entries during retries. The Dispatch Manager and Application Owner should approve the operational fallback before launch.

## Ownership and risks

The Cloud Platform Lead owns network rules and account-level settings. The Application Owner owns endpoint behavior, authorization, input handling, and integration logic. Security/GRC reviews the test evidence.

This design addresses R-03 and R-07 primarily through `CLD-04` and `CLD-10`. The specific AWS networking and application services will be selected in an implementation design.
