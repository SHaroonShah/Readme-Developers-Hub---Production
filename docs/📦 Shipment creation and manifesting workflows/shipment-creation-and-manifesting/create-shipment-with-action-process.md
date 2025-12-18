---
title: Create shipment with Process action
excerpt: >-
  _Process_ is an action that finalises the shipment creation and prepares the
  shipment for transportation.
deprecated: false
hidden: false
icon: fad fa-cart-minus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Cards columns={2}>
  <Card title="Key benefits">
    * Shipments are ready to be manifested immediately
    * Reduces the number of API calls required
    * Labels and CN23 forms are returned in the response
  </Card>

  <Card title="When to use">
    Perfect for warehouses that simultaneously pick, pack, and stick labels to shipments
  </Card>
</Cards>

***

## How Process action works

To use the Process action in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request, refer to the following instructions and flow:

<Tabs>
  <Tab title="API call">
    Set the `action` parameter to `"Process"` in your request body when calling the Create Shipment endpoint.
  </Tab>

  <Tab title="Expected response">
    The response will include:

    * Shipment confirmation details
    * Label data (ready for printing)
    * CN23 forms (for international shipments)
    * Shipment status: "Process"
  </Tab>
</Tabs>

### Workflow process

<Image align="center" alt="Workflow for creating shipments with the Process action" border={false} caption="Workflow for creating shipments with Process action" src="https://files.readme.io/f762106c6e0adca64fd03cbc168faecdddceccf9adcb67b8bb963988cc3090bc-Process_flow.png" />

***

### API recipe

To view a step-by-step guide on how to process the shipments that are created with the action "Process," refer to the following API recipe:

<Recipe slug="process-shipments-created-with-the-action-process" title="Process shipment created with the action “Process”" />
