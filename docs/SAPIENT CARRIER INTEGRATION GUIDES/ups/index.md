---
title: UPS (United Parcel Service)
excerpt: >-
  _UPS (United Parcel Service)_ is a global logistics and package delivery
  company headquartered in the US. UPS operates in over 200 countries and
  territories, providing extensive international shipping options that allow
  businesses to reach customers around the globe. UPS offers a comprehensive
  array of services, including ground shipping, air freight, and much more.
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
      slug: shipping-account-setup
      title: UPS shipping account setup
---
<Image align="center" width="900px" src="https://files.readme.io/1efbc69974d8c513405bf78d99ce1607bc40f3d646b3cd90bed19cdd8e454ad8-UPS_white_banner.png" />

***

The UPS carrier integration within the SAPIENT system enables seamless communication between SAPIENT and UPS’s shipping services. This integration allows customers to efficiently create shipments and track deliveries in real time, directly within the SAPIENT system.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={3}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World). This may include a specific country list, if applicable.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary>, and <Glossary>ZPL203DPI</Glossary> formats.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={2}>
      <Card title="Multi-piece Shipments" icon="fa-solid fa-boxes-stacked">
        UPS supports a maximum of 99999 pieces per single shipment request.
      </Card>

      <Card title="Label Integration" icon="fa-solid fa-tag">
        This integration is in-house, which means that the label is generated within the SAPIENT system without calling the carrier API.
      </Card>

      <Card title="Tracking Integration" icon="fa-solid fa-location-dot">
        Tracking data can be sent via the Tracking API.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    * **Email Notification**: To use this enhancement, you must provide a valid email address.
    * **QV (Quantum View) Ship**: Sends an email notification to the shipper when the shipment has been shipped.
    * **QV Exception**: Notifies the shipper via email if there is an exception or issue with the shipment during transit.
    * **QV Delivery**: Allows UPS to send an email notification to the shipper when the shipment has been successfully delivered.
    * **Alternate Delivery Location**: Sends an email notification to the shipper with details of the alternative delivery location if the package cannot be delivered to the original address.
    * **Saturday Delivery**: Permits delivery on Saturdays, offering greater flexibility in shipping schedules.
    * **Adult Signature**: Requires an adult signature upon delivery, ensuring that the package is received by someone of legal age.
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the UPS integration.

    | Service Name                                         | Description                                                                                                                                                                                                                                                                             |
    | :--------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **UPS Worldwide Express** (1-3 business days)        | This service provides guaranteed morning, next-business-day delivery to and from most business areas within the country and day-definite delivery within three days for international shipments from more than 45 countries and territories to more than 185 countries and territories. |
    | **UPS Standard** (1-5 business days)                 | This service provides scheduled day-definite delivery to and from most addresses within the country and scheduled day-definite delivery within five days for international shipments to and from more than 30 countries and territories.                                                |
    | **UPS Worldwide Expedited** (2-5 business days)      | This service provides day-definite delivery to over 220 countries and territories. Fully tracked, with generous weight limits (up to 150 lbs).                                                                                                                                          |
    | **UPS Worldwide Expedited Plus** (next business day) | This service provides premium express service with the fastest international delivery times.                                                                                                                                                                                            |
    | **UPS Worldwide Saver** (1-3 business days)          | This service provides guaranteed afternoon delivery to over 215 countries. and territories.                                                                                                                                                                                             |

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For the most up-to-date carrier services, use the[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint.*
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect UPS as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a UPS shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

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
      <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/shipping-account-setup" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up a UPS shipping account on SAPIENT.
      </Card>

      <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/tracking-2" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up a UPS tracking account on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT UPS API" href="https://docs.intersoftsapient.net/v4.03/reference/post_v4-shippingaccounts-ups" icon="fa-solid fa-code">
        Explore the UPS API endpoints for creating and managing UPS shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with UPS and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
