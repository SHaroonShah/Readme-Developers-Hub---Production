---
title: Bulk status update flow
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
When the same action needs to be applied to multiple shipments, processing them individually can increase the number of API requests and add unnecessary complexity to your workflow. Where supported, SAPIENT allows you to update multiple shipments in a single operation, making shipment management more efficient and reducing processing time.

This approach is particularly useful when large groups of shipments need to be cancelled, held, released, or otherwise updated as part of the same business process. Instead of performing the same action repeatedly for each shipment, you can submit a single request containing all applicable shipment identifiers and review the outcome for each shipment in the response.

The following workflow demonstrates how to determine when a bulk status update should be used and outlines the recommended process for updating multiple shipments efficiently.

```mermaid
flowchart TD
    A["Identify shipments requiring<br/>the same status change"] --> B{How many shipments?}

    B -->|One| C[Submit one shipment identifier]
    B -->|Multiple| D[Collect the shipment identifiers]
    D --> E[Submit one bulk status update request]

    C --> F{Required action}
    E --> F

    F -->|Cancel| G[Apply Cancelled status]
    F -->|Hold| H[Apply Held status]
    F -->|Release| I[Apply Released status]
    F -->|Recall| J[Apply the supported recall process]

    G --> K[Review the result for each shipment]
    H --> K
    I --> K
    J --> K

    K --> L{Any unsuccessful updates?}
    L -->|No| M[Continue workflow]
    L -->|Yes| N["Review the affected shipment<br/>and carrier-specific conditions"]

    classDef bulk fill:#dff6e4,stroke:#16823b,color:#123b1e;
    classDef decision fill:#fff4cc,stroke:#b58100,color:#4d3900;
    classDef review fill:#ffe2e2,stroke:#c53d3d,color:#571515;

    class A,D,E,G,H,I,J,K,M bulk;
    class B,F,L decision;
    class N review;
```
