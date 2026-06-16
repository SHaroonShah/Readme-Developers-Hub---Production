---
title: FedEx
excerpt: >-
  FedEx is a global leader in logistics and delivery services, renowned for its
  reliable express shipping and comprehensive transportation solutions. It
  offers a range of shipping options tailored for various international markets,
  making it an essential partner for businesses seeking to optimise their
  shipping operations.
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
The FedEx integration supports outbound shipping from Great Britain and Europe to domestic, European, and Rest of the World destinations through SAPIENT.

***

FedEx is a global leader in logistics and delivery services, providing reliable express shipping and transportation solutions for international markets.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) and Europe.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping only.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={2}>
      <Card title="Multipiece Shipments" icon="fa-solid fa-boxes-stacked">
        Support for multipiece shipments is included in the integration.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-box">
        FedEx offers its own distinct <Glossary>package type</Glossary>s. You can look up package types by calling the <Anchor label="Get Carrier Service Package Types" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/">Get Carrier Service Package Types</Anchor> endpoint.
      </Card>

      <Card title="Electronic Trade Document (ETD)" icon="fa-solid fa-file-invoice">
        Supports electronic trade documents, such as <Glossary>commercial invoice</Glossary>, <Glossary>proforma invoice</Glossary>, and in some cases, other specific documents, while configuring the FedEx <Glossary>shipping account</Glossary>. This solution allows you to create and send your trade documents electronically when shipping internationally.
      </Card>
    </Cards>

    <br />

    <Callout icon="📘" theme="default">
      ### *Note*

      *For more information on Electronic Trade Document configuration, refer to the<Anchor label="Add FedEx shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-shipping-account">Add FedEx shipping account</Anchor> section.*
    </Callout>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key service enhancements provided by the FedEx integration:

    * **Saturday Delivery**: Enables package delivery on Saturdays for added convenience.
    * **Declared Values**: Applies a surcharge if the requested declared value of the shipment exceeds the liability stated in FedEx's terms and conditions for the selected service. The *declared value* of a package represents the maximum liability in connection with the shipment of the package, including, but not limited to, any loss, damage, delay, or missed delivery relating to that shipment. As the shipper, it’s your responsibility to prove any actual damages. Exposure to and risk of any loss in excess of your declared value is assumed by you.
    * **Adult Signature**: Obtains a signature from any person of legal age at the delivery address, subject to the provision of a valid ID. If no one qualified to sign is available, an attempt will be made to redeliver the package on another date. Legal age varies depending on the destination country/territory and is governed by local legal age of an adult, not the legal age to purchase specific products.
    * **Direct Signature**: Obtains a signature from someone at the delivery address only. If no one is available to sign, a redelivery attempt of the package will be made on another date.
    * **Indirect Signature**: Obtains a signature from someone at the delivery address, from a neighbour, or from a building manager. If no one is available to sign, the package will be delivered on another date.
    * **No Signature Required**: Allows delivery without obtaining a signature if no one is available to sign. The package will be kept in a safe place.
    * **Email Notifications**: Sends notifications on delivery, estimated delivery, exceptions, shipment status, and tender.

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the API References section.*
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the Create Shipment endpoint.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Cancel Shipment" icon="print">
      The integration for cancelling shipments.
    </Accordion>

    <br />

    <Callout icon="🚧" theme="warning">
      ### *Important*

      *FedEx will not charge customers for transportation costs. However, customs clearance fees may still apply if a package is not cancelled and scanned by FedEx.*
    </Callout>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add FedEx Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-fedex-shipping-account">
        Set up your FedEx shipping account to start creating shipments.
      </Card>

      <Card title="Add FedEx Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-fedex-tracking-account">
        Configure tracking for your FedEx shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT FedEx API" icon="fa-solid fa-code" href="">
        Explore the FedEx API endpoints.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with FedEx and manage your shipping operations from a single platform.
  </Card>
</Cards>
