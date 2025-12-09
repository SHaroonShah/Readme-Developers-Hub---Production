---
title: Create shipments with Create action
excerpt: >-
  _Create_ is an action that initiates a new shipment entry in the system. This
  action captures all the necessary details of the shipment to generate shipping
  documents and prepare for the actual shipping process.
deprecated: false
hidden: false
icon: fad fa-cart-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you do not want the <Glossary>tracking number</Glossary> returned until you send the [Print Label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-rm-shipmentid) request, you can create <Glossary>shipments</Glossary> using the **Create** action.

> 🚧 _Important_
>
> _You can only manifest the shipments for which you have printed the labels._

## How Create action works

<Cards columns={2}>
  <Card title="Delayed Tracking Numbers" icon="clock">
    Tracking numbers are not returned until you send the Print Label request, giving you flexibility in your shipping workflow.
  </Card>

  <Card title="Process Status Default" icon="cogs">
    If no action value is specified in the CreateShipment request, shipments are automatically created with "Process" status for backwards compatibility.
  </Card>
</Cards>

### Workflow process

<Image align="center" alt="Example flow of creating shipment with Create action" border={false} caption="Workflow for creating shipments with Create action" src="https://files.readme.io/822c8b02ea907f91f7549757093ce56cf1c8823b6b310fe73a1b7874474bc8f1-Create_flow.png" />

To view a step-by-step process on how to process the shipments that are created with the action "Create," refer to the following API recipe:

<Recipe slug="process-shipment-created-with-the-action-create" title="Process shipment created with the action &#x22;Create&#x22;" />
