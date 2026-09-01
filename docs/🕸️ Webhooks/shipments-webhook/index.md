---
title: Shipment Webhook
excerpt: >-
  Use the Shipment Webhook to create shipments asynchronously and receive
  processing results at your configured webhook endpoint.
deprecated: false
hidden: true
icon: fad fa-webhook
metadata:
  robots: index
---
Use the _Shipment Webhook_ to create shipments asynchronously, so you can submit shipment requests without waiting for immediate label generation.

Asynchronous processing separates request submission from label generation. This supports high-volume operations and lets you prepare shipments for pick-and-pack workflows before printing labels on demand.

## Key benefits

- Improves performance and reliability by removing synchronous dependencies.
- Scales processing during peak periods through queued requests.
- Gives you flexibility over shipment creation and label printing.
- Supports pre-created shipments and on-demand label printing.

## Workflow

Submit a request to the **Create Shipment Async** endpoint. The system processes the request as follows:

1. Checks whether the **Shipment Webhook** is configured.
2. Performs initial schema validation on the request.
3. Handles the request according to the webhook status.

<Tabs>
  <Tab title="Webhook inactive">
    The system rejects the request with an error response, such as a webhook inactive or not configured error. You can use the standard **Create Shipment** endpoint instead.
  </Tab>

  <Tab title="Webhook active">
    The system accepts the request and returns a **RequestID**. It queues the shipment for asynchronous processing and sends the result to your configured webhook endpoint when processing finishes.

    The result contains either a success response for the requested action or an error response if processing fails.
  </Tab>
</Tabs>

## Retry process

If the system cannot deliver a response to your webhook endpoint, it stores the failed response and retries delivery automatically.

When the webhook is suspended, the system retains pending responses and delivers them after you reactivate the webhook. You cannot submit new asynchronous shipment requests while the webhook is suspended, which prevents the backlog from increasing.

The system stores responses in blob storage for re-delivery. Data-retention policies and storage-capacity considerations apply to stored responses.

***
## Getting started

<Cards columns="2">
  <Card title="Set Up Shipment Webhook Connection" href="https://docs.intersoftsapient.net/v4.04/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request" target="_blank">
    Automate the instantaneous flow of information regarding your shipments.
  </Card>
</Cards>
