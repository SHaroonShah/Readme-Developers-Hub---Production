---
title: Royal Mail
excerpt: >-
  _Royal Mail_ is a leading British postal service and courier company. It
  provides a wide range of services, including standard and express mail
  delivery, parcel distribution, logistics, and international shipping.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - slug: shipping-account-requirements
      title: Royal Mail shipping account setup
      type: basic
---
<Image align="center" width="120px" src="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png" />

***

The Royal Mail-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging Royal Mail's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on inbound outbound shipping.

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
* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid), <Glossary>DDP</Glossary> (Delivered Duty Paid), and <Glossary>DAP</Glossary> (Delivered At Place).
* **Electronic Trade Document (ETD)**: Inclusion of electronic trade documents, such as  <Glossary>commercial invoice</Glossary>, <Glossary>proforma invoice</Glossary>, and in some cases, other specific documents. while configuring the FedEx <Glossary>shipping account</Glossary>. This solution solution allows you to create and send your trade documents electronically when shipping internationally.

## Carrier API services

The following API services are provided by the FedEx integration:

* **Create Shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Cancel Shipment**: The integration for cancelling shipments.

In this section, learn how to:

* [Set up Royal Mail Online Business Account (OBA)](https://docs.intersoftsapient.net/docs/oba-email-validation)
* [Set up Royal Mail shipping account](https://docs.intersoftsapient.net/docs/shipping-account-requirements)
* [Set up Royal Mail tracking account](https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup)
* [Create BFPO shipments](https://docs.intersoftsapient.net/docs/bfpo-shipments)
* [Return shipments](https://docs.intersoftsapient.net/docs/royal-mail-returns)
* [Use pre-allocated tracking number](https://docs.intersoftsapient.net/docs/use-the-royal-mail-pre-allocated-tracking-number)
* [Use collection service](https://docs.intersoftsapient.net/docs/royal-mail-parcel-collect)
* [Use PUDO service](https://docs.intersoftsapient.net/docs/use-local-collect-shipment-service#/)
* [Set up international arrival containers](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers)
