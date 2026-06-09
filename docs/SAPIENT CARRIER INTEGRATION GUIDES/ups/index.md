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
    <Cards columns={1}>
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
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Carrier Services">
    <Cards columns={1}>
      <Card title="UPS Worldwide Express" icon="fa-solid fa-plane-departure">
        This service provides guaranteed morning, next-business-day delivery to and from most business areas within the country and day-definite delivery within three days for international shipments from more than 45 countries and territories to more than 185 countries and territories.
      </Card>

      <Card title="UPS Standard" icon="fa-solid fa-truck">
        This service provides scheduled day-definite delivery to and from most addresses within the country and scheduled day-definite delivery within five days for international shipments to and from more than 30 countries and territories.
      </Card>

      <Card title="UPS Worldwide Expedited" icon="fa-solid fa-earth-americas">
        This service provides day-definite delivery to over 220 countries and territories. Fully tracked, with generous weight limits up to 150 lbs.
      </Card>

      <Card title="UPS Worldwide Expedited Plus" icon="fa-solid fa-gauge-high">
        This service provides premium express service with the fastest international delivery times.
      </Card>

      <Card title="UPS Worldwide Saver" icon="fa-solid fa-business-time">
        This service provides guaranteed afternoon delivery to over 215 countries and territories.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API Capabilities">
    <Cards columns={1}>
      <Card title="Create Shipment" icon="fa-solid fa-box">
        Create shipments using UPS as a primary carrier through the Create Shipment endpoint.
      </Card>

      <Card title="Tracking" icon="fa-solid fa-search-location">
        Track and monitor shipments in real time by receiving automatic updates on shipment status, delivery progress, and exceptions.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />

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