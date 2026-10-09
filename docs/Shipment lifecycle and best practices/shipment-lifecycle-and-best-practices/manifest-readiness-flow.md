---
title: Manifest readiness flow
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
Before a shipment can be manifested, it must meet the required criteria for the selected manifesting method. Depending on how the shipment was created and processed, certain actions may need to be completed first, such as generating labels, releasing held shipments, or resolving shipment status issues.

Understanding what makes a shipment eligible for manifesting helps prevent failed manifest requests and ensures shipments are included in the correct manifest. This is particularly important when working with different creation actions, shipment statuses, containers, or asynchronous manifesting processes.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Shipments may be manifested by container, Picked status, shipping location, shipping account or service code. If no manifest parameters are supplied, shipments in LabelPrinted or Picked status are manifested, excluding future-dated shipments and those assigned to a container._

  _For asynchronous manifesting, the manifest webhook must be configured before using that workflow\._
</Callout>

The following workflow illustrates the key checks and decision points that determine whether a shipment is ready for manifesting and the available paths for submitting shipments to the carrier.

```mermaid
flowchart TD
    A[Shipment has been labelled] --> B{Current shipment state}

    B -->|LabelPrinted| C[Eligible for manifesting]
    B -->|Picked| C
    B -->|Held| D[Release shipment first]
    B -->|Cancelled| E[Not eligible for manifesting]
    B -->|Future dated| F[Wait until the shipment is eligible]

    D --> G[Shipment released]
    G --> C

    C --> H{Choose manifest method}
    H -->|Specific shipments or criteria| I[Manifest using the required filters]
    H -->|Container| J[Manifest shipments in the container]
    H -->|Asynchronous| K[Submit asynchronous manifest request]
    H -->|UI| L[Manifest through the SAPIENT UI]

    I --> M[Manifest response generated]
    J --> M
    L --> M

    K --> N["Receive completion through<br/>the configured Manifest Webhook"]
    N --> M

    M --> O["Print or store manifest<br/>where required"]
    O --> P[Hand shipments to carrier]

    classDef ready fill:#dff6e4,stroke:#16823b,color:#123b1e;
    classDef blocked fill:#ffe2e2,stroke:#c53d3d,color:#571515;
    classDef decision fill:#fff4cc,stroke:#b58100,color:#4d3900;
    classDef endpoint fill:#e8f1ff,stroke:#3973b8,color:#17365d;

    class A,C,D,G,I,J,K,L,M,N,O,P ready;
    class E,F blocked;
    class B,H decision;
```
