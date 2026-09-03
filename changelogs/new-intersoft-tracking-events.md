---
title: New INTERSOFT tracking events
author: Syed Haroon Shah
hidden: true
published_at: '2026-06-23T08:44:49.899Z'
type: added
---
The SAPIENT's Tracking Webhook has been updated improve collection outcomes by introducing the new following new INTERSOFT tracking event codes.

| Tracking Event Code | Tracking Event Name                                                       |
| :------------------ | :------------------------------------------------------------------------ |
| CAMD                | Collection booking was updated or amended after initial scheduling.       |
| CSBK                | Collection has been successfully booked and confirmed.                    |
| PSCS                | Shipment has been collected and left in a designated safe place.          |
| CAAT                | Collection was attempted but not completed.                               |
| CAFI                | Collection attempt failed because the location was inaccessible.          |
| CAFP                | Collection attempt failed due to a packaging issue.                       |
| CAFN                | Collection attempt failed because the shipment was not available.         |
| CAFA                | Collection attempt failed as there was no response at the location.       |
| CAFO                | Collection attempt failed due to oversize or overweight shipment.         |
| CSPP                | Collection from safe place failed due to a packaging issue.               |
| CSPI                | Collection from safe place failed because access was not possible.        |
| CSPN                | Collection from safe place failed as the shipment was not available.      |
| CSPO                | Collection from safe place failed due to oversize or overweight shipment. |
| CCAN                | Collection request has been cancelled.                                    |
| CNAT                | Collection was not attempted.                                             |

These new tracking event codes provides customers with clear, actionable tracking updates for failed collections, enabling faster issue resolution and improved operational decision-making.

> 📘 _Note_
>
> _For detailed information on all tracking events and milestones, refer to the following sections:_
>
> * _[Track events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones)_
> * [_Tracking Webhook Push Payload Example_](https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample)