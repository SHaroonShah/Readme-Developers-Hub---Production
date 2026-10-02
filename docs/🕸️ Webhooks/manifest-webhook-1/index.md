---
title: Manifest Webhook
excerpt: >-
  a _Manifest Webhook_ is a feature that allows customers to receive real-time
  notifications about the manifest request. It is used alongside a Manifest
  Async endpoint, which processes large shipment manifests in the background.
deprecated: false
hidden: false
icon: fad fa-truck-ramp
link:
  new_tab: false
metadata:
  robots: index
---
Use the _Manifest Webhook_ to receive near real-time updates when a <Glossary>manifest</Glossary> request changes status or finishes processing.

The webhook sends notifications to your configured endpoint, so you do not need to poll the manifest request status endpoint. This is useful when large batches of shipments take time to process.

## Key benefits

- Receive notifications when a manifest request has been processed and manifests have been created.
- Monitor asynchronous manifest requests without repeatedly polling the status endpoint.
- Manage large manifest batches while they process in the background.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before configuring a Manifest Webhook, ensure that a webhook endpoint has been created and authenticated within SAPIENT. Once enabled, manifest status notifications will be delivered automatically whenever a manifest request status changes._
</Callout>

## Workflow

After you submit a request to the **Manifest Shipments Async** endpoint, the system processes it as follows:

1. Receives the manifest request and assigns a unique **manifestRequestId**.
2. Processes the request asynchronously in the background.
3. Updates the manifest request status during processing.
4. Sends a webhook notification when the status changes or processing finishes.

<Callout icon="💡" theme="default">
  ### _Tip_

  _If you need more detail about a manifest request, use its&#x20;_**_manifestRequestId_**_&#x20;with the&#x20;_[_Get Manifest Request Status_](https://docs.intersoftsapient.net/reference/get_v4-manifests-manifeststatus-manifestrequestid)_&#x20;endpoint. You do not need to poll this endpoint to receive webhook updates._
</Callout>

***

## Getting started

<Cards columns="3">
  <Card title="Set Up Manifest Webhook Connection" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-code-pull-request" target="_blank">
    Configure your endpoint to receive notifications about asynchronous manifest processing.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Review webhook suspension behaviour and restore delivery.
  </Card>

  <Card title="Manifest Shipments Async" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-async-carriercode" icon="fad fa-square-plus" target="_blank">
    Manifest a shipment request using this endpoint for asynchronous processing.
  </Card>
</Cards>
