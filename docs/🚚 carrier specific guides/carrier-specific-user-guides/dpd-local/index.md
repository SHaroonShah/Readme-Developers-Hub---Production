---
title: DPD Local
excerpt: >-
  DPD Local is part of DPD and Geopost, one of the world’s leading parcel
  delivery networks operating in over 50 countries. DPD Local is a sister
  company to DPD, and used to be called ‘Interlink Express’ until it was
  re-branded to DPD Local in 2017. Like DPD, DPD Local is a major carrier in the
  UK, offering both domestic and international shipping services.
deprecated: false
hidden: true
metadata:
  robots: index
---
> 🚧 _Important_
>
> _This integration is currently under development. The contents are to be updated as soon as possible._

DPD Local offers a range of specialist solutions and services. With over 6,000 drop-off locations throughout the UK, DPD Local gives customers the flexibility to arrange their deliveries around their needs. DPD Local also offers a range of collection services as well as free DPD Local tracking on every booking, whilst international shipping is available to send to one of over 200 countries worldwide at a low cost.

This in an in-house integration, which means that the <Glossary>label</Glossary> will be generated in the SAPIENT system. Additionally, an electronic <Glossary>manifest</Glossary> data file is sent to DPD Local via SFTP when the shipments are manifested.

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>.

## Service enhancements

The following are the key services are provided by the Asendia integration:

* **Proof of Identity**: Requires the receiver to present valid identification at the point of delivery.
* **Proof of Age**: Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
* **Pin Required**: A secure PIN is sent to the receiver, which must be provided upon delivery.
* **Pin Required & Proof of Age**: Requires PIN and age verification at the point of delivery for added security.

## Additional features

The FedEx integration provides the following additional features:

* **Consignment services**:  <Glossary>consignment</Glossary> services are supported, and DPD Local allows a maximum of 99 <Glossary>package</Glossary>s per consignment.
* **Hazardous shipments**: Hazmat shipments are only supported with the e-PAQ Select and Elite DG services.
* **Carrier specific fields**: The **CarrierSpecifics** object contains the following field:
  * **Format**: To specify whether the shipment to EU is either **B** (Boxable) or **N** (Non-boxable) on e-PAQ Standard and e-PAQ Plus services.

## Carrier API services

The following API services are provided by the Asendia integration:

* **Authenticate**: This API must be called first to exchange the API credentials for a token, which is used in the other API calls to Asendia.
* **AddAndPrintShipment**: The integration for creating shipments to reflect Asendia as a primary carrier and allowing users to create shipments using the **Create Shipment** that returns the <Glossary>label</Glossary> in base64 encoded format alongside a <Glossary>CN22</Glossary>. For postal services, a <Glossary>CN23</Glossary> is included with the label image for all dutiable shipments.
* **Tracking**: Retrieves the tracking data by calling the Asendia's API.
