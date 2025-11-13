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

## Enhancements

The following are the key services provided by the Asendia integration:

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
  * e_PAQ Elite – Economy <Glossary>DDP</Glossary>
  * e_PAQ Elite – Express DAP
  * e_PAQ Elite – Express DDP
  * e_PAQ Elite – express Domestic
  * e_PAQ Elite – Express DAP DG
  * e_PAQ Elite – Express DDP DG
  * e_PAQ Elite – Express Domestic DG
* **Declared Values**: A surcharge is applicable if the requested declared value of the shipment exceeds the liability stated in FedEx's terms and conditions for the selected service. The _declared value_ of a package represents the maximum liability in connection with the shipment of the package, including, but not limited to, any loss, damage, delay, or missed delivery relating to that shipment. As the shipper, it’s your responsibility to prove any actual damages. Exposure to and risk of any loss in excess of your declared value is assumed by you.
* **Signature options**: Enhanced signature options include:
  * **Adult signature**: To obtain a signature from any person of legal age at the delivery address, subject to the provision of a valid ID. If no one qualified to sign is available, an attempt will be made to redeliver the package on another date. Legal age varies depending on the destination country/territory and is governed by local legal age of an adult, not the legal age to purchase specific products.
  * **Direct signature**: To obtain a signature from someone at the delivery address only. If no one is available to sign, a redelivery attempt of the package will be made on another date.
  * **Indirect signature**: To obtain a signature from someone at the delivery address, from a neighbour or from a building manager. If no one is available to sign, the package will be delivered on another date.
  * **No signature required**: To obtain a signature at the delivery address. If no one is available to sign, the package will be kept in a safe place without obtaining the signature.
* **Email notifications**: Notifications available on delivery, estimated delivery, exceptions, shipment status, and tender.

## Additional features

The FedEx integration provides the following additional features:

* **Multipiece shipments**: Support for multipiece shipments is included in the integration.
* **Package Types**: FedEx offers its own distinct <Glossary>package type</Glossary>s. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid), <Glossary>DDP</Glossary> (Delivered Duty Paid), and <Glossary>DAP</Glossary> (Delivered At Place).
* **Electronic Trade Document (ETD)**: Inclusion of electronic trade documents, such as  <Glossary>commercial invoice</Glossary>, <Glossary>proforma invoice</Glossary>, and in some cases, other specific documents. while configuring the FedEx <Glossary>shipping account</Glossary>. This solution solution allows you to create and send your trade documents electronically when shipping internationally.

## Carrier API services

The following API services are provided by the FedEx integration:

* **Create Shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Cancel Shipment**: The integration for cancelling shipments.

> 🚧 _Important_
>
> _This integration is currently under development. The contents are to be updated as soon as possible._
