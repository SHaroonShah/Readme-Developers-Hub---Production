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

<Image src="https://files.readme.io/79cb618e1191e3516e756266138d9bec63db210f2763f8d1ce8f27804893dfea-Amazon_white_banner.png" align="center" width="900px" />


***

In the UK, Amazon Shipping covers England, Scotland, and Wales, offering seven-day pickup and delivery, including weekends at no extra cost. Customers benefit from various delivery options, such as Standard (3–5 days), One-Day, and Same-Day for Prime members.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns="3">
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
  </Tab>

  <Tab title="Additional Features">
    <Cards columns="1">
      <Card title="Single Package Shipments" icon="fa-solid fa-box">
        Amazon only supports single package services. Consignment services are not supported in the this integration.
      </Card>

      <Card title="Carrier-specific Fields " icon="fa-solid fa-truck">
        The **CarrierSpecifics** object in the Create Shipment request contains the following fields:

        - **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment.
        - **AmazonOrderID**: The unique Amazon ID for each order, which is only mandatory for On Amazon shipments.
        - **AmazonOrderItemId**: The unique Amazon ID for each item in the order, which is only mandatory for On Amazon shipments and is available at the item-level of the **Create Shipment** request. Additionally, the **SkuCode** field is included to link the **AmazonOrderItemId** to the corresponding item in the shipment.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards>
      <Card title="Signature on Delivery (SOD)" icon="fa-solid fa-signature">
        A signature is required upon delivery for verification of your shipment.
      </Card>

      <Card title="One Time Password (OTP)" icon="fa-solid fa-location-pin-lock">
        Amazon sends the receiver a one-time password to be used upon delivery.
      </Card>
    </Cards>

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements, refer to the [Create Shipment](https://docs.intersoftsapient.net/v4.04/reference/post_v4-shipments-amazon) endpoint._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by teh Amazon integration.

    | Service  Name | Description                                                                                                                               |
    | :------------ | :---------------------------------------------------------------------------------------------------------------------------------------- |
    | **Prime**     | This service provides next-day delivery service with full tracking for Amazon marketplace orders.                                         |
    | **Standard**  | This service provides two-day delivery service with tracking for Amazon marketplace orders.                                               |
    | **Economy**   | This service provides cost-effective tracked delivery service with a longer transit time for Amazon marketplace orders.                   |
    | **1Day**      | This service provides next-day delivery service for non-Amazon orders; may include limited or no tracking compared to On-Amazon services. |
    | **2Day**      | This service provides two-day delivery service for non-Amazon orders; may include limited or no tracking compared to On-Amazon services.  |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect Amazon as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for an Amazon shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add Amazon Shipping Account" href="https://docs.intersoftsapient.net/docs/add-amazon-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your Amazon shipping account to start creating shipments.
      </Card>

      <Card title="Add Amazon Tracking Account" href="https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your Amazon shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT Amazon API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-amazon" icon="fa-solid fa-code" target="_blank">
        Explore the Amazon API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Amazon and manage your shipping operations from a single platform.
  </Card>
</Cards>
