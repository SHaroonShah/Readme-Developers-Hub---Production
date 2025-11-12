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
/cusIn SAPIENT, while [configuring the tracking webhook](https://docs.intersoftsapient.net/docs/create-tracking-webhook), You can choose to receive <Glossary>all tracking events</Glossary> or tracking <Glossary>milestones</Glossary> only.

* If you select to receive milestones only, the system only pushes the tracking when a new milestone is triggered.
* If you select to receive full tracking events, then the system pushes the tracking every time it receives a new tracking event from the carrier, regardless of whether the tracking event triggers a new milestone or not.

***

## Milestones

_Milestones_ refer to significant stages within the shipment process that are essential for monitoring process, such as order created, label printed, out for delivery, and so on.

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
        **IT'S ON ITS WAY**
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

        _`Note`: this is applicable to international shipments only._
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

<Image align="center" border={true} caption="Intersoft milestones and tracking event codes" src="https://files.readme.io/b1bbca49f16a96a5b27941ec0f42315cb937cf2541b6b0a6021cb9f03e317333-Tracking_milestones_list.png" />

> 📘 _Note_
>
> _The **ICLR**, **IARR**, and **IRCO** tracking events have not been allocated to any milestones._

<HTMLBlock>{`
<table>
  <tr>
    <th>Milestone Name</th>
    <th>Milestone Order</th>
    <th>Tracking Event Code</th>
    <th>Tracking Event Name</th>
  </tr>
  <tr>
    <td rowspan="5">It’s on its Way</td>
    <td rowspan="5">1</td>
    <td>PSRE</td>
    <td>Shipment Received</td>
  </tr>
  <tr>
    <td></td>
    <td>PSAN</td>
    <td>Shipment Announced</td>
  </tr>
  <tr>
    <td></td>
    <td>PSCO</td>
    <td>Shipment Collected</td>
  </tr>
  <tr>
    <td></td>
    <td>PSDE</td>
    <td>Shipment Despatched</td>
  </tr>
  <tr>
    <td rowspan="5">In Transit</td>
    <td>2</td>
    <td>PINT</td>
    <td>In Transit</td>
  </tr>
  <tr>
    <td></td>
    <td>PPID</td>
    <td>Shipment Processed in Depot</td>
  </tr>
  <tr>
    <td></td>
    <td>PRID</td>
    <td>Shipment Received in Depot</td>
  </tr>
  <tr>
    <td></td>
    <td>PSDD</td>
    <td>Shipment Departed Depot</td>
  </tr>
  <tr>
    <td></td>
    <td>IOWS</td>
    <td>Oversize/weight Shipment</td>
  </tr>
  <tr>
    <td rowspan="3">In Customs</td>
    <td>3</td>
    <td>BCUI</td>
    <td>Customs Inspection</td>
  </tr>
  <tr>
    <td></td>
    <td>BHBC</td>
    <td>Held by Customs</td>
  </tr>
  <tr>
    <td></td>
    <td>BRBC</td>
    <td>Released by Customs</td>
  </tr>
  <tr>
    <td rowspan="6">Out for Delivery</td>
    <td>4</td>
    <td>POFD</td>
    <td>Out for Delivery</td>
  </tr>
  <tr>
    <td rowspan="6">Delivery Attempt Failed</td>
    <td>5</td>
    <td>FDAF</td>
    <td>Delivery Attempt Failed</td>
  </tr>
  <tr>
    <td></td>
    <td>FNCO</td>
    <td>Not Collected</td>
  </tr>
  <tr>
    <td></td>
    <td>FCAR</td>
    <td>No Answer - Carded</td>
  </tr>
  <tr>
    <td></td>
    <td>FANK</td>
    <td>Address not known</td>
  </tr>
  <tr>
    <td></td>
    <td>FRNK</td>
    <td>Recipient not known</td>
  </tr>
  <tr>
    <td></td>
    <td>FRAA</td>
    <td>Refused at Delivery Address</td>
  </tr>
  <tr>
    <td rowspan="6">Part Delivered</td>
    <td>6</td>
    <td>DPAR</td>
    <td>Partially delivered</td>
  </tr>
  <tr>
    <td rowspan="6">Ready for Collection</td>
    <td>7</td>
    <td>DRFC</td>
    <td>Ready for Collection</td>
  </tr>
  <tr>
    <td rowspan="6">Delivered</td>
    <td>8</td>
    <td>DELV</td>
    <td>Delivered</td>
  </tr>
  <tr>
    <td></td>
    <td>DTSP</td>
    <td>Delivered to Safe Place</td>
  </tr>
  <tr>
    <td></td>
    <td>DPOB</td>
    <td>Delivered to PO Box</td>
  </tr>
  <tr>
    <td></td>
    <td>DDMG</td>
    <td>Delivered Damaged</td>
  </tr>
  <tr>
    <td></td>
    <td>DTNB</td>
    <td>Delivered to Neighbour - No Signature</td>
  </tr>
  <tr>
    <td></td>
    <td>DTNS</td>
    <td>Delivered to Neighbour with Signature</td>
  </tr>
  <tr>
    <td rowspan="4">Collected</td>
    <td>9</td>
    <td>DRCO</td>
    <td>Recipient Collected</td>
  </tr>
  <tr>
    <td rowspan="3">Undeliverable</td>
    <td>10</td>
    <td>RTNS</td>
    <td>Return to Sender</td>
  </tr>
  <tr>
    <td></td>
    <td>RUND</td>
    <td>Undeliverable - Return to Sender</td>
  </tr>
  <tr>
    <td></td>
    <td>RNCO</td>
    <td>Not Collected - Return to Sender</td>
  </tr>
  <tr>
    <td rowspan="5">Transit Delay</td>
    <td>Null</td>
    <td>IDIP</td>
    <td>Delay in Processing</td>
  </tr>
  <tr>
    <td></td>
    <td>IFME</td>
    <td>Force Majure/ Exceptional Event</td>
  </tr>
  <tr>
    <td></td>
    <td>ISMI</td>
    <td>Shipment Misrouted</td>
  </tr>
  <tr>
    <td></td>
    <td>PRET</td>
    <td>Shipment Retention</td>
  </tr>
  <tr>
    <td rowspan="3">N/A</td>
    <td>Null</td>
    <td>ICLR</td>
    <td>Shipment Customs Cleared</td>
  </tr>
  <tr>
    <td></td>
    <td>IARR</td>
    <td>Shipment Arrived at Facility</td>
  </tr>
  <tr>
    <td></td>
    <td>IRCO</td>
    <td>Shipment Ready for Collection from the Facility</td>
  </tr>
</table>
`}</HTMLBlock>

<br />
