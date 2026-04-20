---
title: Add DHL DE shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: true
icon: fad fa-square-plus
metadata:
  robots: index
---
In SAPIENT, with the Add Shipping Account functionality, you can select the desired shipping location and then add a DHL Germany shipping account to it.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have enabled the [label integration](https://docs.intersoftsapient.net/docs/integration-activation) for DHL Germany._

## Key features

* **Ship from destinations**: The integration supports shipping from locations in Germany only.
* **Ship To Destinations**: Users can send shipments domestically within Germany, to Great Britain (GB), Europe (EU), and <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping only.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary> (SAPIENT converts the PDF label image to PNG as standard), <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary>.

## Service enhancements

The following are the key services are provided by the DHL Germany integration:

* Preferred Neighbour: Specifies a preferred neighbour to receive the shipment on recipient's behalf.   
* Preferred Location: Specifies a preferred delivery location, such as a safe place or a specific entry point at the recipient’s address if they are unavailable.
* Visual Check of Age: Specifies the minimum age to be verified upon delivering age-restricted items. This field provides the following options:
  * Age 16: Recipient must be verified to be at least 16 years of age.
  * Age 18: Recipient must be verified to be at least 18 years of age.
* Named Person Only: Specifies that the shipment is delivered only to the specified named person at the recipient's address and no one else.
* No Neighbour Delivery: A flag indicating that deliveries should not be made to neighbors.
* Premium: Specifies options for premium parcel delivery. This enhancement is country-dependent and may be adjusted by DHL if the selected option is not available.
* Closest Drop Point: Specifies delivery to the drop point nearest to the recipient's address. To use this enhancement, one of the following information must be provided: 
  * Destination ContactEmail with a valid email address
  * Destination ContactPhone with a valid phone number
* Go Green Plus: An enhancement indicating a commitment to environmentally friendly delivery methods by investing in measures to reduce greenhouse gas emissions at DHL.
* Endorsement: Specifies handling instructions for undeliverable international shipments, using any of the following values:
  * Return: The undeliverable shipment is returned to the shipper.
  * Abandon: The undeliverable shipment is abandoned
* Bulky Goods: A flag indicating whether the shipment includes bulky goods, for example, items that are large in size and shape and consume a large amount of space.
