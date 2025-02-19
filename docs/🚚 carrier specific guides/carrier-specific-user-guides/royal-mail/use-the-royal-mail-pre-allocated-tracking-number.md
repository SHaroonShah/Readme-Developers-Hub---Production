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
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you need to communicate the Royal Mail tracking number to your customers before you have all the shipment details, you can request a pre-allocated tracking number by providing the following details: 

* Destination country
* Postcode (depending on the Destination Country)
* Service code
* Shipping account that you will be using to create the shipment. 
* Shipping location, if you have more than one shipping location linked to the shipping account.

After you have all the <Glossary>shipment information</Glossary>, you can call the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) endpoint using the <Glossary>pre-allocated tracking number</Glossary>.

The **Create Shipment** request using a pre-allocated tracking number can only have one package, and all the information sent when requesting the pre-allocated tracking number must match the information that is later sent in the **Create Shipment** request.

<Image alt="Workflow for creating shipments with pre-allocated tracking number" align="center" src="https://files.readme.io/6d031f6c0ef480d45d5d3e10ae5296035962f8070a2b289ecbe626789876113b-Manifest_by_preallocate_tracking_number_flow.png">
  Workflow for creating shipments with pre-allocated tracking number
</Image>

> 📘 *Note*
>
> *The pre-allocated tracking number does not expire.*

To view a step-by-step process on how to use the pre-allocated tracking number in your API calls, refer to the following API recipe: 

<TutorialTile backgroundColor="#a5a9ac" emoji="🗃️" id="64e4ac674e47e0006cecbd78" link="https://docs.intersoftsapient.net/v4.02/recipes/use-pre-allocated-tracking-number" slug="use-pre-allocated-tracking-number" title="Use pre-allocated tracking number" />