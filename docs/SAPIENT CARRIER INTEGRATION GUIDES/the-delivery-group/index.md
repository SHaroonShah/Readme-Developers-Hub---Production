---
title: The Delivery Group
excerpt: >-
  The Delivery Group integration supports outbound shipping from Great Britain
  to domestic, European, and Rest of the World destinations through SAPIENT.
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
<Image align="center" width="900px" src="https://files.readme.io/79449f551fdc59a798a190db96a351020b9c97a2f34998ca7b6f1d0acfbf4691-TDG_white_banner.png" />

The Delivery Group integration supports outbound shipping from Great Britain to domestic, European, and Rest of the World destinations through SAPIENT.

***

The Delivery Group (TDG) hands shipments over to other carriers for final-mile delivery. Services for this integration include carriers such as Evri and Yodel. SAPIENT creates the shipment with The Delivery Group using the requested service, and The Delivery Group manages sending the data and transferring the shipment to the final-mile carrier.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
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

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={2}>
      <Card title="Single Piece shipments" icon="fa-solid fa-box">
        The Delivery Group supports single-package shipments only. Consignment services are not supported.
      </Card>

      <Card title="Package Dimensions" icon="fa-solid fa-ruler-combined">
        Package dimensions are mandatory for The Delivery Group shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    * **Signed**: Requires a signature upon delivery of the shipment.
    * **Delivery Instructions**: Provides special instructions related to the delivery of the shipment. This may involve guidance on how the package should be handled or specific requests regarding the delivery location, such as leaving the shipment at the back door or delivering it to a neighbour to sign.

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-tdg) section.*
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      Pre-advises The Delivery Group of shipments. SAPIENT requests The Delivery Group to send the label in the **SubmitItemAdvice** response, which returns the shipment tracking number and label. There is no need to call the **GetLabel** API to retrieve the label.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Tracking" icon="print">
      The Delivery Group tracking API uses the username and password set on the shipping account linked to the tracking account to authorise requests to the Tracking API.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add The Delivery Group Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/the-delivery-group-account-set-up#/">
        Set up your The Delivery Group shipping account to start creating shipments.
      </Card>

      <Card title="Add The Delivery Group Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/the-delivery-group-tracking-account-set-up#/">
        Configure tracking for your The Delivery Group shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT The Delivery Group API" icon="fa-solid fa-code" href="">
        Explore The Delivery Group API endpoints for shipping and tracking.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with The Delivery Group and manage your shipping operations from a single platform.
  </Card>
</Cards>
