---
title: The Delivery Group
excerpt: >-
  The Delivery Group (TDG) is a prominent carrier specializing in mail
  distribution services to enhance the efficiency of shipping and delivery
  processes.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---

<Image src="https://files.readme.io/79449f551fdc59a798a190db96a351020b9c97a2f34998ca7b6f1d0acfbf4691-TDG_white_banner.png" align="center" width="900px" />


The Delivery Group integration supports outbound shipping from Great Britain to domestic, European, and Rest of the World destinations through SAPIENT.

***

The Delivery Group (TDG) hands shipments over to other carriers for <Glossary>final mile delivery</Glossary>. Services for this integration include carriers such as Evri and Yodel. SAPIENT creates the shipment with The Delivery Group using the requested service, and The Delivery Group manages sending the data and transferring the shipment to the final-mile carrier.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and the <Glossary>ROW</Glossary> (Rest of the World).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration supports outbound shipping only.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary>.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single Piece shipments" icon="fa-solid fa-box">
        The Delivery Group supports single-package shipments only. Consignment services are not supported.
      </Card>

      <Card title="Package Dimensions" icon="fa-solid fa-ruler-combined">
        Package dimensions are mandatory for The Delivery Group shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards>
      <Card title="Signed" icon="fa-solid fa-signature">
        Requires a signature upon delivery of the shipment.
      </Card>
    </Cards>

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements and carrier services, refer to the[API References](https://docs.intersoftsapient.net/reference/post_v4-shipments-tdg) section._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by The Delivery Group integration.

    | Service Name     | Description                                                                                                                                                                                           |
    | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **UTrak**        | This service provides tracked UK delivery for e-commerce parcels, typically delivered within 2–3 working days, offering door-to-door tracking, flexible collections, and proof of delivery.           |
    | **ETrak**        | This service provides international tracked parcel delivery, enabling cross-border shipping with consolidated tracking, final-mile carrier integration, and delivery to over 220 global destinations. |
    | **UK 24 Parcel** | This service provides next-working-day delivery within the UK, offering full tracking, proof of delivery, and reliable transit for parcels up to standard weight limits.                              |
    | **UK 48 Parcel** | This service provides cost-effective UK delivery within two working days, including tracking and proof of delivery for less time-sensitive shipments.                                                 |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect The Delivery Group as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for The Delivery Group shipment in the PDF or PNG format. This endpoint must be utilised when the label is not generated in The Delivery Group Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      The Delivery Group’s tracking API uses the username and password set on the shipping account linked to the tracking account, which is used to authorise requests to the Tracking API. This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add The Delivery Group Shipping Account" href="https://docs.intersoftsapient.net/docs/the-delivery-group-account-set-up#/" icon="fa-solid fa-truck" target="_blank">
        Set up your The Delivery Group shipping account to start creating shipments.
      </Card>

      <Card title="Add The Delivery Group Tracking Account" href="https://docs.intersoftsapient.net/docs/the-delivery-group-tracking-account-set-up#/" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your The Delivery Group shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT The Delivery Group API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-tdg" icon="fa-solid fa-code" target="_blank">
        Explore The Delivery Group API endpoints for shipping and tracking.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Sign-Off">
    <Cards columns="2">
      <Card title="TDG Sign-off Process" href="https://docs.intersoftsapient.net/docs/the-delivery-group-sign-off" icon="fa-solid fa-file-signature" target="_blank">
        Complete all the necessary steps before using The Delivery Group for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with The Delivery Group and manage your shipping operations from a single platform.
  </Card>
</Cards>
