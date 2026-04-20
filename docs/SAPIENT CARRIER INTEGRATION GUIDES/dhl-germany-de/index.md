---
title: DHL Germany (DE)
excerpt: >-
  DHL Germany(DE) is a brand within the DHL group, used for shipping from
  Germany. They provide domestic shipping within Germany and international
  shipping to EU and ROW destinations.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
The integration of DHL Germany into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

## Key features

* **Ship from destinations**: The integration supports shipping from locations in Germany only.
* **Ship To Destinations**: Users can send shipments domestically within Germany, to Great Britain (GB), Europe (EU), and <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping only.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary> (SAPIENT converts the PDF label image to PNG as standard), <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary>.

## Service enhancements

The following are the key services are provided by the DHL Germany integration:

* **Preferred Neighbour**: Specifies a preferred neighbour to receive the shipment on recipient's behalf.   
* **Preferred Location**: Specifies a preferred delivery location, such as a safe place or a specific entry point at the recipient’s address if they are unavailable.
* **Visual Check of Age**: Specifies the minimum age to be verified upon delivering age-restricted items. This field provides the following options:
  * **Age 16:** Recipient must be verified to be at least 16 years of age.
  * **Age 18**: Recipient must be verified to be at least 18 years of age.
* **Named Person Only**: Specifies that the shipment is delivered only to the specified named person at the recipient's address and no one else.
* **No Neighbour Delivery**: A flag indicating that deliveries should not be made to neighbors.
* **Premium**: Specifies options for premium parcel delivery. This enhancement is country-dependent and may be adjusted by DHL if the selected option is not available.
* **Closest Drop Point**: Specifies delivery to the drop point nearest to the recipient's address. To use this enhancement, one of the following information must be provided: 
  * Destination **ContactEmail** with a valid email address
  * Destination **ContactPhone** with a valid phone number
* **Go Green Plus**: An enhancement indicating a commitment to environmentally friendly delivery methods by investing in measures to reduce greenhouse gas emissions at DHL.
* **Endorsement**: Specifies handling instructions for undeliverable international shipments, using any of the following values:
  * **Return**: The undeliverable shipment is returned to the shipper.
  * **Abandon**: The undeliverable shipment is abandoned
* **Bulky Goods**: A flag indicating whether the shipment includes bulky goods, for example, items that are large in size and shape and consume a large amount of space.

## Additional features

The DHL Germany integration provides the following additional features:

* **Single-package services**: DHL Germany supports only single-package services. Consignment services are not supported in this integration.
* **Future-date shipments**: DHL Germany allow shipments to be created up to one year in advance, so the SAPIENT maximum of 28 days will apply.

## Carrier API services

The following API services are provided by the DHL Germany integration:

* **Create shipment**: The integration for creating shipments to reflect DHL Germany as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
* **Cancel shipment**: The integration for cancelling any unwanted shipments in the system.

> 📘 _Note_
>
> _Shipments can only be cancelled if they have not been manifested._

* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
* **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).

***

In this section, learn how to:

* [Add an An Post shipping account](https://docs.intersoftsapient.net/docs/add-an-post-shipping-account#/)
* [Add an An Post tracking account](https://docs.intersoftsapient.net/docs/add-an-post-tracking-account#/)
* [Add barcode range to an An Post shipping account](https://docs.intersoftsapient.net/docs/add-barcode-range-for-an-post-shipping-account#/)

> 📘 _Note_
>
> _For more information on how to activate the An Post integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._
