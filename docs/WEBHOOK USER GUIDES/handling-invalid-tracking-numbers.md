---
title: Register tracking numbers via Trackings API
excerpt: >-
  The _Trackings API_ provides a scalable, webhook‑driven approach to Royal Mail
  shipment tracking. By registering tracking numbers explicitly, customers gain
  proactive shipment visibility while maintaining control over tracking
  duration, volume, and costs.
deprecated: false
hidden: false
icon: fad fa-calendar-circle-exclamation
metadata:
  robots: index
---
The [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API is an addition to the standard [tracking webhook](https://docs.intersoftsapient.net/docs/tracking-webhook) service, that automatically pushes tracking information for Royal Mail shipments created through INTERSOFT. This endpoint is intended for registering tracking numbers for shipments produced on other systems or different INTERSOFT accounts.

> 🚧 _Important_
>
> _This endpoint is only supported for Royal Mail shipments and is a chargeable API feature. Customers should ensure tracking registration is performed only when required to avoid unnecessary costs._

To enable tracking updates for Royal Mail shipments, tracking numbers must be explicitly registered with Intersoft using the POST /v4/trackings API. Once registered, Intersoft will monitor the shipment and push tracking updates to your configured webhook endpoint for a defined tracking period.
This approach is designed for customers who require:

* Automated shipment visibility
* Event‑driven tracking updates
* Integration‑based tracking without polling APIs

## Supported tracking period

* Tracking updates are retained and pushed for up to 30 days from registration.
* After the 30‑day tracking window expires, updates for the registered tracking numbers will no longer be generated.

## Processing behaviour

* Real-time tracking updates are delivered via webhook notifications.
* No historical tracking events are sent when a tracking number is registered. Only events occurring after registration are pushed.

## Troubleshooting

To ensure delivery reliability:

* If your webhook endpoint is temporarily unavailable, Intersoft will retry delivery.
* Tracking notifications are retried for up to 72 hours.
* After the retry window expires, undelivered events are discarded.

This ensures temporary outages on the customer side do not result in immediate data loss.

## Royal Mail supported products

Tracking registration is supported only for the following Royal Mail trackable services:

### Domestic Services

* Tracked Standard
* Tracked High Volume
* Tracked Returns
* Special Delivery

### International Services

* International Tracked
* International Signed
* International Tracked and Signed

Tracking registration requests submitted for unsupported products will not return tracking updates.

## Requests limits

* Up to 1,000 tracking numbers can be submitted in a single POST /v4/trackings request.
* Large submissions allow bulk registration of shipments with minimal API overhead.

## How it works

1. Create a Royal Mail shipment (or obtain valid Royal Mail tracking numbers).
2. Register the tracking numbers by submitting them to POST /v4/trackings
3. Intersoft begins monitoring the registered shipments.
4. Tracking updates are pushed to your webhook endpoint as events occur.

## Handle invalid tracking numbers 

The Sapient's [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API processes valid tracking numbers while isolating the invalid ones, providing clear feedback without failing the entire batch.

# Handle invalid tracking numbers

<Cards columns={2}>
  <Card title="Processing Behavior" icon="fa-cogs">
    * All tracking numbers in a request are accepted and inserted into the database (max 1000)
    * Invalid tracking numbers are marked as 'DO NOT TRACK' and not registered with the carrier
    * Requests does not fail if invalid numbers are present—only invalid entries are marked
    * Duplicate tracking numbers within the same batch are accepted
  </Card>

  <Card title="Invalid Tracking Events" icon="fa-exclamation-triangle">
    For each invalid tracking number, a tracking event is created and pushed via webhook.

    **Event Properties:**

    * **Event code:** `INVD`
    * **Event name:** Invalid Tracking Number
    * **Event type:** Tracking
    * **Milestone:** No
    * **Stop the clock:** Yes
  </Card>
</Cards>

> 📘 _Note_
>
> _The webhook payload includes mandatory fields as specified in the <Anchor label="push payload example" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample">push payload example</Anchor> section. Invalid tracking numbers are processed asynchronously to ensure valid shipments continue tracking without interruption._

***

### See also

<Cards columns="3">
  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>

<br />
