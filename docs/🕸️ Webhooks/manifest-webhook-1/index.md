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
