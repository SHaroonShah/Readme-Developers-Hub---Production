---
title: YODEL
excerpt: >-
  _YODEL_ is a prominent logistics and parcel delivery service provider based in
  the UK., specialising in delivery parcels for ecommerce businesses and
  individual customers. YODEL offers a broad range of delivery options,
  including next-day delivery, standard service, and same-day delivery for
  certain locations.
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
      slug: shipping-account-setup-1
      title: Yodel shipping account setup
---

<Image src="https://files.readme.io/3d6b9cd3a2a729d7bb30ada0f5836b3330a213d5425aa775cd814a13b958e44d-YODEL_white_banner.png" align="center" width="900px" />


***

YODEL is fully integrated into the Intersoft SAPIENT platform, allowing businesses to access YODEL’s delivery network through SAPIENT’s unified API.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).

        > _Shipments to Northern Ireland (NI) and the Channel Islands are treated as international._
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid) incoterm only.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
      </Card>
    </Cards>


  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Consignment Services" icon="fa-solid fa-boxes-stacked">
        The integration supports consignment services. The maximum number of packages depends on the service. Some services allow multiple packages, and some do not; the maximum number of packages is stored against the service.

        > _Multi-package requests are not supported for single-package services._
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements documented for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the Yodel integration.

    | Service Name     | Description                                                                                                                                                                                                         |
    | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | **Yodel Xpect**  | This service provides fully tracked parcel delivery with next-day or two-day options, including a two-hour delivery window and in-flight notifications to give recipients greater control over delivery.            |
    | **Yodel Xpress** | This service provides fast, fully tracked delivery for small to medium parcels, offering next-day or two-day delivery with flexible delivery options and in-flight updates.                                         |
    | **Yodel Xpert**  | This service provides specialist delivery for high-value or sensitive items, offering enhanced tracking, address-only delivery options, and additional secure handling features for specific delivery requirements. |



    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect Yodel as a primary carrier and allowing users to create shipments using the Create Shipment API endpoint that returns the label in base64 encoded format.
    </Accordion>



    <Accordion title="Manifest shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.

      <Callout icon="📘" theme="info">
        ### _Note_

        _If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels._
      </Callout>
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a FedEx International Connect shipment in the PDF format. This endpoint must be utilised when the label is not generated in the FedEx International Connect Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>



    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.The YODEL tracking integration enables data files to be sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add YODEL Shipping Account" href="https://docs.intersoftsapient.net/docs/shipping-account-setup-1" icon="fa-solid fa-truck">
        Set up your YODEL shipping account to start creating shipments.
      </Card>

      <Card title="Add YODEL Tracking Account" href="https://docs.intersoftsapient.net/docs/tracking" icon="fa-solid fa-search-location">
        Configure tracking for your YODEL shipments.
      </Card>

      <Card title="Add a Tracking Barcode Range" href="https://docs.intersoftsapient.net/docs/barcode-range-setup-1#/" icon="fa-solid fa-barcode">
        Add a tracking barcode range to your YODEL shipping account.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT YODEL API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-yodel" icon="fa-solid fa-code">
        Explore the YODEL API endpoints for shipping account and shipment workflows.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with YODEL and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />

<br />