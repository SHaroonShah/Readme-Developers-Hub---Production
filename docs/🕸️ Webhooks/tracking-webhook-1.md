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
Use INTERSOFT webhooks to receive real-time <Glossary>shipment</Glossary> and <Glossary>manifest</Glossary> updates at an endpoint you control.

A webhook sends event data from one application to another. When an event occurs, the sending application issues a `POST` request containing the payload to the receiving application’s endpoint. Unlike traditional request–response APIs, the receiving application hosts the endpoint, not the sender.

INTERSOFT supports two webhook types:

- **Tracking webhook**: Receives tracking events from carriers and sends the data directly to your configured endpoint.
- **Manifest webhook**: Works with [asynchronous manifesting](https://docs.intersoftsapient.net/docs/manifest-shipment-asychronously) and notifies your configured endpoint when a manifest request has completed processing. The notification includes the final status—successful or failed.
- **Shipment webhook**: Create shipments asynchronously and receive processing results at your configured webhook endpoint.

***

## Get started

Choose the guide that matches the webhook task you want to complete:

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.04/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request" target="_blank">
    Configure an endpoint to receive shipment tracking status updates.
  </Card>

  <Card title="Set Up Manifest Webhook Connection" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook" target="_blank">
    Receive notifications when asynchronous manifest processing completes.
  </Card>

  <Card title="Set up Shipment Webhook Connection">
    Create a shipment request using this endpoint for asynchronous processing.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Review webhook suspension behaviour and restore delivery.
  </Card>
</Cards>
