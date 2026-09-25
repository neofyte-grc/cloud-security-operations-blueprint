# Data Flows and Trust Boundaries

## Primary workflow

1. A commercial or healthcare customer provides an order through an approved PLG intake channel.
2. An authorized dispatcher reviews the order and assigns a delivery in the dispatch application.
3. The assigned employee driver or independent courier retrieves only the details needed for that delivery.
4. The driver or courier submits status and proof-of-delivery information.
5. Authorized PLG personnel review completion and send approved billing references to the billing process.
6. Required operational and security events are sent to the designated monitoring and log destinations.

The AWS workload does not directly expose the WMS or billing system to courier devices.

## Logical flows

| Flow | Source → destination | Data | Boundary and protection question |
|---|---|---|---|
| F-01 | Intake channel → dispatch application | Order details | Which source is trusted, and how is input validated? |
| F-02 | Dispatcher → dispatch application | Assignment and updates | How is employee identity verified and authorized? |
| F-03 | Application → assigned courier | Minimum delivery details | How is access limited to current assignments? |
| F-04 | Courier → application | Status and proof of delivery | How is submission authenticated and checked? |
| F-05 | WMS ↔ approved integration | Fulfillment status | Which fields, direction, and network path are allowed? |
| F-06 | Application → billing process | Billing reference | How are unnecessary personal details excluded? |
| F-07 | AWS workload → log destination | Events and findings | Who can alter or retrieve retained records? |

## Trust boundaries

- **TB-01, external users/devices:** Customer and courier connections cross into the application entry point.
- **TB-02, workforce identity:** PLG employee identity crosses into AWS administration or application access.
- **TB-03, application/data:** Application components cross into protected data stores.
- **TB-04, AWS/on-premises:** Approved integration crosses between the AWS workload and PLG systems.
- **TB-05, workload/security:** Events cross from workload accounts into a separately governed security destination.

## Design implications

Require authentication and authorization at each relevant entry point. Limit courier records to assigned work, encrypt approved transmission paths, validate inputs, and record significant access and administrative actions. Document failure behavior for WMS and billing integrations so a broken interface does not silently lose or duplicate deliveries.

The corresponding diagrams will be maintained in `diagrams/context-diagram.md` and `diagrams/data-flow-and-trust-boundaries.md`.
