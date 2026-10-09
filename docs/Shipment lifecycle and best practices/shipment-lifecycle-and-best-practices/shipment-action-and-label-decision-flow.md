---
title: Shipment action and label decision flow
excerpt: >-
  When creating a shipment in SAPIENT, the value specified in the Action field
  determines how the shipment is processed, what information is returned in the
  response, and whether additional API calls are required before the shipment
  can be manifested.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
Choosing the correct action is important for optimising your integration and avoiding unnecessary processing steps. For example, when using the Process action, tracking numbers and labels are returned directly in the Create Shipment response, making additional label generation requests unnecessary. In contrast, the Create and Allocate actions require further processing before the shipment is ready for manifesting.

The following decision flow helps you determine the expected outcome of each shipment action and identifies when the Print Label API should be used. It also highlights the recommended processing path for each action so that shipments can progress efficiently through the shipment lifecycle.

```mermaid
flowchart TD
    A[Create Shipment request] --> B{Which Action did you send?}

    B -->|Process| C["Read tracking number and label<br/>from Create Shipment response"]
    C --> D[Do not call Print Label]
    D --> E[Store and print the returned label]
    E --> F["Continue to shipment processing<br/>or manifesting"]

    B -->|Allocate| G["Read tracking number<br/>from Create Shipment response"]
    G --> H[Call Print Label endpoint]
    H --> I[Store and print the returned label]
    I --> F

    B -->|Create| J["Shipment is created without<br/>tracking number or label"]
    J --> H

    classDef recommended fill:#dff6e4,stroke:#16823b,color:#123b1e;
    classDef warning fill:#fff4cc,stroke:#b58100,color:#4d3900;
    classDef endpoint fill:#e8f1ff,stroke:#3973b8,color:#17365d;

    class C,D,E,F recommended;
    class A,G,H,I,J endpoint;
    class B warning;
```
