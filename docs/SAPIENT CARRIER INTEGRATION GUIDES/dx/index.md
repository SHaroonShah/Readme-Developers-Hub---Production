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
<Image align="center" width="900px" src="https://files.readme.io/18184b139f3c15f60566ae06ce4aacb8b6f3255b216fe298f6f8c971a8337e73-DX_Express_white_banner.png" />

***

Express is one of DX's core solutions that provides a fast and secure next-day delivery service to businesses and home addresses for single and multiple items under 25 kg in weight and 2 metres in dimension.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={3}>
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

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
      <Card title="Single Piece Shipments" icon="fa-solid fa-box">
        DX Express supports only single-piece shipments. The integration does not support consignment or multipiece shipments.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-box-circle-check">
        DX support their own <Glossary>package type</Glossary>s. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 *Note*
    >
    > *There are no service enhancements for this integration.*
  </Tab>
</Tabs>

***

## API Services

<br />

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
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

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DX Express and manage your shipping operations from a single platform.
  </Card>
</Cards>
