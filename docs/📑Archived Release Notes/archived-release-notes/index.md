---
title: SAPIENT archived release notes
excerpt: >-
  In this section, you can view the release notes that have been deployed in
  previous years.
deprecated: false
hidden: false
icon: fad fa-notes
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: link
      title: Latest release notes
      url: https://docs.intersoftsapient.net/changelog
---
<Cards columns="4">
  <Card title="2026 release notes" href="https://docs.intersoftsapient.net/docs/2026-release-notes" icon="fa-regular fa-calendar-lines">
    Release notes for 2026.
  </Card>

  <Card title="2025 release notes" href="https://docs.intersoftsapient.net/docs/2025-release-notes" icon="fa-regular fa-calendar-lines">
    Release notes for 2025.
  </Card>

  <Card title="2024 release notes" href="https://docs.intersoftsapient.net/docs/2024-release-notes" icon="fa-regular fa-calendar-lines">
    Release notes for 2024.
  </Card>

  <Card title="2023 release notes" href="https://docs.intersoftsapient.net/docs/2023-release-notes" icon="fa-regular fa-calendar-lines">
    Release notes for 2023.
  </Card>
</Cards>

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
