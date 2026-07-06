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
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Cards columns={2}>
  <Card title="Pre-orders & delayed stock" icon="fa-solif fa-clock">
    Defer shipments when goods are not yet available, such as pre-orders or items awaiting restocking.
  </Card>

  <Card title="Early availability" icon="fa-solid fa-forward">
    Move future-dated shipments to an earlier date when goods become available ahead of schedule.
  </Card>
</Cards>

## How deferring works

If you have one or more shipments that you're unable to ship immediately, you can defer these shipments for up to 28 days in the future. This process can be repeated as needed until goods become available.

When goods become available before their scheduled shipment dates, you can also defer shipments to an earlier date, including today's date.

<Accordion title="Deferring Rules & Limitations">
  * **Maximum defer period:** 28 days from the current date
  * **Repeatable process:** You can defer shipments multiple times as needed
  * **Auto-manifestation:** Shipments are automatically manifested when the deferred date is reached (if not further deferred)
  * **Early shipping:** Shipments can be moved to earlier dates, including the current date
</Accordion>

### Workflow process


<Image src="https://files.readme.io/60bca3e1e424cc4ea4fedb09016ef3f69f29ff6deae8f0110fa57f62a7b8884e-Defer_flow.png" alt="Workflow for defer shipment request" align="center" caption="Workflow for defer shipment request" />


***

### API recipe

To view a step-by-step process on how to defer shipments via API, refer to the following API recipe:

<Recipe slug="defer-shipment" title="Defer shipments" />

<br />
