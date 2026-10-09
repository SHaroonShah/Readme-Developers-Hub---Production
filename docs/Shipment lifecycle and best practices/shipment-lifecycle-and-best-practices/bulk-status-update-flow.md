---
title: Bulk status update flow
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
Choose whether to submit one shipment identifier or a supported bulk status update request, then check the result for each shipment.

## Choose your request

Use the number of shipments requiring the same status change to select a path:

<Columns layout="auto">
  <Column>
    ### One shipment

    Submit one shipment identifier for the required action.
  </Column>

  <Column>
    ### Multiple shipments

    Collect the eligible shipment identifiers and submit them in one supported bulk status update request for the same action.
  </Column>
</Columns>

## Follow the status update flow

The diagram shows the available action paths—cancel, hold, release and the supported recall process—and how to review their results.

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

## Review the results

1. Check the response for the outcome of each shipment identifier.
2. If any update was unsuccessful, review the affected shipment and any carrier-specific conditions before continuing the workflow.
3. Continue the workflow when there are no unsuccessful updates.

<Callout icon="far fa-circle-info" theme="info">
  ### _Note_

  _Use a bulk status update only where the operation supports multiple shipments._
</Callout>
