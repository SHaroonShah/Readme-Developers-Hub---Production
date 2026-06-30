---
title: EVRi
excerpt: >-
  _EVRi_ is a logistics and parcel delivery service provider that operates
  primarily in the UK. EVRi offers a wide range of delivery options, including
  standard, next-day, and scheduled deliveries, catering to both business and
  residential customers.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: shipping-account-setup-3
      title: Evri shipping account setup
---
<Image align="center" width="900px" src="https://files.readme.io/01dc0d3b7707e7095a26e08e874ca4fb1b7f2f82ba588e5d1c119b8f20e5e9c9-EVRi_white_banner.png" />

***

The EVRi integration into the SAPIENT platform enhances our shipping capabilities by enabling users to seamlessly manage their shipments through Evri's robust delivery network. Customers can now access Evri's comprehensive suite of services, including real-time tracking, flexible delivery options, and efficient returns management, all within the familiar SAPIENT interface. This enhancement aims to streamline the shipping process, improve operational efficiency, and provide a better overall experience for our users.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping and inbound shipping services.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration only supports <Glossary>DDU</Glossary>incoterm.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The intergration supports label in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.<br />
      </Card>
    </Cards>

    <br />

    > 📘 *Note*
    >
    > *QR code generation is supported for the returns shipments only.*
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
      <Card title="Single Package Shipments" icon="fa-solid fa-box">
        All services in this integration support only single-package services. Which means, only one package can be sent per request. Consignment services are not supported in the this integration.
      </Card>

      <Card title="Carrier-specific Fields " icon="fa-solid fa-truck">
        The **CarrierSpecifics** object in the Create Shipment request contains the following fields:

        * **SpecialInstruction1**: To provide special instructions or requests to the carrier for handling the shipment, such as handling procedures or delivery preferences.
        * **SpecialInstruction2**: To provide additional specific instructions concerning the shipment handling that Evri should be aware of.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Signed" icon="fa-solid fa-signature">
        Requires a signature upon delivery for verification of your shipment.
      </Card>

      <Card title="SMS" icon="fa-solid fa-message-sms">
        Requires a contact number to receive delivery updates via SMS.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-evri)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the Evri integration.

    | Service Name          | Description                                                                                                                                                                                   |
    | :-------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **International**     | This service provides international parcel delivery to over 200 countries and territories, offering global shipping with tracking and customs handling support.                               |
    | **Next Day Delivery** | This service provides next-working-day delivery across the UK, including tracking, delivery notifications, and weekend delivery options depending on location                                 |
    | **Returns**           | This service provides a convenient parcel returns solution, allowing customers to send items back to retailers via courier collection, ParcelShops, or lockers with full tracking visibility. |
    | **Sunday Service**    | This service provides parcel delivery on Sundays, offering extended weekend delivery coverage with tracking and flexible drop-off and collection options in supported areas.                  |
    | **Standard Delivery** | This service provides cost-effective parcel delivery within the UK, typically delivered within 2–4 working days with full tracking and flexible sending options.                              |

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For the most up-to-date carrier services, use the[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint.*
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect EVRi as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest shipment">
      Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for an EVRi shipment in the PDF or PNG format. This endpoint must be utilised when the label is not generated in the EVRi Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For EVRi shipments, the data files are sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={3}>
      <Card title="Add EVRi Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/v4.03/docs/shipping-account-setup-3">
        Set up your EVRi shipping account to start creating shipments.
      </Card>

      <Card title="Add EVRi Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/v4.03/docs/tracking-account-setup">
        Configure tracking for your EVRi shipments.
      </Card>

      <Card title="Add Child Client Department to Parent Shipping Account" icon="fa-solid fa-circle-user" href="https://docs.intersoftsapient.net/v4.03/docs/client-id-and-child-clinet-id-management-1">
        Create a parent shipping account and have multiple sub-accounts.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT EVRi API" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-evri">
        Explore the EVRi API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with EVRi and manage your shipping operations from a single platform.
  </Card>
</Cards>
