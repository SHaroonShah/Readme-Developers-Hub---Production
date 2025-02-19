---
title: Track events and milestones
excerpt: >-
  Tracking _all events_ refers to the setting that enables the monitoring and
  logging of every possible event related to a shipment throughout its
  lifecycle, for example, shipment announced, shipment departed depot, delivered
  to safe place, and other.  On the contrary, _milestones_ refer to significant
  stages within the shipment process that are essential for monitoring process,
  such as order created, label printed, out for delivery, and so on.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, while [configuring the tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook), You can choose to receive <<glossary:all tracking events>> or tracking <<glossary:milestones>> only.

- If you select to receive milestones only, the system only pushes the tracking when a new milestone is triggered. 
- If you select to receive full tracking events, then the system pushes the tracking every time it receives a new tracking event from the carrier, regardless of whether the tracking event triggers a new milestone or not.

***

## Milestones

_Milestones_ refer to significant stages within the shipment process that are essential for monitoring process, such as order created, label printed, out for delivery, and so on.

If you choose to receive tracking milestones, bear in mind that each milestone only gets triggered once. To understand each milestone and its expected order of occurrence, refer to the information explained in the following table:

[block:parameters]
{
  "data": {
    "h-0": "Milestone",
    "h-1": "Description",
    "0-0": "**IT'S ON IT'S WAY**",
    "0-1": "The <<glossary:shipment>> was handed over or is on its way to the <<glossary:carrier>>.",
    "1-0": "**IN TRANSIT**",
    "1-1": "The shipment is travelling through the carrier's network.",
    "2-0": "**TRANSIT DELAY**",
    "2-1": "The shipment processing through the carrier's network is delayed.",
    "3-0": "**IN CUSTOMS**",
    "3-1": "The shipment is undergoing customs inspections.  \n  \n_`Note`: this is applicable to international shipments only._",
    "4-0": "**OUT FOR DELIVERY**",
    "4-1": "The shipment is on the way to the recipient.",
    "5-0": "**DELIVERY ATTEMPT FAILED**",
    "5-1": "The delivery was attempted, but failed.",
    "6-0": "**READY FOR COLLECTION**",
    "6-1": "The shipment was left at a chosen location for the recipient to collect.",
    "7-0": "**DELIVERED**",
    "7-1": "The shipment was successfully delivered to the recipient (or another person/place chosen by the recipient).",
    "8-0": "**COLLECTED**",
    "8-1": "The shipment was successfully collected from the collection point.",
    "9-0": "**PART DELIVERED**",
    "9-1": "The part of a consignment shipment was delivered successfully.",
    "10-0": "**UNDELIVERABLE**",
    "10-1": "The delivery of the shipment was not possible."
  },
  "cols": 2,
  "rows": 11,
  "align": [
    "center",
    "left"
  ]
}
[/block]


***

## Final events

Final events are the stages of a shipment lifecycle where no further tracking statuses are sent after the event/milestone was hit. 

The following events are considered as the final events.

- All delivered events
- Recipient collected
- Shipment lost/destroyed
- Undeliverable - destroyed.

***

### List of tracking milestones and tracking events

The following table displays a comprehensive structure of the milestones, event codes, and events that occur throughout the shipping journey of a shipment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1312237f5bcebd28d9d969bebf4a03fb61a27d49511ac12a3668ab47f40d1bf0-Tracking_milestones_list.png",
        null,
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]