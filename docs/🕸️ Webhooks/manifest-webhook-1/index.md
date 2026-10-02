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
Manifest webhook eliminates the need to repeatedly check the status endpoint and provide near real-time updates when a <Glossary>manifest</Glossary> is processed, improving efficiency when handling large volumes of shipments.

Instead of polling the [Get Manifest Request](https://docs.intersoftsapient.net/reference/get_v4-manifests-manifeststatus-manifestrequestid) Status endpoint at regular intervals, the system sends a webhook notification to a configured endpoint whenever the status of the manifest request changes or processing is completed.

This solution is particularly useful for customers processing large shipment volumes, where manifest generation may take time to complete. By using webhooks, integrations can react immediately when manifests are available, improving efficiency and reducing unnecessary API traffic.

With this solution you can:&#x20;

- Manifest processing: Receive notifications when a manifest request has been successfully processed and manifests have been created.
- Monitor status: Track the progress of asynchronous manifest requests without polling the status endpoint.
- Mange high-volume operations: Efficiently manage large manifest batches that require background processing.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before configuring a Manifest Webhook, ensure that a webhook endpoint has been created and authenticated within SAPIENT. Once enabled, manifest status notifications will be delivered automatically whenever a manifest request status changes._
</Callout>

## Workflow

After submitting the request to the **Manifest Shipments Async** endpoint, the system processes the request as follows:

1. Receives the manifest request and assigns a unique **manifestRequestId**.
2. Processes the request asynchronously in the background.
3. Updates the manifest request status throughout processing.
4. Sends a webhook notification when the status changes or processing completes.
5. The receiving application can use the **manifestRequestId** to retrieve detailed manifest information through the **Get Manifest Request Status** endpoint if required.

## Getting started

<Cards columns="3">
  <Card title="Set Up Manifest Webhook Connection" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-code-pull-request" target="_blank">
    Configure and receive notifications when asynchronous manifest processing completes
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Review webhook suspension behaviour and restore delivery.
  </Card>

  <Card title="Manifest Shipments Async" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-async-carriercode" icon="fad fa-square-plus" target="_blank">
    Manifest a shipment request using this endpoint for asynchronous processing.
  </Card>
</Cards>
