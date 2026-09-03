---
title: Swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2026-06-23T09:01:53.979Z'
type: added
---
# EU customs changes

As part of the new EU customs regulations, the following fields have been added at the **Items** level of the **Create Shipment** endpoint for all carriers:

* **ManufactureProductId**: A unique identifier used to reference the shipped item and support carrier-specific requirements.
* **StandardiseProductId**: A globally recognised product identifier used for standardised item identification and to support carrier-specific requirements for customs and risk assessment.

> 📘 _Note_
>
> _If applicable, this information may be included in the carrier's pre-advice._
>
> _For more information, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/introduction">API References</Anchor> section._

# Royal Mail new optional field

A new optional field, **AdditionalHandlingFeesPaid**, has been added to the **CarrierSpecifics** object of the Royal Mail **Create Shipment** endpoint. This field indicates whether any extra handling charges have already been paid by the shipper, helping improve cost visibility and ensure accurate shipment processing.

> 📘 _Note_
>
> _If applicable, this information may be included in the carrier's pre-advice._
>
> _For more information, refer to the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) endpoint._