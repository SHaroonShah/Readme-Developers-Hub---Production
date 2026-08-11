---
title: DX Express
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

<Image src="https://files.readme.io/18184b139f3c15f60566ae06ce4aacb8b6f3255b216fe298f6f8c971a8337e73-DX_Express_white_banner.png" align="center" width="900px" />


***

Express is one of DX's core solutions that provides a fast and secure next-day delivery service to businesses and home addresses for single and multiple items under 25 kg in weight and 2 metres in dimension.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Northern Ireland (NI)—shipments to GB country code with a postcode beginning with BT).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration support labels in <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>
    </Cards>


  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single Piece Shipments" icon="fa-solid fa-box">
        DX Express supports only single-piece shipments. The integration does not support consignment or multipiece shipments.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-box-circle-check">
        DX support their own <Glossary>package type</Glossary>s. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the DX Express integration.

    | Service Name        | Description                                                                                                                                                                       |
    | :------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Secure Flex**     | This service provides next-day delivery of parcels and packets, primarily to residential addresses across the UK, with secure handling, tracking, and flexible delivery options.  |
    | **Secure Business** | This service provides next-day delivery of parcels and packets to business addresses across the UK and Ireland, with secure handling and delivery during standard business hours. |



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
      The integration for creating shipments to reflect DX as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>



    <Accordion title="Cancel Shipment">
      The integration for directly calling the DX’s API to cancel shipments within DX’s system, to ensures that cancellations are fully registered with DX, helping prevent customers from being mistakenly charged for cancelled shipments. <br />

      <Callout icon="🚧" theme="warn">
        ### _Important_

        _If you attempt to release a held shipment to a later date, please be aware that the shipment will no longer be eligible for cancellation. Shipments can only be cancelled if they have not been manifested._
      </Callout>


    </Accordion>



    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for DX shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DX Create Shipment request.

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
      <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/shipping-accounts-5" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up a DX Express shipping account on SAPIENT.
      </Card>

      <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/tracking-1" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up a DX Express tracking account on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT DX Express API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dxf" icon="fa-solid fa-code">
        Explore the DX Express API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Sign-Off">
    <Cards>
      <Card title="DXF Sign-off Process" href="https://docs.intersoftsapient.net/docs/dx-freight-sign-off-copy" icon="fa-solid fa-file-signature">
        Complete all the necessary steps before using DX Express for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="DX Rate Limit">
    <Cards>
      <Card title="DX Rate Limiting" href="https://docs.intersoftsapient.net/docs/dx-rate-limit" icon="fa-solid fa-gauge-max">
        Learn more on how to restrict your API calls over a specified time frame.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DX Express and manage your shipping operations from a single platform.
  </Card>
</Cards>