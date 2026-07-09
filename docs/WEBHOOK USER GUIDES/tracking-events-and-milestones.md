---
title: Track events and milestones
excerpt: >-
  This setting enables the monitoring and logging of every possible event and
  milestone related to a shipment throughout its lifecycle.
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

- If you select to receive milestones only, the system only pushes the tracking when a new milestone is triggered.
- If you select to receive full tracking events, then the system pushes the tracking every time it receives a new tracking event from the carrier, regardless of whether the tracking event triggers a new milestone or not.

***

## Milestones

_Milestones_ refer to significant stages within the shipment process that are essential for monitoring process, such as order created, label printed, out for delivery, and so on.

If you choose to receive tracking milestones, bear in mind that each milestone only gets triggered once. To understand each milestone and its expected order of occurrence, refer to the information explained in the following table:

<Accordion title="My Accordion Title" icon="fa-info-circle">
  <HTMLBlock>{`
<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Milestone
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        <stron>IT'S ON ITS WAY</strong>
      </td>

      <td>
        The <Glossary>shipment</Glossary> was handed over or is on its way to the <Glossary>carrier</Glossary>.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN TRANSIT**
      </td>

      <td>
        The shipment is travelling through the carrier's network.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **TRANSIT DELAY**
      </td>

      <td>
        The shipment processing through the carrier's network is delayed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN CUSTOMS**
      </td>

      <td>
        The shipment is undergoing customs inspections.

        \`Note\`_: this is applicable to international shipments only._
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **OUT FOR DELIVERY**
      </td>

      <td>
        The shipment is on the way to the recipient.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERY ATTEMPT FAILED**
      </td>

      <td>
        The delivery was attempted, but failed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **READY FOR COLLECTION**
      </td>

      <td>
        The shipment was left at a chosen location for the recipient to collect.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERED**
      </td>

      <td>
        The shipment was successfully delivered to the recipient (or another person/place chosen by the recipient).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **COLLECTED**
      </td>

      <td>
        The shipment was successfully collected from the collection point.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **PART DELIVERED**
      </td>

      <td>
        The part of a consignment shipment was delivered successfully.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **UNDELIVERABLE**
      </td>

      <td>
        The delivery of the shipment was not possible.
      </td>
    </tr>
  </tbody>
</Table>
`}</HTMLBlock>
</Accordion>



<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Milestone
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **IT'S ON ITS WAY**
      </td>

      <td>
        The <Glossary>shipment</Glossary> was handed over or is on its way to the <Glossary>carrier</Glossary>.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN TRANSIT**
      </td>

      <td>
        The shipment is travelling through the carrier's network.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **TRANSIT DELAY**
      </td>

      <td>
        The shipment processing through the carrier's network is delayed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **IN CUSTOMS**
      </td>

      <td>
        The shipment is undergoing customs inspections.

        `Note`_: this is applicable to international shipments only._
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **OUT FOR DELIVERY**
      </td>

      <td>
        The shipment is on the way to the recipient.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERY ATTEMPT FAILED**
      </td>

      <td>
        The delivery was attempted, but failed.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **READY FOR COLLECTION**
      </td>

      <td>
        The shipment was left at a chosen location for the recipient to collect.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **DELIVERED**
      </td>

      <td>
        The shipment was successfully delivered to the recipient (or another person/place chosen by the recipient).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **COLLECTED**
      </td>

      <td>
        The shipment was successfully collected from the collection point.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **PART DELIVERED**
      </td>

      <td>
        The part of a consignment shipment was delivered successfully.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
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

- All delivered events
- Recipient collected
- Shipment lost/destroyed
- Undeliverable - destroyed.

***

### List of tracking milestones and tracking events

The following section displays a comprehensive structure of the milestones, event codes, and events that occur throughout the shipping journey of a shipment.

<Accordion title="Tracking Events and Milestones" icon="fa-duotone fa-solid fa-display-chart-up">
  <HTMLBlock>{`
                            <table>
                              <tr>
                                <th style="background-color: #778899;">Milestone Name</th>
                                <th style="background-color: #778899;">Milestone Order</th>
                                <th style="background-color: #778899;">Tracking Event Code</th>
                                <th style="background-color: #778899;">Tracking Event Name</th>
                              </tr>
                              <tr>
                                <td rowspan="4"><strong>It’s on its Way</strong></td>
                                <td rowspan="4">1</td>
                                <td>PSRE</td>
                                <td>Shipment Received</td>
                            </tr>
                              <tr>
                                <td>PSAN</td>
                                <td>Shipment Announced</td>
                              </tr>
                              <tr>
                                <td>PSCO</td>
                                <td>Shipment Collected</td>
                              </tr>
                              <tr>
                                <td>PSDE</td>
                                <td>Shipment Despatched</td>
                              </tr>
                              <tr>
                                <td rowspan="5"><strong>In Transit</strong></td>
                                <td rowspan="5">2</td>
                                <td>PINT</td>
                                <td>In Transit</td>
                              </tr>
                              <tr>
                                <td>PPID</td>
                                <td>Shipment Processed in Depot</td>
                              </tr>
                              <tr>
                                <td>PRID</td>
                                <td>Shipment Received in Depot</td>
                              </tr>
                              <tr>
                                <td>PSDD</td>
                                <td>Shipment Departed Depot</td>
                              </tr>
                              <tr>
                                <td>IOWS</td>
                                <td>Oversize/weight Shipment</td>
                              </tr>
                              <tr>
                                <td rowspan="3"><strong>In Customs</strong></td>
                                <td rowspan="3">3</td>
                                <td>BCUI</td>
                                <td>Customs Inspection</td>
                              </tr>
                              <tr>
                                <td>BHBC</td>
                                <td>Held by Customs</td>
                              </tr>
                              <tr>
                                <td>BRBC</td>
                                <td>Released by Customs</td>
                              </tr>
                              <tr>
                                <td rowspan="1"><strong>Out for Delivery</strong></td>
                                <td>4</td>
                                <td>POFD</td>
                                <td>Out for Delivery</td>
                              </tr>
                              <tr>
                                <td rowspan="8"><strong>Delivery Attempt Failed</strong></td>
                                <td rowspan="8">5</td>
                                <td>FDAF</td>
                                <td>Delivery Attempt Failed</td>
                              </tr>
                              <tr>
                                <td>FNCO</td>
                                <td>Not Collected</td>
                              </tr>
                              <tr>
                                <td>FCAR</td>
                                <td>No Answer - Carded</td>
                              </tr>
                              <tr>
                                <td>FANK</td>
                                <td>Address Not Known</td>
                              </tr>
                              <tr>
                                <td>FRNK</td>
                                <td>Recipient Not Known</td>
                              </tr>
                              <tr>
                                <td>FRAA</td>
                                <td>Refused at Delivery Address</td>
                              </tr>
                              <tr>
                                <td>FINA</td>
                                <td>Incomplete Address</td>
                              </tr>
                              <tr>
                                <td>FUTA</td>
                                <td>Unable to Access Delivery Point</td>
                              </tr>
                              <tr>
                                <td rowspan="1"><strong>Part Delivered</strong></td>
                                <td>6</td>
                                <td>DPAR</td>
                                <td>Partially delivered</td>
                              </tr>
                              <tr>
                                <td rowspan="1"><strong>Ready for Collection</strong></td>
                                <td>7</td>
                                <td>DRFC</td>
                                <td>Ready for Collection</td>
                              </tr>
                              <tr>
                                <td rowspan="8"><strong>Delivered</strong></td>
                                <td rowspan="8">8</td>
                                <td>DELV</td>
                                <td>Delivered</td>
                              </tr>
                              <tr>
                                <td>DTSP</td>
                                <td>Delivered to Safe Place</td>
                              </tr>
                              <tr>
                                <td>DPOB</td>
                                <td>Delivered to PO Box</td>
                              </tr>
                              <tr>
                                <td>DDMG</td>
                                <td>Delivered Damaged</td>
                              </tr>
                              <tr>
                                <td>DTNB</td>
                                <td>Delivered to Neighbour - No Signature</td>
                              </tr>
                              <tr>
                                <td>DTNS</td>
                                <td>Delivered to Neighbour with Signature</td>
                              </tr>
                            <tr>
                                <td>DNSV</td>
                                <td>Delivered to Neighbour with Signature - ID Verified</td>
                              </tr>
                            <tr>
                                <td>DNSO</td>
                                <td>Delivered to Neighbour with Signature - Over 25</td>
                              </tr>
                              <tr>
                                <td rowspan="1"><strong>Collected</strong></td>
                                <td>9</td>
                                <td>DRCO</td>
                                <td>Recipient Collected</td>
                              </tr>
                              <tr>
                                <td rowspan="7"><strong>Undeliverable</strong></td>
                                <td rowspan="7">10</td>
                                <td>RTNS</td>
                                <td>Return to Sender</td>
                              </tr>
                              <tr>
                                <td>RUND</td>
                                <td>Undeliverable - Return to Sender</td>
                              </tr>
                              <tr>
                                <td>RNCO</td>
                                <td>Not Collected - Return to Sender</td>
                              </tr>
                              <tr>
                                <td>UDTS</td>
                                <td>Delivered to Sender</td>
                              </tr>
                              <tr>
                                <td>IDES</td>
                                <td>Shipment Lost/Destroyed</td>
                              </tr>
                              <tr>
                                <td>ICAN</td>
                                <td>Shipment Cancelled</td>
                              </tr>
                              <tr>
                                <td>FUDS</td>
                                <td>Undeliverable - Destroyed</td>
                              </tr>

                              <tr>
                                <td rowspan="4"><strong>Transit Delay</strong></td>
                                <td rowspan="4">Null</td>
                                <td>IDIP</td>
                                <td>Delay in Processing</td>
                              </tr>
                              <tr>
                                <td>IFME</td>
                                <td>Force Majeure/ Exceptional Event</td>
                              </tr>
                              <tr>
                                <td>ISMI</td>
                                <td>Shipment Misrouted</td>
                              </tr>
                              <tr>
                                <td>PRET</td>
                                <td>Shipment Retention</td>
                              </tr>
                              <tr>
                                <td rowspan="3"><strong>N/A</strong></td>
                                <td rowspan="3">Null</td>
                                <td>ICLR</td>
                                <td>Shipment Customs Cleared</td>
                              </tr>
                              <tr>
                                <td>IARR</td>
                                <td>Shipment Arrived at Facility</td>
                              </tr>
                              <tr>
                                <td>IRCO</td>
                                <td>Shipment Ready for Collection from the Facility</td>
                              </tr>
                            </table>
  `}</HTMLBlock>

  > 📘 *Note*
  >
  > *The**ICLR**, **IARR**, and **IRCO** tracking events have not been allocated to any milestones.*
</Accordion>

***

### See also

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>

<br />
