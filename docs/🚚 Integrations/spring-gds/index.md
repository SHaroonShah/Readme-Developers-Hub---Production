---
title: Spring GDS
excerpt: >-
  Spring Global Delivery Solutions (GDS) is a carrier aggregator providing
  international mail and parcel services through a network of final mile
  delivery partners.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/7a82628e4e235002d83f650d09fae2c0cda1c19c1cf18ba7da0d892bae962f24-Spring_banner_white.png" align="center" width="900px" />


***

The integration of Spring GDS into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) and European Union (UN).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), European Union (EU), Rest of the World ( <Glossary>ROW</Glossary>)
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping only.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> , <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>

      <Card title="Incoterms Support">
        The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary>.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards columns="1">
      <Card title="Single-package Services" icon="fad fa-box">
        Spring GDS supports only single-package services. Consignment services are not supported in this integration.
      </Card>

      <Card title="Carrier Specifics" icon="fad fa-list-check">
        he following fields are optional and are specified in the **CarrierSpecifics** block of the create shipment request.

        > _Before using the carrier-specific fields, please bear in mind the following:_
        >
        > - _Carrier-specific fields are only applicable to Spring Clear and default to false if not supplied and do not cause shipment validation failures when omitted._
        > - _Spring Clear cannot be configured at the shipping account level or via any UI setting in SAPIENT. It is not a configurable feature on our side and depends on the customer’s agreement and setup with Spring GDS._
        > - _If configured, you can trigger it by setting the incoterm to DDP in the create shipment request._

        - **Preferential Origin Tag:&#x20;**&#x49;ndicates whether the goods qualify for preferential origin under a trade agreement between the origin and destination countries, making them eligible for a reduced or zero customs duty rate. Set this field to true only if the goods meet the applicable rules of origin.
        - **Bonded Goods**: Indicates goods on which customs duty has not yet been paid yet, meaning they remain in a warehouse under customs supervision until the duty is settled.
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
    The following key services are provided by the InPost integration.

    | Service Name          | Description                                                                                                                                                                                                                                                                    |
    | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Labelled B2C**      | This service provides business-to-consumer parcel delivery using a printed shipping label, where the sender generates and attaches the label before drop-off at an InPost locker or shop.                                                                                      |
    | **Labelless Returns** | This service provides a label-free returns solution using a QR code, allowing customers to drop off parcels at the desired <Glossary>PUDO</Glossary> location, such as lockers or shops without printing labels, with tracking and labelling handled by InPost during transit. |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the&#x20;_[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_&#x20;endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect SPRING GDS as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Manifest shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.

      <Callout icon="📘" theme="info">
        ### _Note_

        _If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels._
      </Callout>
    </Accordion>

    <Accordion title="Get PUDO locations">
      Enable customers to users to access essential shipping options for both sending and returning packages seamlessly via the [Get PUDO Locations endpoint](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for an InPost shipment in the PDF format. This endpoint must be utilised when the label is not generated in the InPost Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add InPost Shipping Account" href="https://docs.intersoftsapient.net/docs/add-inpost-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your InPost shipping account to start creating shipments.
      </Card>

      <Card title="Add InPost Tracking Account" href="https://docs.intersoftsapient.net/docs/add-inpost-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your InPost shipments.
      </Card>

      <Card title="Use Inpost PUDO service" href="https://docs.intersoftsapient.net/docs/pudo-integration" icon="fa-solid fa-search-location" target="_blank">
        Utilise the SAPIENT Pick Up and Drop Off (PUDO) service to use a convenient out of home option to collect or return InPost parcels at designated locations.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT InPost API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost" icon="fa-solid fa-code" target="_blank">
        Explore the InPost API endpoints for a seamless shipping experience.
      </Card>

      <Card title="Get PUDO Locations" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost" icon="fa-solid fa-code" target="_blank">
        Explore the SAPIENT's core PUDO Locations endpoint to reetrieve a list of Pick-Up and Drop-Off (PUDO) locations associated with InPost.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Sign-Off">
    <Cards columns="2">
      <Card title="Inpost Sign-off Process" href="https://docs.intersoftsapient.net/docs/inpost-sign-off" icon="fa-solid fa-file-signature" target="_blank">
        Complete all the necessary steps before using InPost for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with InPost and manage your shipping operations from a single platform.
  </Card>
</Cards>
