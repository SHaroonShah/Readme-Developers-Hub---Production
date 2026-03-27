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
<Image align="center" width="900px" src="https://files.readme.io/ed4b0e49c08719ebbc9ac569d952798457c6cf7205c33335f35fa9bc462e65e3-DX_Freight_white_banner.png" />

***

Freight is one of DX's core solutions, also referred to as _IDW_ (Irregular Dimensions and Weight), that provides delivery services to businesses and home addresses for multi-item <Glossary>consignment</Glossary>s, pallets up to 6 metres in length, and individual <Glossary>items</Glossary> in excess of 25 kg in weight.

## Overview

<br />

<Tabs>
  <Tab title="Key Features">
    <Cards columns={3}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Channel Islands.
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
    </Cards> <br />

    > 📘 *Note*
    >
    > *Bear in mind that shipments to Channel Islands are treated as domestic destination for freight shipments.*

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Accordion title="Single piece shipments" icon="">
      DX Freight supports a maximum of 999 packages in a shipment, but the SAPIENT maximum—99 is used instead.
    </Accordion>

    <br />

    <Accordion title="DX-1" icon="">
      A 1-man service type that is typically deigned for door to door standard next-day delivery of parcels weighing up to a specific limit (50 kg) to the capability of effectively handling pallets. This service is usually best for smaller and lighter <Glossary>package</Glossary>s. 1Man service type includes the following services:

      * **ON**: Overnight
      * **3D**: 3Day
      * 930: Overnight 9:30
      * AM: Overnight pre noon
      * SAT: Saturday
      * S93: Saturday 9:30
    </Accordion>

    <br />

    <Accordion title="DX-2" icon="">
      A 2-man service type that caters to larger and heavier <Glossary>shipments</Glossary>, typically allowing for items that require 2-person handling due to their size or weight. This service is useful particularly for businesses that deal with bulky items or items that cannot be managed by one person. 2Man service type includes the following services:

      * **H1**: 2Man Overnight
      * **H2**: 2Man Standard
      * **HS**: 2Man Saturday
      * **C1**: 2Man Collection Overnight
      * **C2**: 2Man Collection Standard
      * **CS**: 2Man Saturday Only
    </Accordion>
  </Tab>
</Tabs>

***

## API Services

<br />

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect DXF as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Delete Shipment" icon="plus-circle">
      The integration to delete an existing shipment cancelled in SAPIENT.

      <br />
    </Accordion>
  </Tab>

  <Tab title="Advanced Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for a DXF shipment in the PDF or ZPL format. This endpoint must be utilised when the label is not generated in the DXF Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking" icon="print">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For DXF shipments, the data files to be sent via SFTP for both—1Man and 2Man services.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-shipping-account" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up An Post shipping account on SAPIENT.
      </Card>

      <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-tracking-account#/" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up An Post tracking account on SAPIENT.
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

  <Tab title="Related Topics">
    <Cards>
      <Card title="DXF Sign-off Process" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off" icon="fa-solid fa-file-signature">
        Complete all the necessary steps before using DXF for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Royal Mail and manage your shipping operations from a single platform.
  </Card>
</Cards>

In this section, learn how to:

* [Add a DX Freight shipping account](https://docs.intersoftsapient.net/docs/add-dx-freight-shipping-account)
* [Add a DX Freight tracking account](https://docs.intersoftsapient.net/docs/add-dx-freight-tracking-account#/)

> 📘 _Note_
>
> _For more information on how to activate the DX Freight integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._

<br />
