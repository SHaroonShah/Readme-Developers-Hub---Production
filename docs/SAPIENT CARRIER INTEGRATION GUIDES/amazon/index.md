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
<Image align="center" width="900px" src="https://files.readme.io/79cb618e1191e3516e756266138d9bec63db210f2763f8d1ce8f27804893dfea-Amazon_white_banner.png" />

***

In the UK, Amazon Shipping covers England, Scotland, and Wales, offering seven-day pickup and delivery, including weekends at no extra cost. Customers benefit from various delivery options, such as Standard (3–5 days), One-Day, and Same-Day for Prime members.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB) only, including Northern Ireland (NI).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping on both, Amazon-owned marketplaces (referred to as <Glossary>On-Amazon</Glossary> shipments) and orders originating from non-Amazon owned channels (referred to as <Glossary>Off-Amazon</Glossary>).
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports shipping domestically within the shipper country only. Therefore, incoterms are not applicable.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.<br />
        The label formats are supported for both On Amazon and Off Amazon shipments. However, the available label formats depends on the service used.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    * **Single package shipments**: Amazon only supports single package services. Consignment services are not supported in the this integration.

    * **Carrier-Specific Fields**: The **CarrierSpecifics** object in the **Create Shipment** request contains the following fields:

      * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment.
      * **AmazonOrderID**: The unique Amazon ID for each order, which is only mandatory for On Amazon shipments.
      * **AmazonOrderItemId**: The unique Amazon ID for each item in the order, which is only mandatory for On Amazon shipments and is available at the item-level of the **Create Shipment** request. Additionally, the **SkuCode** field is included to link the **AmazonOrderItemId** to the corresponding item in the shipment.
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Signature on Delivery (SOD)" icon="fa-solid fa-signature">
        A signature is required upon delivery for verification of your shipment.
      </Card>

      <Card title="One Time Password (OTP)" icon="fa-solid fa-location-pin-lock">
        Amazon sends the receiver a one-time password to be used upon delivery.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/v4.03/reference/post_v4-shipments-amazon)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>
</Tabs>

***

## Getting Started

<Cards columns={3}>
  <Card title="Add Amazon shipping account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-amazon-shipping-account">
    Set up your Amazon shipping account to start creating shipments.
  </Card>

  <Card title="Add Amazon tracking account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/">
    Configure tracking for your Amazon shipments.
  </Card>

  <Card title="API References" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-amazon">
    Explore the Amazon API endpoints for a seamless shipping experience.
  </Card>
</Cards>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Amazon and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
