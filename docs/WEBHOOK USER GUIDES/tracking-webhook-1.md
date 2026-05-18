---
title: Webhooks
excerpt: >-
  Learn how INTERSOFT webhooks send tracking and manifest updates to your
  configured endpoint.
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
Use INTERSOFT webhooks to receive real-time shipment and manifest updates at an endpoint you control.

A webhook sends event data from one application to another. When an event occurs, the sending application issues a `POST` request containing the payload to the receiving application’s endpoint. Unlike traditional request–response APIs, the receiving application hosts the endpoint, not the sender.

INTERSOFT supports two webhook types:

- **<Glossary>Tracking webhook</Glossary>**: Receives tracking events from carriers and sends the data directly to your configured endpoint.
- **Manifest webhook**: Works with asynchronous manifesting and notifies your configured endpoint when a manifest request has completed processing. The notification includes the final status: successful or failed.

***

## Get started

Choose the guide that matches the webhook task you want to complete:

<Cards columns="3">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.02/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Configure an endpoint to receive shipment tracking status updates.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Receive notifications when asynchronous manifest processing completes.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Review webhook suspension behaviour and restore delivery.
  </Card>
</Cards>