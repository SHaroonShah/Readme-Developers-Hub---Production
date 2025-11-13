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
Asendia is an API integration and in SAPIENT, it integrates with its newest AShipping solution. This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>ZPL203DPI</Glossary>.

## Enhancements

The following are the key services are provided by the Asendia integration:

* **e-PAQ Standard**: Untracked postal delivery, with low cost and high global reach. Last-mile delivery and customs clearance is handled by the country's postal service. This service includes the following: 
  * e-PAQ Standard Priority
  * e-PAQ Standard Non-Priority
* **e-PAQ Plus**: Tracked postal delivery, offering simplified customs processing. Last-mile delivery and customs clearance is handled by the country's postal service, utilising their tracked service. This service includes the following:
  * e-PAQ Plus Mailbox
  * e-PAQ Plus Personal
* **e-PAQ Select**: Home delivery service. offering full feature, and adapted to every market you sell in. Last-mile delivery is handled by a best-in-class parcel delivery partner in each country. This service includes the following:
  * e-PAQ Select DG (dangerous goods)
* **e-PAQ Elite**: Precision delivery service for your most time-critical and valuable shipments. Last-mile delivery is handled by courier partners that specialise in express and heavier weight shipments. This includes the following: 
  * e-PAQ Elite – Economy <Glossary>DAP</Glossary>
  * e_PAQ Elite – Economy with DAP incoterm
  * e_PAQ Elite – Express with DAP incoterm
  * e_PAQ Elite – Express with DDP incoterm
  * e_PAQ Elite – express Domestic
  * e_PAQ Elite – Express DAP DG 
  * e_PAQ Elite – Express DDP DG
  * e_PAQ Elite – Express Domestic DG

## Additional features

The FedEx integration provides the following additional features:

* **Single package shipments**: Asendia only support single package shipments.
* **Hazardous shipments**: Hazmat shipments are only supported with the e-PAQ Select and Elite DG services.
* **Carrier specific fields**: The **CarrierSpecifics** object contains the following fields: 
  * **Format**: To specify whether the shipment to EU is either **B** (Boxable) or **N** (Non-boxable) on e-PAQ Standard and e-PAQ Plus services.

## Carrier API services

The following API services are provided by the Asendia integration:

* **Authenticate**: This API must be called first to exchange the API credentials for a token, which is used in the other API calls to Asendia.
* **AddAndPrintShipment**: The integration for creating shipments to reflect Asendia as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Tracking**: Retrieves the tracking data by calling the Asendia's API. 
