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
The application sending the data issues a POST API call containing the payload to the receiving application. The endpoint is hosted by the receiving application, not the sender, unlike traditional request–response APIs. 

INTERSOFT offers comprehensive webhook solutions, including the <Glossary>tracking webhook</Glossary> and manifest webhook. The tracking webhook enables customers to receive tracking events from carriers, with data delivered directly to the configured endpoint. The manifest webhook, used alongside asynchronous manifesting, notifies customers when a manifest request has completed processing, sending the final status (successful or failed) to the configured endpoint without the need for polling.

***

## Get started

In this section, learn how to manage your webhooks by accessing the following essential functions:

<Cards columns="3">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>
