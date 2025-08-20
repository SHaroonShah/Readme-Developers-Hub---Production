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
icon: fad fa-timeline-arrow
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
      <th>
        Milestone
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **IT'S ON IT'S WAY**
      </td>

      <td>
        The <Glossary>shipment</Glossary> was handed over or is on its way to the <Glossary>carrier</Glossary>.
      </td>
    </tr>

    <tr>
      <td>
        **IN TRANSIT**
      </td>

      <td>
        The shipment is travelling through the carrier's network.
      </td>
    </tr>

    <tr>
      <td>
        **TRANSIT DELAY**
      </td>

      <td>
        The shipment processing through the carrier's network is delayed.
      </td>
    </tr>

    <tr>
      <td>
        **IN CUSTOMS**
      </td>

      <td>
        The shipment is undergoing customs inspections.

        *`Note`: this is applicable to international shipments only.*
      </td>
    </tr>

    <tr>
      <td>
        **OUT FOR DELIVERY**
      </td>

      <td>
        The shipment is on the way to the recipient.
      </td>
    </tr>

    <tr>
      <td>
        **DELIVERY ATTEMPT FAILED**
      </td>

      <td>
        The delivery was attempted, but failed.
      </td>
    </tr>

    <tr>
      <td>
        **READY FOR COLLECTION**
      </td>

      <td>
        The shipment was left at a chosen location for the recipient to collect.
      </td>
    </tr>

    <tr>
      <td>
        **DELIVERED**
      </td>

      <td>
        The shipment was successfully delivered to the recipient (or another person/place chosen by the recipient).
      </td>
    </tr>

    <tr>
      <td>
        **COLLECTED**
      </td>

      <td>
        The shipment was successfully collected from the collection point.
      </td>
    </tr>

    <tr>
      <td>
        **PART DELIVERED**
      </td>

      <td>
        The part of a consignment shipment was delivered successfully.
      </td>
    </tr>

    <tr>
      <td>
        **UNDELIVERABLE**
      </td>

      <td>
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

<Image align="center" border={true} caption="Intersoft milestones and tracking event codes" src="https://files.readme.io/b1700586e9f4dcf22e7ad38f9fa200672bf8ee2ecf5740f71683472dbd90d26f-Tracking_webhook_milestones_and_events_latest.png" />