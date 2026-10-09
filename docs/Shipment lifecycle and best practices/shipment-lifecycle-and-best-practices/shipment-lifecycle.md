---
title: Shipment lifecycle
excerpt: >-
  The shipment lifecycle represents the recommended end-to-end workflow for
  creating, managing, and manifesting shipments in SAPIENT. It illustrates the
  key stages a shipment can move through, from the initial shipment creation
  request to manifesting and carrier handover.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
Use this workflow to choose a shipment creation action, identify when to generate a label and move your shipment towards manifesting and carrier handover.

## Choose a shipment action

The **Action** you select determines what the Create Shipment response returns. Open the guide for your chosen action for more detail.

<Cards>
  <Card title="Process" href="/docs/create-shipment-with-action-process" icon="fa-check-circle">
    Returns a tracking number and label. You do not need to call Print Label.
  </Card>
  <Card title="Allocate" href="/docs/create-shipments-with-action-allocate" icon="fa-barcode">
    Returns a tracking number without a label. Call Print Label to generate the label.
  </Card>
  <Card title="Create" href="/docs/create-shipments-with-action-create" icon="fa-box">
    Creates the shipment without allocating a tracking number or label. Call Print Label to generate the label.
  </Card>
</Cards>

## View the full lifecycle

Expand the flow to follow the shipment from preparation through label generation, further processing and manifesting.

<Accordion title="Shipment lifecycle flow" icon="fa-info-circle">
  ```mermaid
  flowchart TD

      A[Prepare shipment data] --> B[Create shipment]

      B --> C{Which Action is used?}

      C -->|Process| D[Tracking number and label returned]
      C -->|Allocate| E["Tracking number returned<br/>Label not returned"]
      C -->|Create| F["Shipment created<br/>Tracking number and label not allocated"]

      E --> G[Call Print Label]
      F --> G

      G --> H[Label generated]

      D --> I[Shipment ready for processing]
      H --> I

      I --> J{Is another action required?}

      J -->|No| K[Manifest shipment]
      J -->|Hold| L[Place shipment on hold]
      J -->|Cancel| M[Cancel shipment]
      J -->|Other processing| N[Continue warehouse processing]

      L --> O[Release shipment]
      O --> K

      M --> P{Recall shipment?}

      P -->|Yes| Q[Recall cancelled shipment]
      Q --> J

      P -->|No| R[Shipment remains cancelled]

      N --> K

      K --> S[Manifest created]

      S --> T[Shipment ready for carrier handover]

      classDef happy fill:#dff6e4,stroke:#16823b,color:#123b1e;
      classDef decision fill:#fff4cc,stroke:#b58100,color:#4d3900;
      classDef exception fill:#ffe2e2,stroke:#c53d3d,color:#571515;
      classDef action fill:#e8f1ff,stroke:#3973b8,color:#17365d;

      class A,B,D,E,F,G,H,I,K,N,O,Q,S,T happy;
      class C,J,P decision;
      class L action;
      class M,R exception;
  ```
</Accordion>

## After label generation

Once the label is available, decide whether the shipment needs another action before manifesting:

- **Hold:** Place the shipment on hold, then release it before manifesting.
- **Cancel:** Cancel the shipment. If you need to process it again, recall it and return to the processing decision.
- **Other processing:** Continue warehouse processing before manifesting.
- **No further action:** Manifest the shipment so it is ready for carrier handover.

<Callout icon="🚧" theme="warning">
  When **Action** is **Process**, the successful Create Shipment response already includes the label. Do not call **Print Label** afterwards. Call **Print Label** for shipments created with **Create** or **Allocate**, because their Create Shipment responses do not include a label.
</Callout>