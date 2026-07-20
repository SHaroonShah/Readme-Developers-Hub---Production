---
title: Navigation structure
deprecated: false
hidden: true
metadata:
  robots: index
---
Follow this navigation structure to move from onboarding through implementation and support.

## Navigation hierarchy

```text
Home
├── Introduction
├── Getting Started
│   └── Quick Start
├── Authentication
└── API Reference
```

<Callout icon="🧭" theme="info">
  ### _Note_

  _This navigation mirrors the developer journey from onboarding to implementation and support._
</Callout>

## Documentation page types

<Cards>
  <Card title="Concept pages" icon="lightbulb">
    **Purpose:** Explain foundational knowledge before you begin implementation.

    **Example:** Introduction
  </Card>
  <Card title="How-to guides" icon="list-check">
    **Purpose:** Walk you through a specific task with step-by-step instructions.

    **Examples:** Quick Start and Authentication
  </Card>
  <Card title="Reference pages" icon="book-open">
    **Purpose:** Provide factual, detailed information you can consult while developing.

    **Example:** API Reference
  </Card>
</Cards>

### <br />Layout Rationale

The reason I structured the information in the preceding hierarchy is because this structure separates learning content from reference content, making it easier for different audiences to find what they need.&#x20;

Developers can move from conceptual understanding to implementation without unnecessary context switching, while experienced users can jump directly to the API References section.

<br />This design also aligns with Docs-as-Code approach by enabling independent updates, simpler code reviews, and AI-assisted maintenance without introducing duplicate or conflicting content.
