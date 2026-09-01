---
title: Set up Shipment Webhook connection
excerpt: >-
  Shipment Webhook is a customer-configured webhook endpoint that receives the
  results of asynchronous shipment creation requests. Instead of waiting for the
  shipment to be processed synchronously, SAPIENT immediately returns a Request
  ID and then sends the completed shipment response (including labels and
  carrier details) to the customer's webhook endpoint once processing finishes.
deprecated: false
hidden: true
icon: fad fa-webhook
metadata:
  robots: index
---
This functionality helps reduce API response-time dependency, improve scalability during high-volume periods, and provide greater flexibility for customers who wish to separate shipment creation from downstream label generation, documentation generation, and fulfilment processes

# How it works

1. The customer calls the [Create Shipment Async](https://docs.intersoftsapient.net/reference/post_v4-shipments-async-rm) endpoint.
2. SAPIENT performs initial validation and immediately returns a **Request ID**.
3. The shipment is processed in the background.
4. Once complete, SAPIENT sends the shipment result to the customer's configured webhook URL. The response can contain successful shipment details, labels, carrier information, or processing errors.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before calling the Create shipment Async endpoint, you must configure the shipment webhook via the SAPIENT UI._
</Callout>

##
