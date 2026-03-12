---
title: Use pre-allocated tracking number
excerpt: >-
  A _pre-allocated tracking number_ is a unique identifier assigned in advance
  to a shipment or order before it is physically despatched. This tracking
  number is generated automatically by the logistics system when an order is
  placed or processed, allowing for seamless tracking of the shipment throughout
  its journey.
deprecated: false
hidden: false
icon: fad fa-rectangle-barcode
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you need to communicate the Royal Mail tracking number to your customers before you have all the shipment details, you can request a pre-allocated tracking number by providing the following details:

| Detail | Description |
| --- | --- |
| **Destination country** | The country where the shipment will be delivered. |
| **Postcode** | Required depending on the destination country. |
| **Service code** | The Royal Mail service code for the shipment. |
| **Shipping account** | The account you will use to create the shipment. |
| **Shipping location** | Required if you have more than one shipping location linked to the shipping account. |

## Create the shipment

After you have all the <Glossary>shipment information</Glossary>, call the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) endpoint using the <Glossary>pre-allocated tracking number</Glossary>.

<Callout icon="⚠️" theme="warning">
  The **Create Shipment** request using a pre-allocated tracking number can only have **one package**, and all the information sent when requesting the pre-allocated tracking number must match the information sent in the **Create Shipment** request.
</Callout>

<Image alt="Workflow for creating shipments with pre-allocated tracking number" align="center" src="https://files.readme.io/6d031f6c0ef480d45d5d3e10ae5296035962f8070a2b289ecbe626789876113b-Manifest_by_preallocate_tracking_number_flow.png">
  Workflow for creating shipments with pre-allocated tracking number
</Image>

<Callout icon="📘" theme="info">
  The pre-allocated tracking number does not expire.
</Callout>

## Next steps

<Cards columns={2}>
  <Card title="Create Shipment API" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-plus">
    View the full API reference for creating Royal Mail shipments.
  </Card>
  <Card title="Pre-allocated tracking number recipe" href="https://docs.intersoftsapient.net/v4.02/recipes/use-pre-allocated-tracking-number" icon="fa-book">
    Follow a step-by-step guide on using pre-allocated tracking numbers in your API calls.
  </Card>
</Cards>

<TutorialTile backgroundColor="#a5a9ac" emoji="🗃️" id="64e4ac674e47e0006cecbd78" link="https://docs.intersoftsapient.net/v4.02/recipes/use-pre-allocated-tracking-number" slug="use-pre-allocated-tracking-number" title="Use pre-allocated tracking number" />