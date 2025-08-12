---
title: InPost
excerpt: >-
  InPost is a Polish public logistics limited company with courier, package
  delivery and express mail service. The company specialises in parcel locker
  service operated in Poland, Italy, United Kingdom, France, Benelux, Spain, and
  Portugal.
deprecated: false
hidden: false
metadata:
  robots: index
---
<Image align="center" width="100px" src="https://files.readme.io/c9a342d05f1245bceed832bf7bb489e46969f9bddf8cb6b92007139484f4cf6b-InPost_logo.png" />

***

InPost provides a convenient, eco-friendly parcel delivery service through a network of 24/7 automated lockers and partnered shops in the UK. You can drop off or pick up parcels at these locations anytime, offering flexibility and ease for both senders and recipients.

InPost is launching an innovative and affordable parcel locker service in the UK, aimed at enhancing the shipping experience for both outbound and return deliveries. With its integration with SAPIENT, it offers several key features that streamline the shipping process. This article summarises the in-scope features of the integration and provides detailed explanations of the associated process flows.

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotland).
* **Ship to Destinations**: Users can send <Glossary>shipments</Glossary> to the Great Britain (GB) mainland only.
* **Service Type**: The integration is focused on outbound and return shipping.
* **InPost shipping services**: These services include the following:
  * **Labelled B2C**: to generate and return a <Glossary>label</Glossary> to be attached to the parcel for a B2C <Glossary>business transaction type</Glossary> deliveries.
  * **Labelless returns using QR codes**: to generate a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.
* **API endpoints for shipment creation and QR code retrieval**: The integration includes specific API endpoints that developers can use to create shipments, get PUDO locations, and retrieve labels or QR codes. This enables seamless interaction between the InPost service and SAPIENT system, ensuring efficient data flow and functionality.
  * Create Parcel endpoint for B2C service
  * Create Parcel endpoint for returns service
  * Get Label/QR code endpoint
  * Get PUDO Locations endpoint

In this section, learn how to:

* <Anchor label="Add an InPost shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-inpost-shipping-account#/">Add an InPost shipping account</Anchor>
* [Use InPost PUDO service](https://docs.intersoftsapient.net/docs/pudo-integration#/)