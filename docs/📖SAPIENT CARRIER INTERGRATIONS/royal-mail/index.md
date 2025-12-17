---
title: Royal Mail
excerpt: >-
  _Royal Mail_ is a leading British postal service and courier company. It
  provides a wide range of services, including standard and express mail
  delivery, parcel distribution, logistics, and international shipping.
deprecated: false
hidden: false
icon: fad fa-truck-fast
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  pages:
    - slug: shipping-account-requirements
      title: Royal Mail shipping account setup
      type: basic
---
<Image align="center" border={false} width="120px" src="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png" />

***

The Royal Mail-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging Royal Mail's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Europe and the <Glossary>ROW</Glossary> (Rest of the World).
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

* **Create Shipment**: The integration for creating shipments to reflect Royal Mail as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Print Label**: Generate and return the label for the Royal Mail shipment. This endpoint is utilised after a Royal Mail shipment has been created and is meant to facilitate the printing of the label required for that shipment.

> 📘 _Note_
>
> _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._

* **Print My Label QR Code**: Generate an easy-to-scan QR code for the associated label specified in the **PrintLabel** API endpoint. This endpoint can only be used for Royal Mail Tracked Return services.
* **Pre Allocate Tracking Number**: Receive a Royal Mail Tracking Number that will be pre-allocated to the service and destination supplied in the request. No shipment or label will be produced using this endpoint. This endpoint can only be used for services that are assigned a tracking number.
* **Offline Barcoding**: Request a specific range of barcodes for use in your shipping processes. Offline Barcoding is only available if it has been activated on your customer account in the GUI.
* **PUDO Locations**: Retrieves a list of Pick-Up and Drop-Off (PUDO) locations associated with a specified carriers that are within a set radius of the postcode provided in the request. That radius is set to 10 Miles / 16.09 Kilometres. With this endpoint, you can find convenient locations for dropping off or picking up shipments, enhancing logistical efficiency and user experience.

> 🚧 _Important_
>
> _This endpoint must be called before the **Create Shipment** endpoint so that the desired PUDO location is selected in the Create Shipment request_.

* **International Arrivals Containers**: Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. Define which carrier and shipping location the container should be linked to.

  Unlike the common [Containers](https://docs.intersoftsapient.net/reference/get_v4-containers#/) API, the **International Arrivals Containers** endpoint is used for Royal Mail shipments that are being imported into GB only. For shipments in these containers, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with its associated ID, for better tracking and visibility purposes.

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

<br />

<HTMLBlock>{`
<Banner
  isInline={false}
  color="#118cfd"
  textColor="#ffffff"
  fontSize="14px"
  fontWeight="bold"
  imageSrc="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png"
  imageAlt="ReadMe favicon"
  linkHref="https://example.com"
  imageWidth="48px"
  imageHeight="48px"
/>
`}</HTMLBlock>

<Banner isInline={true} imageSrc="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png" linkHref="https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/royal-mail" message="" color="#118cfd" textColor="#ffffff" fontSize="14px" fontWeight="bold" />
