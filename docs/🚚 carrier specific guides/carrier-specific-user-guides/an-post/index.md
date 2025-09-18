---
title: An Post
excerpt: >-
  An Post is the national postal service provider of Ireland. It offers a
  variety of services including mail delivery, parcel shipping, and financial
  services.  It provides a comprehensive range of postal services, including
  mail delivery, parcel shipping, and logistics solutions. An Post is known for
  its extensive network of post offices across Ireland, offering not just
  mailing services but also banking and government services.
deprecated: false
hidden: true
metadata:
  robots: index
---
<Image align="center" width="100px" src="https://files.readme.io/7e02be8b94572feafa989a21a47f67912c0f1afcaeb4b5e8339cd690e591cd46-image.png" />

***

The integration of An Post, Ireland's national postal service, into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Ireland (IE) and Great Britain (GB).
* **Ship to Destinations**: Users can send <Glossary>shipments</Glossary> to Ireland (IE), Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound and inbound shipping.

> 📘 _Note_
>
> _An Post does not support consignment services; all services are single-package services only. Also, the Express International and Priority Post services are only available to limited destinations._

* **Supported incoterms**: <Glossary>DDU</Glossary>
* **Label image formats**: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>
* **Integrations in scope**: The following integrations are added to the scope:
  * **Label integration**: This integration feature simplifies the process of generating and managing shipping labels in the standard 6x4 size, PDF format, which is essential for efficient logistics. Based on the destination country, customers must be aware of the following:
    * For delivery to addresses in Northern Ireland (IE), only the shipping <Glossary>label</Glossary> is required.
      * For delivery to EU destinations excluding Northern Ireland (IE), a security declaration is required.
      * The signature image will be taken from the signature image the customer has uploaded for the shipping account in the [Logos and Signatures](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) screen.
    * For delivery to ROW addresses, including GB and Northern Ireland (IE), a shipping label and <Glossary>CN23</Glossary> is required. Sapient will generate a separate address label and CN23, as this is consistent with the behaviour for other integrations.

> 📘 _Note_
>
> _Please be advised that the existing SAPIENT CN23 format will be used._

* **Tracking integration**: This integration allows users to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
* **Manifest or pre-advice integration**: This integration generate an electronic <Glossary>pre-advice</Glossary>/manifest file upon manifesting a shipment and sent to An Post via SFTP.

In this section, learn how to:

* [Add an An Post shipping account](https://docs.intersoftsapient.net/docs/add-an-post-shipping-account#/)
* [Add an An Post tracking account](https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/)
* [Add barcode range to an An Post shipping account](https://docs.intersoftsapient.net/docs/add-barcode-range-for-an-post-shipping-account#/)

<br />
