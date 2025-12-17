---
title: Webhooks
excerpt: >-
  _Webhooks_ are valuable tools for receiving real-time updates and data from
  various services and applications. They allow you to automate workflows,
  integrate systems, and stay up to date on important events.
deprecated: false
hidden: false
icon: fad fa-webhook
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The application sending the data sends a **POST** API call containing the data to the receiving application​. The endpoint is hosted by the application receiving the data, not the application sending the data as with a request and response-based API​.

INTERSOFT offers a comprehensive <Glossary>tracking webhook</Glossary> solution for receiving tracking events from carriers. The tracking data is sent to the customer’s endpoint configured in the tracking webhook setup.

With this solution, you can track:

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

***

## Get started

In this section, learn how to:

<Cards columns="3">
  <Card title="Add Tracking Webhook" href="https://docs.intersoftsapient.net/docs/create-tracking-webhook" icon="fa-solid fa-calendar-circle-plus">
    Configure your webhook endpoint to receive tracking data.
  </Card>

  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments. 
  </Card>

  <Card title="Set Up Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>
