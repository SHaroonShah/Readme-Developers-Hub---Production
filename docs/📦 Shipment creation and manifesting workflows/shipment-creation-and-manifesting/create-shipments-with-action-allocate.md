---
title: Create shipments with Allocate action
excerpt: >-
  Learn how to use the Allocate action when creating shipments to efficiently
  manage inventory allocation and on-demand label printing in your warehouse
  workflow.
deprecated: false
hidden: false
icon: fad fa-cart-arrow-up
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    _Allocate_ refers to an action that assigns resources (like items from
    inventory) to the shipment for fulfilment. This action ensures that the
    items intended for shipment are set aside and ready to be despatched.
  robots: index
---
## What is the Allocate Action?

<Accordion title="Understanding Allocate Action" icon="info-circle">
  **Allocate** refers to an action that assigns resources (like items from inventory) to the <Glossary>shipment</Glossary> for fulfilment. This action ensures that the items intended for shipment are set aside and ready to be dispatched.
</Accordion>

## When to Use Allocate Action

<Cards columns={2}>
  <Card title="Pre-sorted Packages" icon="box">
    Perfect for packages that are already sorted and only need labels printed after shipment creation.
  </Card>
  <Card title="On-demand Label Printing" icon="print">
    Enables printing labels only when required in your warehouse process, optimizing workflow efficiency.
  </Card>
</Cards>

## How It Works

If your packages are pre-sorted and need labels to be printed after the <Glossary>shipments</Glossary> have been created, using the **Allocate** action in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request enables you to print <Glossary>labels</Glossary> only when they are required in your warehouse process.

**Important:** Only shipments that you have printed the labels for will be ready to be manifested.

<Accordion title="Default Behavior" icon="cog">
  If no value is set for this action in the **Create Shipment** request, then the shipments are created with the **Process** status.
</Accordion>

## Workflow Overview

<Image align="center" alt="Workflow for creating shipments with Allocate action" border={false} caption="Workflow for creating shipments with Allocate action" src="https://files.readme.io/ba62c3736040ac758d924aa4f0ec47c4dc6d3bcd390cd370b139454f8e2a4a47-Allocate_flow.png" />

## Step-by-Step Implementation

<Cards columns={1}>
  <Card title="Complete Tutorial: Process Shipments with Allocate Action" href="/docs/recipe-titleprocess-shipment-created-with-the-action-allocate" icon="book">
    Follow our comprehensive API recipe for a detailed, step-by-step process on how to handle shipments created with the "Allocate" action.
  </Card>
</Cards>