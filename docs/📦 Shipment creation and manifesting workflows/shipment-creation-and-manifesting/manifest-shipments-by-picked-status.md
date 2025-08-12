---
title: Manifest shipments by picked status
excerpt: >-
  Manifesting the shipment by the **Picked** status refers to the process of
  preparing and documenting shipments that have been marked as Picked,
  indicating that the items designated for shipment have been successfully
  collected from the inventory and are now ready for the next steps in the
  shipping process.
deprecated: false
hidden: false
icon: fad fa-cart-circle-check
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you want to ensure that only <Glossary>shipments</Glossary> that are ready to be picked up by the <Glossary>carrier</Glossary> are to be manifested, you can update the shipments’ status to **Picked** throughout the day when you compete the packing and labelling processes and <Glossary>manifest</Glossary> only picked shipments by calling the manifest service using the status “**Picked**”.

> 🚧 *Important*
>
> *Before updating the shipment status to**Picked**, make sure to print the <Glossary>labels</Glossary> . If you use the default action (that is [Process](https://docs.intersoftsapient.net/docs/create-shipment-with-action-process)) in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) requests, the labels are returned in the response.*

If you use the action [Create](https://docs.intersoftsapient.net/docs/create-shipments-with-action-create) or [Allocate](https://docs.intersoftsapient.net/docs/create-shipments-with-action-allocate), then you need to send a [Print Label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-rm-shipmentid) request before you can update the shipment status to “**Picked**” and manifest by “**Picked**” status.

You can update the shipment status one by one or in batches, depending on your warehouse process.

<Image align="center" alt="Workflow of manifesting shipments with the Picked status" border={false} caption="Workflow of manifesting shipments by Picked status" src="https://files.readme.io/ed310971eabce3d2cd34b1a1a63a2d1683f26ee432f6cf1601d0dae6851b1a2e-Manifest_by_picked_flow.png" />

To view a step-by-step process on how to manifest the shipments by the **Picked** status via API, refer to the following API recipe:

<TutorialTile emoji="🦉" slug="release-and-manifest-held-shipments" title="Manifest picked shipments" />