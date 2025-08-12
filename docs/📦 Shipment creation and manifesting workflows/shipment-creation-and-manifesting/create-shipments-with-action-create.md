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

> 🚧 *Important*
>
> *You can only manifest the shipments for which you have printed the labels.*

If no value is set for this action in the [CreateShipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request, then the shipments are created with the “**Process**” status.

This functionality is included for backwards compatibility to allow existing customers to migrate to the new platform.

<Image align="center" alt="Example flow of creating shipment with Create action" border={false} caption="Workflow for creating shipments with Create action" src="https://files.readme.io/822c8b02ea907f91f7549757093ce56cf1c8823b6b310fe73a1b7874474bc8f1-Create_flow.png" />

To view a step-by-step process on how to process the shipments that are created with the action "Create," refer to the following API recipe:

<TutorialTile emoji="🦉" slug="process-shipment-created-with-the-action-create" title="Process shipment created with the action &#x22;Create&#x22;" />