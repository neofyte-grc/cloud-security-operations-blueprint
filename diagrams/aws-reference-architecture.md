# AWS Reference Architecture

**Status:** Proposed logical architecture; specific AWS compute, database, networking, and integration services have not been selected.

```mermaid
flowchart TB
    Users["Dispatchers and assigned drivers/couriers"]
    Entry["Approved application entry point"]
    App["Application and API"]
    Data["Protected dispatch data"]
    Integrations["Approved WMS and billing interfaces"]
    Security["Separately governed logs and findings"]

    Users -->|"Authenticated requests"| Entry
    Entry --> App
    App <-->|"Authorized data access"| Data
    App <-->|"Minimum necessary exchange"| Integrations
    Entry -->|"Relevant events"| Security
    App -->|"Application and security events"| Security
    Data -->|"Relevant audit events"| Security
```

## Account boundaries

| Boundary | Proposed contents or purpose |
|---|---|
| Management/billing account | Organization administration; no routine dispatch workload. |
| Production workload account | Entry point, application components, data tier, and approved interfaces. |
| Nonproduction workload account | Development and tests using synthetic or approved de-identified data. |
| Security/logging boundary | Restricted storage and review of selected events and findings. |

The account layout and services must be finalized in the implementation design. Backups require a protected recovery arrangement that ordinary workload access cannot readily compromise. The diagram shows logical event flows; it does not imply that every data-store action is logged automatically.

Control connections: CLD-01, CLD-04, CLD-05, CLD-07, and CLD-11.
