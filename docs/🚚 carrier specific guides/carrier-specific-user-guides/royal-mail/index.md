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

The following are the key enhancements provided by the Royal Mail integration:

* **CL1** - Consequential Loss £1000: Coverage for losses up to £1000.
* **CL2** - Consequential Loss £2500: Coverage for losses up to £2500.
* **CL3** - Consequential Loss £5000: Coverage for losses up to £5000.
* **CL4** - Consequential Loss £7500: Coverage for losses up to £7500.
* **CL5** - Consequential Loss £10000: Coverage for losses up to £10000
* **Signed**: A signature is required upon delivery, applicable to 24, 48, 1st Class, and 2nd Class services.
* **SMS**: Provides delivery updates via SMS for Special Delivery Guaranteed, Tracked, and Tracked High Volume services.
* **Email**: Sends delivery updates via email for eligible services, such as Special Delivery Guaranteed, Tracked and Tracked High Volume, International Tracked and International Tracked and Signed services.
* **Safeplace**: The shipment will be left in a specified safe place location; details must be provided in the SafeplaceLocation field. Can be used with Tracked, Tracked High Volume and 24/48 services.
* **LocalCollect**: The shipment will be delivered to a Post Office for collection by the receiver.  Can be used with Special Delivery Guaranteed, Tracked and Tracked High Volume services.
* **CustomsEmail**: The receiver's email address will be included in eCustoms data. This enhancement code can be used with international services.
* **CustomsPhone**: The receiver's phone number will be included in eCustoms data. This enhancement code can be used with international services.

## Additional features

The Royal Mail integration provides the following additional features:

* **Multipiece shipments**: Support for multipiece shipments is included in the integration.
* **Package Types**: Royal Mail offers its own distinct <Glossary>package type</Glossary>s, such as Letter, Large letter, Parcel, and Printed papers. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
* **Incoterms**: The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, <Glossary>DAP</Glossary>, and <Glossary>DAT</Glossary>.

## Carrier API services

The following API services are provided by the Royal Mail integration:

* **Create Shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Print Label**:
* **Print My Label QR Code**:
* **Pre Allocate Tracking Number**:
* **Offline Barcoding**: 
* **PUDO Locations**: The integration for cancelling shipments.
* **International Arrivals Containers**:

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
