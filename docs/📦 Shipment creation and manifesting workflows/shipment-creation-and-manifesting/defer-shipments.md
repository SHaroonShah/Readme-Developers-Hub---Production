---
title: Defer shipments
excerpt: >-
  Deferring shipments refers to the practice of postponing or delaying the
  dispatch of goods to a later date or time. This could occur for various
  reasons, for example, supply chain issues, customer requests, logistical
  challenges, and so on.
deprecated: false
hidden: false
icon: fad fa-cart-circle-xmark
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
Deferring <Glossary>shipments</Glossary> refers to the practice of postponing or delaying the dispatch of goods to a later date or time. This feature is essential for managing supply chain challenges, customer requests, and logistical issues.

<Cards columns={2}>
  <Card title="Pre-orders & Delayed Stock" icon="clock">
    Defer shipments when goods are not yet available, such as pre-orders or items awaiting restocking.
  </Card>
  <Card title="Early Availability" icon="fast-forward">
    Move future-dated shipments to an earlier date when goods become available ahead of schedule.
  </Card>
</Cards>

## How Deferring Works

If you have one or more shipments that you're unable to ship immediately, you can defer these shipments for up to 28 days in the future. This process can be repeated as needed until goods become available.

When goods become available before their scheduled shipment dates, you can also defer shipments to an earlier date, including today's date.

<Accordion title="Deferring Rules & Limitations" icon="info-circle">

### Key Rules:
- **Maximum defer period:** 28 days from the current date
- **Repeatable process:** You can defer shipments multiple times as needed
- **Auto-manifestation:** Shipments are automatically manifested when the deferred date is reached (if not further deferred)
- **Early shipping:** Shipments can be moved to earlier dates, including the current date

### Important Notes:
- Each deferral can extend the shipment date by up to 28 days
- If you don't defer a shipment again before its scheduled date, it will be automatically processed
- This flexibility helps you adapt to changing inventory and customer needs

</Accordion>

## Workflow Process

<Image align="center" alt="Workflow for defer shipment request" border={false} caption="Workflow for defer shipment request" src="https://files.readme.io/60bca3e1e424cc4ea4fedb09016ef3f69f29ff6deae8f0110fa57f62a7b8884e-Defer_flow.png" />

## Next Steps

<Cards>
  <Card title="API Implementation" href="/docs/defer-shipment" icon="code">
    Learn how to defer shipments programmatically with our step-by-step API tutorial.
  </Card>
</Cards>

<TutorialTile emoji="🦉" slug="defer-shipment" title="Defer shipments" />