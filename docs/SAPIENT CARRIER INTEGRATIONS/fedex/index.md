---
title: FedEx
excerpt: >-
  FedEx is a global leader in logistics and delivery services, renowned for its
  reliable express shipping and comprehensive transportation solutions. It
  offers a range of shipping options tailored for various international markets,
  making it an essential partner for businesses seeking to optimize their
  shipping operations.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Image align="center" border={false} width="100px" src="https://files.readme.io/88a7599e1a64e2eb5cd20cc992a3a87dc3b68ebb766615ba6766c7f560586e5e-FedEx_White_BG.png" />

***

The FedEx-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging FedEx's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) and Europe.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid), <Glossary>DDP</Glossary> (Delivered Duty Paid), and <Glossary>DAP</Glossary> (Delivered At Place).
* **Service Type**: The integration is focused on outbound shipping.

## Enhancements

The following are the key enhancements provided by the FedEx integration:

* **Saturday Delivery**: The option to deliver packages on Saturdays for added convenience.
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
* **Electronic Trade Document (ETD)**: Inclusion of electronic trade documents, such as  <Glossary>commercial invoice</Glossary>, <Glossary>proforma invoice</Glossary>, and in some cases, other specific documents. while configuring the FedEx <Glossary>shipping account</Glossary>. This solution solution allows you to create and send your trade documents electronically when shipping internationally.

## Carrier API services

The following API services are provided by the FedEx integration:

* **Create Shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Cancel Shipment**: The integration for cancelling shipments.

> 🚧 _Important_
>
> _It is important to note that FedEx will not charge customers for transportation costs. However, the customs clearance fees may still apply if a package is not cancelled and scanned by FedEx._

In this section, learn how to:

* [Add a FedEx shipping account](https://docs.intersoftsapient.net/docs/add-fedex-shipping-account#/)
* [Add a FedEx tracking account](https://docs.intersoftsapient.net/docs/add-fedex-tracking-account#/)

> 📘 _Note_
>
> _For more information on how to activate the FedEx integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._
