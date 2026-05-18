---
title: Tracking webhook
excerpt: '  INTERSOFT offers a comprehensive tracking webhook solution for receiving tracking events from carriers. The tracking data is sent to the customer’s endpoint configured in the tracking webhook setup.'
deprecated: false
hidden: false
icon: fad fa-calendar-clock
metadata:
  robots: index
---
The webhook operates using a POST API call, transmitting tracking events in a structured JSON format. This payload includes key shipment details such as tracking ID, tracking number, status tags, timestamps, event locations, and carrier‑specific metadata. The system ensures customers receive timely, accurate tracking updates throughout the parcel’s journey, offering full transparency from dispatch to delivery.

Wirth this solution, you can track:

<Cards columns="3">
  <Card title="SAPIENT Shipments" icon="box">
    Track all shipments created on the SAPIENT platform with comprehensive tracking data and real-time updates.
  </Card>

  <Card title="Intelligent Shipper" icon="truck">
    Monitor specific shipments created on Intelligent Shipper for targeted tracking capabilities.
  </Card>

  <Card title="Royal Mail Integration" icon="mail-bulk">
    Track Royal Mail shipments created on any external shipping platform or by individuals.
  </Card>
</Cards>

To start receiving tracking updates, customers must configure their webhook within the INTERSOFT platform. Once enabled, the webhook can be tailored to send either milestones only or all tracking events, depending on business needs. This flexibility allows organisations to manage their data flow efficiently while maintaining full visibility of parcel movement.

***

In this section, learn how to manage your tracking webhook by accessing the following essential functions:

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>
</Cards>

<Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
  Understand tracking events and milestone data.
</Card> 

<Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
  Register Royal Mail tracking numbers with the Trackings API to receive webhook updates for eligible shipments created outside your standard INTERSOFT tracking flow.
</Card>

<br />
