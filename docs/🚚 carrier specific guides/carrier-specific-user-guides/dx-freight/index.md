---
title: DX Freight
excerpt: >-
  _DX_ is a UK-based logistics and parcel delivery company that specialises in
  providing tailored delivery solutions for businesses and individuals. DX
  offers a wide range of delivery options, including time-sensitive and next-day
  services, focusing on delivering parcels, documents, and heavy items.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Image align="center" border={false} width="130px" src="https://files.readme.io/9b5162bacf5f3ac36b0200401aa0441bd609545eaf01e789087d520c1455ca64-DX_freight_logo.png" />

***

Freight is one of DX's core solutions, also referred to as _IDW_ (Irregular Dimensions and Weight), that provides delivery services to businesses and home addresses for multi-item <Glossary>consignment</Glossary>s, pallets up to 6 metres in length, and individual <Glossary>items</Glossary> in excess of 25 kg in weight.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Channel Islands.

> 📘 _Note_
>
> _Shipments to Channel Islands are treated as domestic destination for freight shipments._

* **Service Type**: The integration is focused on outbound shipping.

## Carrier services

The following are one of the main DX Freight service types tailored to meet different delivery requirements:

* **DX-1**: a 1 man service type that is typically deigned for door to door standard next-day delivery of parcels weighing up to a specific limit (50 kg) to the capability of effectively handling pallets. This service is usually best for smaller and lighter <Glossary>package</Glossary>s. 1Man service type includes the following services:
  * **ON**: Overnight
  * **3D**: 3Day
  * 930: Overnight 9:30
  * AM: Overnight pre noon
  * SAT: Saturday
  * S93: Saturday 9:30
* **DX-2**:  a 2 man service type that caters to larger and heavier <Glossary>shipments</Glossary>, typically allowing for items that require 2-person handling due to their size or weight. This service is useful particularly for businesses that deal with bulky items or items that cannot be managed by one person. 2Man service type includes the following services:
  * **H1**: 2Man Overnight
  * **H2**: 2Man Standard
  * **HS**: 2Man Saturday
  * **C1**: 2Man Collection Overnight
  * **C2**: 2Man Collection Standard
  * **CS**: 2Man Saturday Only
* **Consignment services**: Supports a maximum of 999 packages in a shipment, but the SAPIENT maximum—99 will be used instead.

## Carrier API services

The following API services are provided by the UPS integration:

* **Get Session Key**: The integration to authenticate and authorise users to use the carrier services via API.
* **Add Consignment**: The integration for creating shipments to reflect DXF as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
* **Get Labels**: The integration to retrieve package labels in the <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
* **Delete consignment**: The integration to delete an existing shipment cancelled in SAPIENT.

## Integration types

The following integration types are available for this integration:

* **Label integration**: Enables retrieving the package label in the PDF or ZPL format.
* **Tracking integration**: Enables data files to be sent via SFTP for both—1Man and 2Man services.

In SAPIENT, you can integrate with various available DX Freight services and features to streamline your shipping process.

In this section, learn how to:

* [Add a DX Freight shipping account](https://docs.intersoftsapient.net/docs/add-dx-freight-shipping-account)
* [Add a DX Freight tracking account](https://docs.intersoftsapient.net/docs/add-dx-freight-tracking-account#/)

<br />
