---
title: DHL Germany (DE)
excerpt: >-
  DHL Germany(DE) is a brand within the DHL group, used for shipping from
  Germany. They provide domestic shipping within Germany and international
  shipping to EU and ROW destinations.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/1c75f5e50dcdc7dfcdde00afa6ddf1f96bb34d0a329a8f93155a21e02605cc47-DHL_DE_banner_white.png" align="center" width="900px" />


***

The integration of DHL Germany (DE) into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        The integration supports shipping from locations in Germany only.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single piece shipments" icon="fa-solid fa-box">
        DHL Germany supports only single-package services. Consignment services are not supported in this integration.
      </Card>

      <Card title="Future-date shipments" icon="fa-solid fa-box-circle-check">
        DHL Germany allow shipments to be created up to one year in advance, so the SAPIENT maximum of 28 days will apply.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key services enhancements provided by the DHL Germany integration:

    - **Preferred Neighbour**: Specifies a preferred neighbour to receive the shipment on recipient's behalf.   
    - **Preferred Location**: Specifies a preferred delivery location, such as a safe place or a specific entry point at the recipient’s address if they are unavailable.
    - **Visual Check of Age**: Specifies the minimum age to be verified upon delivering age-restricted items. This field provides the following options:
      - **Age 16:** Recipient must be verified to be at least 16 years of age.
      - **Age 18**: Recipient must be verified to be at least 18 years of age.
    - **Named Person Only**: Specifies that the shipment is delivered only to the specified named person at the recipient's address and no one else.
    - **No Neighbour Delivery**: A flag indicating that deliveries should not be made to neighbors.
    - **Premium**: Specifies options for premium parcel delivery. This enhancement is country-dependent and may be adjusted by DHL if the selected option is not available.
    - **Closest Drop Point**: Specifies delivery to the drop point nearest to the recipient's address. To use this enhancement, one of the following information must be provided: 
      - Destination **ContactEmail** with a valid email address
      - Destination **ContactPhone** with a valid phone number
    - **Go Green Plus**: An enhancement indicating a commitment to environmentally friendly delivery methods by investing in measures to reduce greenhouse gas emissions at DHL.
    - **Endorsement**: Specifies handling instructions for undeliverable international shipments, using any of the following values:
      - **Return**: The undeliverable shipment is returned to the shipper.
      - **Abandon**: The undeliverable shipment is abandoned
    - **Bulky Goods**: A flag indicating whether the shipment includes bulky goods, for example, items that are large in size and shape and consume a large amount of space.

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements and carrier services, refer to the following endpoints:_

      - _[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dhlde)_
      - _[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the DHL Germany integration.

    | Service Name                | Description                                                                                                                                                                                     |
    | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **DHL Paket**               | This service provides reliable domestic parcel delivery within Germany, typically within 1–2 working days, with tracking, liability cover, and flexible delivery options.                       |
    | **DHL Paket International** | This service provides international parcel delivery to over 220 countries and territories, offering door-to-door shipping with tracking, customs handling, and reliable transit times.          |
    | **DHL Europaket**           | This service provides reliable parcel delivery across European destinations, offering cross-border shipping with defined transit times, tracking, and customs support where required.           |
    | **DHL Kleinpaket**          | This service provides cost-effective shipping for small, lightweight goods within Germany, including tracking, delivery confirmation, and liability coverage for low-value items.               |
    | **Warenpost International** | This service provides affordable international delivery for small, lightweight goods, offering flexible shipping options with optional tracking and customs processing for global destinations. |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect DHL Germany as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Cancel Shipment">
      The integration to cancel any unwanted shipments, to ensures that cancellations are fully registered with DHL Germany, helping prevent customers from being mistakenly charged for cancelled shipments. <br />

      <Callout icon="info" theme="info">
        ### _Note_

        _Shipments can only be cancelled if they have not been manifested._
      </Callout>
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a DHL Germany shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

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
      <Card title="Add DHL Germany Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dhl-de-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your DHL Germany shipping account to start creating shipments.
      </Card>

      <Card title="Add DHL Germany Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dhl-de-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your DHL Germany shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT DHL Germany API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dhlde" icon="fa-solid fa-code" target="_blank">
        Explore the DHL Germany API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DHL Germany and manage your shipping operations from a single platform.
  </Card>
</Cards>
