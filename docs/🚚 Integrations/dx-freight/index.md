---
title: DX Freight
excerpt: >-
  _DX_ is a UK-based logistics and parcel delivery company that specialises in
  providing tailored delivery solutions for businesses and individuals. DX
  offers a wide range of delivery options, including time-sensitive and next-day
  services, focusing on delivering parcels, documents, and heavy items.
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

<Image src="https://files.readme.io/ed4b0e49c08719ebbc9ac569d952798457c6cf7205c33335f35fa9bc462e65e3-DX_Freight_white_banner.png" align="center" width="900px" />


***

Freight is one of DX's core solutions, also referred to as _IDW_ (Irregular Dimensions and Weight), that provides delivery services to businesses and home addresses for multi-item <Glossary>consignment</Glossary>s, pallets up to 6 metres in length, and individual <Glossary>items</Glossary> in excess of 25 kg in weight.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Channel Islands (CI).

        > _Shipments to Channel Islands are treated as domestic destination for freight shipments._
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration does not support any incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration support labels in <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Accordion title="Single piece shipments">
      DX Freight supports a maximum of 999 packages in a shipment, but the SAPIENT maximum—99 is used instead.
    </Accordion>

    <Accordion title="DX-1 service">
      A 1-man service type that is typically deigned for door to door standard next-day delivery of parcels weighing up to a specific limit (50 kg) to the capability of effectively handling pallets. This service is usually best for smaller and lighter <Glossary>package</Glossary>s. 1Man service type includes the following services:

      - **ON**: Overnight
      - **3D**: 3Day
      - 930: Overnight 9:30
      - AM: Overnight pre noon
      - SAT: Saturday
      - S93: Saturday 9:30
    </Accordion>

    <Accordion title="DX-2 service">
      A 2-man service type that caters to larger and heavier <Glossary>shipments</Glossary>, typically allowing for items that require 2-person handling due to their size or weight. This service is useful particularly for businesses that deal with bulky items or items that cannot be managed by one person. 2Man service type includes the following services:

      - **H1**: 2Man Overnight
      - **H2**: 2Man Standard
      - **HS**: 2Man Saturday
      - **C1**: 2Man Collection Overnight
      - **C2**: 2Man Collection Standard
      - **CS**: 2Man Saturday Only
    </Accordion>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the DX Freight integration.

    | Service Name           | Description                                                                                                                                                                          |
    | :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **3Day**               | This service provides reliable delivery of freight within three working days, suitable for non-urgent shipments of heavy or irregular items with full tracking visibility.           |
    | **Overnight 9:30**     | This service provides next-working-day delivery of freight by 9:30 AM, ensuring early arrival for time-critical shipments with full tracking and confirmation.                       |
    | **Overnight pre noon** | This service provides next-working-day delivery of freight before 12:00 PM, offering a timed delivery option for urgent consignments requiring arrival before midday.                |
    | **2Man Overnight**     | This service provides next-working-day delivery of large or heavy items requiring two-person handling, ensuring safe transport and placement for oversized consignments              |
    | **2Man Standard**      | This service provides scheduled delivery of large or heavy items using a two-person crew, offering a cost-effective solution for non-urgent shipments requiring specialist handling. |
    | **2Man Saturday**      | This service provides Saturday delivery of large or heavy items using a two-person crew, enabling convenient weekend delivery with specialist handling for oversized goods.          |
    | **Overnight**          | This service provides next-working-day delivery of freight, offering fast and reliable transport for heavy, bulky, or irregular shipments with full tracking.                        |
    | **Saturday 9:30**      | This service provides Saturday delivery of freight by 9:30 AM, ensuring early weekend delivery for time-sensitive consignments.                                                      |
    | **Saturday**           | This service provides standard Saturday delivery of freight, enabling weekend delivery of heavy or bulky items with full tracking and reliable handling.                             |

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
      The integration for creating shipments to reflect DX Freight as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Delete Shipment">
      The integration to delete an existing shipment cancelled in SAPIENT.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a DX Freight shipment in the PDF or ZPL format. This endpoint must be utilised when the label is not generated in the DXF Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For DXF shipments, the data files are sent via SFTP for both—1Man and 2Man services.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-shipping-account" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up a DX Freight shipping account on SAPIENT.
      </Card>

      <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-tracking-account#/" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up a DX Freight tracking account on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT DXF API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dxf" icon="fa-solid fa-code">
        Explore the DX Freight API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Sign-Off">
    <Cards>
      <Card title="DXF Sign-off Process" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off" icon="fa-solid fa-file-signature">
        Complete all the necessary steps before using DXF for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DX Freight and manage your shipping operations from a single platform.
  </Card>
</Cards>