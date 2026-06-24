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
The FedEx-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging FedEx's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

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
        FedEx offers its own distinct <Glossary>package type</Glossary>s.

        > *For more information on the carrier package types, use the<Anchor label="Get Carrier Service Package Types" target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/">Get Carrier Service Package Types</Anchor> endpoint.*
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
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the Create Shipment endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>

    <br />

    <Accordion title="Cancel Shipment">
      The integration to cancel any unwanted shipments, to ensures that cancellations are fully registered with FedEx, helping prevent customers from being mistakenly charged for cancelled shipments.
    </Accordion>

    <br />

    <Callout icon="🚧" theme="warning">
      ### *Important*

      *FedEx will not charge customers for transportation costs. However, customs clearance fees may still apply if a package is not cancelled and scanned by FedEx.*
    </Callout>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a DHL Germany shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>
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
      <Card title="SAPIENT FedEx API" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-fedex">
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
