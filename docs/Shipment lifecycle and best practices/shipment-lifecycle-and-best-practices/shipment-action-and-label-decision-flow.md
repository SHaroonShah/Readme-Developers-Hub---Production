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
Choose the **Action** for your Create Shipment request and determine whether you need to call the Print Label application programming interface (API) before processing or manifesting the shipment.

## Choose your action

Use these paths to identify what the Create Shipment response contains and what to do next:

<Cards columns="3">
  <Card title="Process" href="/docs/create-shipment-with-action-process" icon="fa-check-circle">
    The response includes a tracking number and label. Store and print the returned label; do not call Print Label.
  </Card>

  <Card title="Allocate" href="/docs/create-shipments-with-action-allocate" icon="fa-barcode">
    The response includes a tracking number, but no label. Call Print Label, then store and print the returned label.
  </Card>

  <Card title="Create" href="/docs/create-shipments-with-action-create" icon="fa-box">
    The shipment has no tracking number or label. Call Print Label, then store and print the returned label.
  </Card>
</Cards>

## Follow the decision flow

Follow your **Action** path from the Create Shipment request to shipment processing or manifesting.

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

<Callout icon="🚧" theme="warning">
  ### _Important_

  _When&#x20;_**_Action_**_&#x20;is&#x20;_**_Process_**_, use the label from the Create Shipment response. Do not call&#x20;_**_Print Label_**_&#x20;for the same shipment. Call&#x20;_**_Print Label_**_&#x20;when you used&#x20;_**_Create_**_&#x20;or&#x20;_**_Allocate_**_._
</Callout>
