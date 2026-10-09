---
title: Manage shipment status flow
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
Manage a shipment after creation by choosing whether to hold, release, defer, cancel or recall it before manifesting.

## Choose a status action

Select the action that matches what you need to do with the shipment:

<Cards>
  <Card title="Hold shipment" href="/docs/held-shipments" icon="fa-pause-circle">
    Temporarily exclude a shipment from manifesting until you release it.
  </Card>

  <Card title="Release shipment" href="/docs/release-shipment" icon="fa-play-circle">
    Remove a shipment from hold so it can proceed towards manifesting.
  </Card>

  <Card title="Defer shipment" href="/docs/defer-shipments" icon="fa-clock">
    Move a shipment to a later date when it cannot ship immediately.
  </Card>

  <Card title="Cancel shipment" href="/docs/view-cancelled-shipments" icon="fa-ban">
    Stop a shipment and move it to **Cancelled**.
  </Card>

  <Card title="Recall shipment" href="/docs/recall-shipment" icon="fa-undo">
    Reinstate a cancelled shipment within the first 24 hours.
  </Card>
</Cards>

## Follow the status flow

Use the diagram to see how each action affects the shipment's path to manifesting.

```mermaid
flowchart TD

    A[Shipment created] --> B{What do you need to do?}

    B -->|Continue normally| C[Prepare shipment for manifesting]

    B -->|Temporarily prevent manifesting| D[Hold shipment]
    D --> E[Shipment excluded from manifesting]
    E --> F{Ready to continue?}
    F -->|Yes| G[Release shipment]
    G --> C
    F -->|No| E

    B -->|Ship at a later date| P[Defer shipment]
    P --> Q[Shipment moved to Deferred]
    Q --> R{Deferred date reached?}
    R -->|Yes| C
    R -->|No| Q

    B -->|Stop the shipment| H[Cancel shipment]
    H --> I[Shipment moved to Cancelled]

    I --> J{Reinstate the shipment?}

    J -->|Yes, within the permitted period| K[Recall shipment]
    K --> L[Shipment restored to its previous state]

    L --> M{Was it restored to Held?}
    M -->|Yes| G
    M -->|No| C

    J -->|No| N[Shipment remains cancelled]

    C --> O[Manifest shipment]

    classDef happy fill:#dff6e4,stroke:#16823b,color:#123b1e;
    classDef hold fill:#fff4cc,stroke:#b58100,color:#4d3900;
    classDef deferred fill:#e0f0ff,stroke:#3973b8,color:#17365d;
    classDef cancel fill:#ffe2e2,stroke:#c53d3d,color:#571515;
    classDef decision fill:#f3ebff,stroke:#7a52c7,color:#3f276d;

    class A,C,G,K,L,O happy;
    class D,E hold;
    class P,Q deferred;
    class H,I,N cancel;
    class B,F,J,M,R decision;
```

## Manifesting and recall rules

- **Held shipments:** Held shipments are excluded from manifesting. Release them before manifesting. The manifest status filter supports **Picked**; without that filter, matching **Picked** or **LabelPrinted** shipments are included, but held shipments remain excluded.
- **Bulk release:** You can select and release multiple held shipments together in the user interface (UI) so they can be closed out.
- **Recall period:** You can recall a cancelled shipment within the first 24 hours. Recall restores its previous processed or unprocessed state.
- **Recall of a held shipment:** A shipment cancelled while on hold returns to **Held** when recalled. Release it before manifesting.