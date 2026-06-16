---
title: Shipments Webhook
excerpt: >-
  The _Shipments Webhook_ introduces an asynchronous approach to shipment
  creation, decoupling request processing from immediate label generation. 
deprecated: false
hidden: true
icon: fad fa-webhook
metadata:
  robots: index
---
This feature enhances system scalability, reduces response-time dependency, and provides greater flexibility for customers managing high‑volume operations.

## Key benefits

* Improved performance and reliability by removing synchronous dependencies 
* Scalability during peak periods through queued processing 
* Greater flexibility in handling shipment creation and label printing
* Enhanced user experience, enabling workflows such as pre-creating shipments for pick-and-pack operations and printing labels on demand

## Workflow

When a customer submits a request using the Create Shipment Async endpoint, the system:

Checks whether the Shipment Webhook is configured. Performs initial schema validation on the request.

If Shipment Webhook is not active:

The request is rejected with an error response (e.g. webhook inactive or not configured). Customers can fall back to the standard Create Shipment endpoint.

If Shipment Webhook is active:

The request is accepted and a RequestID is returned. The shipment is queued for asynchronous processing. Once processed, the system sends the result to the customer’s configured webhook endpoint:

A success response based on the requested action, or An error response if processing fails

## Retry process

If the system is unable to deliver the response to the customer’s webhook endpoint, it enters a retry process:

Failed responses are stored and retried automatically. If the webhook becomes suspended, pending responses are retained and delivered once it is reactivated. No new asynchronous shipment requests can be submitted while the webhook is suspended, preventing backlog buildup. Responses are stored in blob storage, ready for re-delivery. Data retention policies and storage capacity considerations apply to stored responses.

<br />
