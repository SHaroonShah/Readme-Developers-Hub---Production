---
title: Asendia
excerpt: >-
  Asendia is a global e-commerce and mail delivery specialist and is a joint
  venture, between La Poste and Swiss Post, offering international delivery to
  over 200 countries, handling final mile delivery via partner couriers. 
deprecated: false
hidden: true
metadata:
  robots: index
---
> 🚧 _Important_
>
> _This integration is currently under development. The contents are to be updated as soon as possible._

Asendia is an API integration and in SAPIENT, it integrates with its newest AShipping solution.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>ZPL203DPI</Glossary>.

## Carrier shipping services

The following are the key services are provided by the Asendia integration:

* **e-PAQ Standard**: Untracked postal delivery, with low cost and high global reach. Last-mile delivery and customs clearance is handled by the country's postal service. This service includes the following:
  * e-PAQ Standard Priority
  * e-PAQ Standard Non-Priority
* **e-PAQ Plus**: Tracked postal delivery, offering simplified customs processing. Last-mile delivery and customs clearance is handled by the country's postal service, utilising their tracked service. This service includes the following:
  * e-PAQ Plus Mailbox
  * e-PAQ Plus Personal
* **e-PAQ Select**: Home delivery service. offering full feature, and adapted to every market you sell in. Last-mile delivery is handled by a best-in-class parcel delivery partner in each country. This service includes the following:
  * e-PAQ Select
  * e-PAQ Select, shipping dangerous goods
* **e-PAQ Elite**: Precision delivery service for your most time-critical and valuable shipments. Last-mile delivery is handled by courier partners that specialise in express and heavier weight shipments. This service includes the following with domestic and international shipping, including hazardous items:
  * e-PAQ Elite – Economy
  * e_PAQ Elite – Express

## Additional features

The Asendia integration provides the following additional features:

* **Single package shipments**: Asendia only support single package shipments.
* **Hazardous shipments**: Hazmat shipments are only supported with the e-PAQ Select and Elite DG services.
* **Carrier specific fields**: The **CarrierSpecifics** object contains the following field:
  * **Format**: To specify whether the shipment to EU is either **B** (Boxable) or **N** (Non-boxable) on e-PAQ Standard and e-PAQ Plus services.

## Carrier API services

The following API services are provided by the Asendia integration:

* **Create shipment**: The integration for creating shipments to reflect Asendia as a primary carrier and allowing users to create shipments using the **Create Shipment** that returns the <Glossary>label</Glossary> in base64 encoded format alongside a <Glossary>CN22</Glossary>. For postal services, a <Glossary>CN23</Glossary> is included is returned in the **Documents** section of the response for all <Glossary>dutiable shipments</Glossary>.
* **Tracking**: Retrieves the tracking data via the tracking webhook.

<br />
