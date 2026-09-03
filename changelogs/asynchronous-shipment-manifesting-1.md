---
title: Asynchronous shipment manifesting
author: Syed Haroon Shah
hidden: true
published_at: '2025-10-23T11:24:07.343Z'
type: added
---
A fully asynchronous shipment manifesting process has been introduced across the SAPIENT API and UI, allowing customers to submit manifest requests without waiting for completion.

* **API endpoints**: The following two new endpoints have been added to our existing **Manifests** API endpoint.
  * **Manifest Shipments Async**. To submit the manifest requests to be processed asynchronously. This endpoint accepts the same parameters as the existing [Manifests](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode#/) endpoint, excluding the **async** parameter.
  * **Get Manifest Request Status**: To check the status of the submitted manifest request with optional detailed responses, including manifest images when complete.
* **Manifest webhook**: To configure a manifest webhook via the UI to receive automatic updates when a manifest request completes or fails, with retry logic and suspension handling.
* **Manifest via UI**: To get real-time progress on async manifest in a separate pop-up dialog and access to completed manifests through the **Manifest History** page.