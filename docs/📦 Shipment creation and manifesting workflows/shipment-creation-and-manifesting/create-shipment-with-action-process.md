---
title: Create shipment with Process action
excerpt: >-
  Process is an action that finalises the shipment creation and prepares the
  shipment for transportation.
deprecated: false
hidden: false
icon: fad fa-cart-minus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

The **Process** action is used when you want to create <Glossary>shipments</Glossary> and print <Glossary>labels</Glossary> simultaneously. This action finalizes the shipment creation and prepares the shipment for transportation.

<Cards columns={2}>
  <Card title="Key Benefits" icon="fa-check-circle">
    - Shipments are ready to be manifested immediately
    - Reduces the number of API calls required
    - Labels and CN23 forms are returned in the response
  </Card>
  
  <Card title="When to Use" icon="fa-warehouse">
    Perfect for warehouses that simultaneously pick, pack, and stick labels to shipments
  </Card>
</Cards>

## How It Works

<Accordion title="Default Behavior" icon="fa-info-circle">
If no value is set for the **Create Shipment** action, then the shipments are created with the **Process** status by default.
</Accordion>

<Accordion title="Response Contents" icon="fa-file-text">
When using the Process action, the successful response includes:
- Shipment details
- Printable labels (if required)
- CN23 customs forms (if required for international shipments)
</Accordion>

## Workflow Diagram

<Image 
  align="center" 
  alt="Workflow for creating shipments with the Process action" 
  border={false} 
  caption="Workflow for creating shipments with Process action" 
  src="https://files.readme.io/f762106c6e0adca64fd03cbc168faecdddceccf9adcb67b8bb963988cc3090bc-Process_flow.png" 
/>

## Implementation

To use the Process action in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request:

<Tabs>
  <Tab title="API Call">
    Set the `action` parameter to `"Process"` in your request body when calling the Create Shipment endpoint.
  </Tab>
  
  <Tab title="Expected Response">
    The response will include:
    - Shipment confirmation details
    - Label data (ready for printing)
    - CN23 forms (for international shipments)
    - Shipment status: "Process"
  </Tab>
</Tabs>

## Next Steps

Once you've created shipments with the Process action, follow this step-by-step guide to complete the workflow:

<TutorialTile 
  emoji="🦉" 
  slug="process-shipments-created-with-the-action-process" 
  title="Process shipment created with the action Process" 
/>

## Related Topics

<Cards columns={3}>
  <Card title="Create Shipment API" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-plus-circle">
    Learn about all available parameters and options
  </Card>
  
  <Card title="Manifesting Shipments" icon="fa-list-check">
    How to manifest your processed shipments
  </Card>
  
  <Card title="Label Printing" icon="fa-print">
    Best practices for handling label printing workflows
  </Card>
</Cards>