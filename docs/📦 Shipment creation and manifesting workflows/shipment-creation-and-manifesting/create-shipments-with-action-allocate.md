---
title: Create shipments with Allocate action
excerpt: >-
  _Allocate_ refers to an action that assigns resources (like items from
  inventory) to the shipment for fulfilment. This action ensures that the items
  intended for shipment are set aside and ready to be despatched.
deprecated: false
hidden: false
icon: fad fa-cart-arrow-up
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Cards columns={2}>
  <Card title="Pre-sorted packages" icon="box">
    Perfect for packages that are already sorted and only need labels printed after shipment creation.
  </Card>

  <Card title="On-demand label pinting" icon="print">
    Enables printing labels only when required in your warehouse process, optimizing workflow efficiency.
  </Card>
</Cards>

***

## How Allocate action works

If your packages are pre-sorted and need labels to be printed after the <Glossary>shipments</Glossary> have been created, using the **Allocate** action in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request enables you to print <Glossary>labels</Glossary> only when they are required in your warehouse process, and only shipments that you have printed the labels for will be ready to be manifested.

If no value is set for this action in the **Create Shipment** request, then the shipments are created with the **Process** status.

### Workflow process

<Image align="center" alt="Workflow for creating shipments with Allocate action" border={false} caption="Workflow for creating shipments with Allocate action" src="https://files.readme.io/ba62c3736040ac758d924aa4f0ec47c4dc6d3bcd390cd370b139454f8e2a4a47-Allocate_flow.png" />

To view a step-by-step process on how to process the shipments that are created with the action "Allocate," refer to the following API recipe:

<Recipe slug="recipe-titleprocess-shipment-created-with-the-action-allocate" title="Process shipment created with the action &#x22;Allocate&#x22;" />
