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
In SAPIENT, while [configuring the tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook), You can choose to receive <Glossary>all tracking events</Glossary> or tracking <Glossary>milestones</Glossary> only.

* If you select to receive milestones only, the system only pushes the tracking when a new milestone is triggered. 
* If you select to receive full tracking events, then the system pushes the tracking every time it receives a new tracking event from the carrier, regardless of whether the tracking event triggers a new milestone or not.

***

## Milestones

*Milestones* refer to significant stages within the shipment process that are essential for monitoring process, such as order created, label printed, out for delivery, and so on.

If you choose to receive tracking milestones, bear in mind that each milestone only gets triggered once. To understand each milestone and its expected order of occurrence, refer to the information explained in the following table:

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Milestone
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **IT'S ON IT'S WAY**
      </td>

      <td style={{ textAlign: "left" }}>
        The <Glossary>shipment</Glossary> was handed over or is on its way to the <Glossary>carrier</Glossary>.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN TRANSIT**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment is travelling through the carrier's network.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **TRANSIT DELAY**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment processing through the carrier's network is delayed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN CUSTOMS**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment is undergoing customs inspections.  

        *`Note`: this is applicable to international shipments only.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **OUT FOR DELIVERY**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment is on the way to the recipient.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERY ATTEMPT FAILED**
      </td>

      <td style={{ textAlign: "left" }}>
        The delivery was attempted, but failed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **READY FOR COLLECTION**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment was left at a chosen location for the recipient to collect.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERED**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment was successfully delivered to the recipient (or another person/place chosen by the recipient).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **COLLECTED**
      </td>

      <td style={{ textAlign: "left" }}>
        The shipment was successfully collected from the collection point.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **PART DELIVERED**
      </td>

      <td style={{ textAlign: "left" }}>
        The part of a consignment shipment was delivered successfully.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **UNDELIVERABLE**
      </td>

      <td style={{ textAlign: "left" }}>
        The delivery of the shipment was not possible.
      </td>
    </tr>
  </tbody>
</Table>

***

## Final events

Final events are the stages of a shipment lifecycle where no further tracking statuses are sent after the event/milestone was hit. 

The following events are considered as the final events.

* All delivered events
* Recipient collected
* Shipment lost/destroyed
* Undeliverable - destroyed.

***

### List of tracking milestones and tracking events

The following table displays a comprehensive structure of the milestones, event codes, and events that occur throughout the shipping journey of a shipment.

<Image align="center" src="https://files.readme.io/1312237f5bcebd28d9d969bebf4a03fb61a27d49511ac12a3668ab47f40d1bf0-Tracking_milestones_list.png" />
