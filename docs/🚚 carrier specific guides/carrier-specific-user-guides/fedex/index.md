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
<Image align="center" width="100px" src="https://files.readme.io/7fdbe37491cd4cb64c9b34a2eb87c9e0f35428aececde1dff435205b1d970a6e-FedEx.png" />

The FedEx-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging FedEx's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) and Europe.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping and returns.

## Enhancements

The following are the key enhancements provided by the FedEx integration:

* **Saturday Delivery**: The option to deliver packages on Saturdays for added convenience.
* **Enhanced transit Liability**: A surcharge is applicable if the requested enhanced value of the shipment exceeds the liability stated in FedEx's terms and conditions for the selected service.
* **Signature options**: Enhanced signature options include:
  * Adult signature
  * Direct signature
  * Indirect signature
  * No signature required
  * **Email notifications**: Notifications available on delivery, estimated delivery, exceptions, shipment status, and tender.

## Additional features

The FedEx integration provides the following additional features:

* **Multipiece shipments**: Support for multipiece shipments is included in the integration.
* **Package Types**: FedEx offers its own distinct <Glossary>package type</Glossary>s.
* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid), <Glossary>DDP</Glossary> (Delivered Duty Paid), and <Glossary>DAP</Glossary> (Delivered At Place)
* **Electronic Trade Document (ETD)**: Inclusion of electronic trade documents while configuring the FedEx <Glossary>shipping account</Glossary>.

## Carrier API services

The following API services are provided by the FedEx integration:

* **Create Shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Cancel Shipment**: The integration for cancelling shipments.

> 🚧 *Important*
>
> *It is important to note that FedEx will not charge customers for transportation costs. However, the customs clearance fees may still apply if a package is not cancelled and scanned by FedEx.*

* **Upload Images**: Users can upload their logo and signature images for use on commercial invoices. This information is included as part of the electronic trade document.

In this section, learn how to:

* Add a FedEx shipping account
* Add a FedEx tracking account

> 📘 *Note*
>
> *For more information on how to activate the FedEx integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section.*