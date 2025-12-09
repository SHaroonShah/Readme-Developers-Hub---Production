---
title: Manifest shipments by picked status
excerpt: >-
  Learn how to manifest shipments by Picked status to ensure only ready-to-ship
  items are processed for carrier pickup, with step-by-step workflows for
  different action types.
deprecated: false
hidden: false
icon: fad fa-cart-circle-check
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
If you want to ensure that only <Glossary>shipments</Glossary> that are ready to be picked up by the <Glossary>carrier</Glossary> are to be manifested, you can update the shipments' status to **Picked** throughout the day when you compete the packing and labelling processes and <Glossary>manifest</Glossary> only picked shipments by calling the manifest service using the status "**Picked**".

<Accordion title="Prerequisites and Important Notes" icon="exclamation-triangle">

> 🚧 *Important*
>
> *Before updating the shipment status to**Picked**, make sure to print the <Glossary>labels</Glossary> . If you use the default action (that is [Process](https://docs.intersoftsapient.net/docs/create-shipment-with-action-process)) in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) requests, the labels are returned in the response.*

If you use the action [Create](https://docs.intersoftsapient.net/docs/create-shipments-with-action-create) or [Allocate](https://docs.intersoftsapient.net/docs/create-shipments-with-action-allocate), then you need to send a [Print Label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-rm-shipmentid) request before you can update the shipment status to "**Picked**" and manifest by "**Picked**" status.

</Accordion>

## Workflow Options

<Tabs>
  <Tab title="Process Action (Default)">
    When using the **Process** action in your Create Shipment requests:
    - Labels are automatically returned in the response
    - You can immediately update shipment status to "Picked"
    - No additional Print Label request needed
  </Tab>
  <Tab title="Create/Allocate Actions">
    When using **Create** or **Allocate** actions:
    - Send a Print Label request first
    - Update shipment status to "Picked"
    - Then manifest by "Picked" status
  </Tab>
</Tabs>

## Key Process Steps

<Cards columns={2}>
  <Card title="Individual Updates" icon="box">
    Update shipment status one by one as items are packed and ready for pickup.
  </Card>
  <Card title="Batch Updates" icon="boxes">
    Update multiple shipment statuses in batches, depending on your warehouse process workflow.
  </Card>
</Cards>

## Visual Workflow

<Image align="center" alt="Workflow of manifesting shipments with the Picked status" border={false} caption="Workflow of manifesting shipments by Picked status" src="https://files.readme.io/ed310971eabce3d2cd34b1a1a63a2d1683f26ee432f6cf1601d0dae6851b1a2e-Manifest_by_picked_flow.png" />

## Next Steps

<Cards>
  <Card title="API Implementation Guide" href="/docs/release-and-manifest-held-shipments" icon="code">
    Follow our step-by-step API recipe to learn how to manifest shipments by Picked status via API.
    <TutorialTile emoji="🦉" slug="release-and-manifest-held-shipments" title="Manifest picked shipments" />
  </Card>
</Cards>