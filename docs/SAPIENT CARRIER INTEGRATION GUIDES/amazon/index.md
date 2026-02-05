---
title: Amazon
excerpt: >-
  Amazon Shipping is a parcel delivery service offered by Amazon for businesses,
  including those selling on Amazon and other platforms. It provides fast,
  reliable, and cost-effective shipping solutions with features like next-day
  and two-day delivery, real-time tracking, photo-on-delivery, and customer
  notifications.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" border={false} width="900px" src="https://files.readme.io/79cb618e1191e3516e756266138d9bec63db210f2763f8d1ce8f27804893dfea-Amazon_white_banner.png" />

***

In the UK, Amazon Shipping covers England, Scotland, and Wales, offering seven-day pickup and delivery, including weekends at no extra cost. Customers benefit from various delivery options, such as Standard (3–5 days), One-Day, and Same-Day for Prime members.

## Key features

This integration provides the following key features:

* **Ship from Destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship to Destinations**: Users can send shipments to Great Britain (GB) only, including Northern Ireland (NI).
* **Service Type**: The integration is focused on outbound shipping on both, Amazon-owned marketplaces (referred to as <Glossary>On-Amazon</Glossary> shipments) and orders originating from non-Amazon owned channels (referred to as <Glossary>Off-Amazon</Glossary>).
* **Incoterms**: The integration supports shipping domestically within the shipper country only. Therefore, incoterms are not applicable.
* **Label Formats**: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.

> 📘 _Note_
>
> _The label formats are supported for both On Amazon and Off Amazon shipments. However, the available label formats depends on the service used._

## Service enhancements

The following are the key services are provided by the Amazon integration:

* **Signature on Delivery** (SOD): A signature is required upon delivery for verification of your shipment.
* **One time password** (OTP): Amazon sends the receiver a onetime password to be used upon delivery.

## Additional features

The Amazon integration provides the following additional features:

* **Single package services**:  Amazon only supports single package services.
* **Carrier specific fields**: The **CarrierSpecifics** object in the **Create Shipment** request contains the following fields:
  * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment.
  * **AmazonOrderID**: The unique Amazon ID for each order, which is only mandatory for On Amazon shipments.
  * **AmazonOrderItemId**: The unique Amazon ID for each item in the order, which is only mandatory for for On Amazon shipments and is available at the item-level of the **Create Shipment** request. Additionally, the **SkuCode** field is included to link the **AmazonOrderItemId** to the corresponding item in the shipment.

<br />

***

this section, learn how to:

* [Add an Amazon shipping account](https://docs.intersoftsapient.net/docs/add-an-post-shipping-account#/)
* [Add an An Amazon tracking account](https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/)

> 📘 _Note_
>
> _For more information on how to activate the Amazon integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._
