---
title: Amazon
excerpt: >-
  Amazon Shipping is a parcel delivery service offered by Amazon for businesses,
  including those selling on Amazon and other platforms. It provides fast,
  reliable, and cost-effective shipping solutions with features like next-day
  and two-day delivery, real-time tracking, photo-on-delivery, and customer
  notifications.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" border={false} width="900px" src="https://files.readme.io/79cb618e1191e3516e756266138d9bec63db210f2763f8d1ce8f27804893dfea-Amazon_white_banner.png" />

***

In the UK, Amazon Shipping covers England, Scotland, and Wales, offering seven-day pickup and delivery, including weekends at no extra cost. Customers benefit from various delivery options, such as Standard (3–5 days), One-Day, and Same-Day for Prime members.
<Tabs>
<Tab title="Key Features">
<Cards columns={2}>
  <Card title="Ship from Destinations" icon="fa-solid fa-truck">
    The integration supports shipping from locations in Great Britain (GB) only.
  </Card>
  <Card title="Ship to Destinations" icon="fa-solid fa-location-dot">
    Users can send shipments to Great Britain (GB) only, including Northern Ireland (NI).
  </Card>
  <Card title="Service Type" icon="fa-solid fa-box">

    The integration is focused on outbound shipping on both, Amazon-owned marketplaces (referred to as <Glossary>On-Amazon</Glossary> shipments) and orders originating from non-Amazon owned channels (referred to as <Glossary>Off-Amazon</Glossary>).
  </Card>
  <Card title="Incoterms" icon="fa-solid fa-globe">
    The integration supports shipping domestically within the shipper country only. Therefore, incoterms are not applicable.
  </Card>
  <Card title="Label Formats" icon="fa-solid fa-file">
    <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.
  </Card>
</Cards>
</Tab>
<Tab title="Additional Features">

* **Single package services**: Amazon only supports single package services.
* **Carrier specific fields**: The **CarrierSpecifics** object in the **Create Shipment** request contains the following fields:
  * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment.
  * **AmazonOrderID**: The unique Amazon ID for each order, which is only mandatory for On Amazon shipments.
  * **AmazonOrderItemId**: The unique Amazon ID for each item in the order, which is only mandatory for On Amazon shipments and is available at the item-level of the **Create Shipment** request. Additionally, the **SkuCode** field is included to link the **AmazonOrderItemId** to the corresponding item in the shipment.

</Tab>
</Tabs>

> 📘 _Note_
>
> _The label formats are supported for both On Amazon and Off Amazon shipments. However, the available label formats depends on the service used._

## Service enhancements

The following key services are provided by the Amazon integration:
<Columns layout="auto">
  <Column>
    **Signature on Delivery (SOD)**

    A signature is required upon delivery for verification of your shipment.
  </Column>
  <Column>
    **One Time Password (OTP)**

    Amazon sends the receiver a one-time password to be used upon delivery.
  </Column>
</Columns>

***
In this section, learn how to:

<Cards columns={2}>
  <Card title="Add an Amazon shipping account" icon="fa-solid fa-plus" href="https://docs.intersoftsapient.net/docs/add-amazon-shipping-account">
    Set up your Amazon shipping account to start creating shipments.
  </Card>
  <Card title="Add an Amazon tracking account" icon="fa-solid fa-satellite-dish" href="https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/">
    Configure tracking for your Amazon shipments.
  </Card>
</Cards>

> 📘 _Note_
>
> _For more information on how to activate the Amazon integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._

<br />