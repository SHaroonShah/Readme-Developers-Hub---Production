---
title: Create shipments with Create action
excerpt: >-
  _Create_ is an action that initiates a new shipment entry in the system. This
  action captures all the necessary details of the shipment to generate shipping
  documents and prepare for the actual shipping process.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you do not want the <<glossary:tracking number>> returned until you send the [Print Label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-rm-shipmentid) request, you can create <<glossary:shipments>> using the **Create** action.

> 🚧 _Important_
> 
> _You can only manifest the shipments for which you have printed the labels._

If no value is set for this action in the [CreateShipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request, then the shipments are created with the “**Process**” status.

This functionality is included for backwards compatibility to allow existing customers to migrate to the new platform.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/822c8b02ea907f91f7549757093ce56cf1c8823b6b310fe73a1b7874474bc8f1-Create_flow.png",
        "",
        "Example flow of creating shipment with Create action"
      ],
      "align": "center",
      "caption": "Workflow for creating shipments with Create action"
    }
  ]
}
[/block]