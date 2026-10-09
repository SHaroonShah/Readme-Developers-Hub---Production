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
The shipment lifecycle represents the recommended end-to-end workflow for creating, managing, and manifesting shipments in SAPIENT. It illustrates the key stages a shipment can move through, from the initial shipment creation request to manifesting and carrier handover.

Use the following workflow to understand how shipments move through SAPIENT, identify the correct next step at each stage, and avoid common processing mistakes such as generating labels unnecessarily or performing manual actions that can be completed in bulk.

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

<Callout icon="🚧" theme="warn">
  ### _Important_

  _When Action is set to&#x20;_**_Process_**_, the shipment label is returned in the successful Create Shipment response. Do not call the&#x20;_**_Print Label_**_&#x20;endpoint afterwards. Use the Print Label endpoint when the shipment was created using&#x20;_**_Create_**_&#x20;or&#x20;_**_Allocate&#x20;_**_actions, as the label is not returned in the Create Shipment response._
</Callout>
