---
title: InPost
excerpt: >-
  InPost is a Polish public logistics limited company with courier, package
  delivery and express mail service. The company specialises in parcel locker
  service operated in Poland, Italy, United Kingdom, France, Benelux, Spain, and
  Portugal.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/75762ee66dc10880c8cfd75e2d683174396ef3ed0fd727fd959f2eb44e013de6-InPost_white_banner.png" />

***

InPost provides a convenient, eco-friendly parcel delivery service through a network of 24/7 automated lockers and partnered shops in the UK. You can drop off or pick up parcels at these locations anytime, offering flexibility and ease for both senders and recipients.

This integration offers several key features that streamline the shipping process. This article summarises the in-scope features of the integration and provides detailed explanations of the associated process flows.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotlabd).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB) mainland only.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound and inbound shipping.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards column={1}>
      <Card title="Labelled B2C" icon="fa-solid fa-id-card">
        Generates and returns a label to be attached to the parcel for a B2C business transaction type deliveries.
      </Card>
<Card title="Labelless Returns Using QR Codes" icon="fa-solid fa-id-card">
  Generates a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.
      </Card>
</Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Proof of Identity" icon="fa-solid fa-id-card">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fa-solid fa-calendar-circle-user">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fa-solid fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fa-solid fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>
</Tabs>

<br />

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotland).
* **Ship to Destinations**: Users can send <Glossary>shipments</Glossary> to the Great Britain (GB) mainland only.
* **Service Type**: The integration is focused on outbound and return shipping.

## Additional features

These services include the following:

* **Labelled B2C**: to generate and return a <Glossary>label</Glossary> to be attached to the parcel for a B2C <Glossary>business transaction type</Glossary> deliveries.
* **Labelless returns using QR codes**: to generate a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.

## Carrier API services

* **API endpoints for shipment creation and QR code retrieval**: The integration includes specific API endpoints that developers can use to create shipments, get PUDO locations, and retrieve labels or QR codes. This enables seamless interaction between the InPost service and SAPIENT system, ensuring efficient data flow and functionality.
  * Create shipment for B2C and returns services
  * Get PUDO Locations

In this section, learn how to:

* <Anchor label="Add an InPost shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-inpost-shipping-account#/">Add an InPost shipping account</Anchor>
* [Use InPost PUDO service](https://docs.intersoftsapient.net/docs/pudo-integration#/)
