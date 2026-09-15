---
title: Shipment Webhook and Asynchronous Shipment Creation
author: Weronika Kucharska
hidden: true
published_at: '2026-08-25T13:39:03.956Z'
type: added
---
A new asynchronous shipment creation workflow is available through the **Create Shipment Async&#x20;**&#x65;ndpoint, enabling shipment requests to be processed in the background and responses to be delivered to a configured Shipment Webhook endpoint.

<Callout icon="📘" theme="info">
  ### _Note_

  _For more information, refer to the&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-async-rm">_Create Shipment Async_</Anchor>_&#x20;endpoint._
</Callout>

When using this endpoint, Sapient performs initial validation and immediately **returns a Request ID**. The shipment request is then processed asynchronously. Once processing is complete, the **Create Shipment response is pushed to the configured Shipment Webhook endpoint.** Successful responses include shipment details, generated labels, and any applicable customs documentation, while failed requests return the relevant error details.

Key capabilities include:

- Available across all supported carriers.
- Support for all shipment actions: Process, Allocate, Create, and default Process behaviour when no action is specified.
- Shipment Webhook configuration through the Sapient user interface.
- Automatic retry handling for failed webhook deliveries, with pending responses retained and resent when the webhook is reactivated.

This functionality helps reduce API response-time dependency, improve scalability during high-volume periods, and provide greater flexibility for customers who wish to separate shipment creation from downstream label generation, documentation generation, and fulfilment processes.

<br />