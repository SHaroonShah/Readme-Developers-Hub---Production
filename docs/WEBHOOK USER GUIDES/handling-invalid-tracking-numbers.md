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
Register Royal Mail tracking numbers with the [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API to receive webhook updates for eligible shipments created outside your standard INTERSOFT tracking flow.

> 🚧 _Important_
>
> _This endpoint is only supported for Royal Mail shipments and is a chargeable API feature. Customers should ensure tracking registration is performed only when required to avoid unnecessary costs._

INTERSOFT monitors each registered tracking number and pushes new events to your configured webhook for a defined tracking period.

Use this endpoint when you need:

* Automated shipment visibility
* Event‑driven tracking updates
* Integration‑based tracking without polling APIs

<Cards columns={3}>
  <Card title="Royal Mail only" icon="fa-truck">
    This endpoint supports Royal Mail shipments only.
  </Card>

  <Card title="30-day tracking window" icon="fa-calendar">
    Tracking updates are retained and pushed for up to 30 days from registration.
  </Card>

  <Card title="Batch Processing" icon="fa-boxes-stacked">
    Submit up to 1,000 tracking numbers in a single `POST /v4/trackings` request.
  </Card>
</Cards>

# How it works

1. Create a Royal Mail shipment, or obtain valid Royal Mail tracking numbers.
2. Register the tracking numbers by submitting them to `POST /v4/trackings`.
3. INTERSOFT begins monitoring the registered shipments.
4. INTERSOFT pushes tracking updates to your webhook endpoint as events occur.

## Tracking window and delivery behaviour

* Tracking updates are retained and pushed for up to 30 days from registration.
* After the 30‑day tracking window expires, updates for the registered tracking numbers are no longer generated.
* Real-time tracking updates are delivered through webhook notifications.
* No historical tracking events are sent when a tracking number is registered. INTERSOFT pushes only events that occur after registration.

## Retry behaviour

If your webhook endpoint is temporarily unavailable, INTERSOFT retries delivery for up to 72 hours. After the retry window expires, undelivered events are discarded.

## Supported Royal Mail products

Tracking registration is supported only for the following Royal Mail trackable services:

<Columns layout="auto">
  <Column>
    ### Domestic services

    * Tracked Standard
    * Tracked High Volume
    * Tracked Returns
    * Special Delivery
  </Column>

  <Column>
    ### International services

    * International Tracked
    * International Signed
    * International Tracked and Signed
  </Column>
</Columns>

Tracking registration requests submitted for unsupported products will not return tracking updates.

# Handle invalid tracking numbers

If a batch contains invalid tracking numbers, the [Trackings](https://docs.intersoftsapient.net/reference/post_v4-trackings) API continues processing the valid ones and reports the invalid entries separately.

<Cards columns={2}>
  <Card title="Processing behaviour" icon="fa-cogs">
    * All tracking numbers in a request are accepted and inserted into the database, up to 1,000 entries per request.
    * Invalid tracking numbers are marked as `DO NOT TRACK` and are not registered with the carrier.
    * The request does not fail when invalid numbers are present.
    * Duplicate tracking numbers within the same batch are accepted.
  </Card>

  <Card title="Invalid tracking event" icon="fa-exclamation-triangle">
    For each invalid tracking number, Intersoft creates a tracking event and pushes it to your webhook.

    **Event properties**

    * **Event code:** `INVD`
    * **Event name:** `Invalid Tracking Number`
    * **Event type:** `Tracking`
    * **Milestone:** `No`
    * **Stop the clock:** `Yes`
  </Card>
</Cards>

> 📘 _Note_
>
> _The webhook payload includes the mandatory fields shown in the [push payload example](https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample). Invalid tracking numbers are processed asynchronously so valid shipments continue tracking without interruption._

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
