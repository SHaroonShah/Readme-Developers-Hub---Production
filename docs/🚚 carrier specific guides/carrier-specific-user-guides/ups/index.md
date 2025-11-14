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
<Image align="center" border={false} width="60px" src="https://files.readme.io/afec4e485f461b873476f04e7712572b474ba6552fdacea5d984530b5e16cd5b-image.png" />

***

The UPS carrier integration within the SAPIENT system enables seamless communication between SAPIENT and UPS’s shipping services. This integration allows customers to efficiently create shipments and track deliveries in real time, directly within the SAPIENT system.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World). This may include a specific country list, if applicable.
* **Incoterms**: The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary>, and <Glossary>ZPL203DPI</Glossary>.
* **Service Type**: The integration is focused on outbound shipping.

## Carrier services

The following carrier services are included in the integration:

* **UPS Worldwide Express** (1-3 business days): This service provides guaranteed morning, next-business-day delivery to and from most business areas within the country and day-definite delivery within three days for international shipments from more than 45 countries and territories to more than 185 countries and territories.
* **UPS Standard** (1-5 business days): This service provides scheduled day-definite delivery to and from most addresses within the country and scheduled day-definite delivery within five days for international shipments to and from more than 30 countries and territories.
* **UPS Worldwide Expedited** (2-5 business days): This service provides day-definite delivery to over 220 countries and territories. Fully tracked, with generous weight limits (up to 150 lbs).
* **UPS Worldwide Expedited Plus** (next business day): This service provides premium express service with the fastest international delivery times.
* **UPS Worldwide Saver** (1-3 business days): This service provides guaranteed afternoon delivery to over 215 countries. and territories.

## Service enhancements

The following are the key enhancements provided by the UPS integration:

* Email notification: To use this enhancement, you must provide a valid email address. This enhancement includes the following codes:
  * **QV (Quantum View) ship**: An enhancement code that sends an email notification to the shipper when the shipment has been shipped.
  * **QV exception**: An enhancement code that notifies the shipper via email if there is an exception or issue with the shipment during transit.
  * **QV delivery**: An enhancement code that allows UPS to send an email notification to the shipper when the shipment has been successfully delivered.
  * **Alternate Delivery Location**: An enhancement code that sends an email notification to the shipper with details of the alternative delivery location if the package cannot be delivered to the original address.
  * **Saturday Delivery**: An enhancement code that permits delivery on Saturdays, offering greater flexibility in shipping schedules.
  * **Adult Signature**: An enhancement code that requires an adult signature upon delivery, ensuring that the package is received by someone of legal age.

## Additional features

The UPS integration provides the following additional features:

* **Multi-piece shipments**: Supports a maximum of 99999 pieces per single shipment request.

## Carrier API services

The following API services are provided by the UPS integration:

* **Authorisation**: The integration to authenticate and authorise users to use the carrier services via API.
* **Create Shipment**: The integration for creating shipments to reflect UPS as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Tracking**: The integration to track and monitor shipments in real time by receiving automatic updates on shipment status, delivery progress, and exceptions.

## Integration types

The following integration types are available for this integration:

* **Label integration**: This integration is In-house, which means that the label is generated within the SAPIENT system without calling the carrier API.
* **Tracking integration**: Enables the tracking data to be sent via the Tracking API.

In this section, learn how to:

* [Add UPS shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup)
* [Add UPS tracking account](https://docs.intersoftsapient.net/docs/tracking-2)

<br />
