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
flowchart LR
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
