---
title: Shipments
excerpt: Any item transported from one point to another.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Shipment Information**

* General Information about the shipment, including units of measurement and currency code. Not all Shipment Information elements are mandatory. Depends on the destination, carrier, content type, and reason for export.

**Label Format**

* This is the format labels for the shipment that will be returned upon the successful creation of the shipment. The labels are returned as a base64 string that will need to be converted by your integration in the format they have been generated.
  * **PDF** - a Base 64 encoded PDF text that must be converted using a base64 to PDF convertor to create a PDF label.
  * **PNG** – a Base 64 encoded PNG text that must be converted using a base64 to PNG convertor to create a PNG label.
  * **ZPL203DPI** – a Base 64 encoded text for Zebra printer at 203 DPI – ZPL (Zebra Programming Language) the printing control language used by Zebra printers.
  * **ZPL300DPI** - a Base 64 encoded text for Zebra printer at 300 DPI
  * **DATASTREAM** is only available if it has been activated on your account. Label components broken down into a data-stream, for you to draw your own label.

**Content Type**

* This is the nature of the items in your shipment. A shipment can only have one Content Type.
  * **DOX** – the shipment contains only documents and does not have commercial value.
  * **NDX** – non documents, the shipment contains items with commercial values.
  * **HV** – items with high commercial value.

**Description Of Goods**

* This is a short generic description of the content of the shipment, for example: electrical goods, beauty items, women fashion, men shoes.

**Business Transaction Type**

* Describes the shipment’s commercial transaction type, Business to Consumer. Business to Business, etc. Some carriers require it.

**Domestic Shipments**

* Domestic shipping is when goods or documents are shipped within a country's borders. When you ship domestically, you don’t usually need to include any documents beyond a shipping label.

**International Shipments**

* International shipping is importing and exporting goods between different countries. International shipping is the process of moving goods over borders, accompanied by many rules and regulations. To successfully import or export goods, businesses must know and follow specific policies of international shipping.

**Dutiable Shipments**

* Dutiable shipments are subject to a customs duty, which is a tariff or tax imposed on goods when transported across international borders.

**Non-Dutiable Shipments**

* Shipments that are not subject to custom taxes. Applicable to DOX shipments to and from any destination, and domestic shipments of any type (DOX, NDX or HV) and EU to EU shipments of any type (DOX, NDX and HV)

**Reason For Export**

* This can be carrier specific. Royal Mail accepts the following reasons for exports.\
  Gift\
  Commercial Sample\
  Documents\
  Sale of Goods\
  Return of Goods\
  Mixed Content\
  Other

**Incoterms**

* Incoterms, widely used terms of sale, are a set of 11 internationally recognized rules which define the responsibilities of sellers and buyers. Incoterms specify who is responsible for paying and managing the shipment, insurance, documentation, customs clearance, and other logistical activities. The rules are revised periodically by the International Chamber of Commerce (ICC). The last review has been made in 2020. Although the ICC recommends using Incoterms® 2020 from beginning January 1, 2020, parties to a sales contract can agree to use any version of Incoterms. [https://www.incotermsexplained.com/the-incoterms-rules/incoterms-2010-rules/](https://www.incotermsexplained.com/the-incoterms-rules/incoterms-2010-rules/)API v4 currently supports the following Incoterms:
  * **DAT** - Delivered At Terminal - The seller is responsible for arranging carriage and for delivering the goods, the buyer is responsible for import clearance and any applicable local taxes or import duties.
  * **DAP** - Delivered At Place - The seller is responsible for arranging carriage and for delivering the goods, ready for unloading from the arriving means of transport, at the named place.
  * **DDP** - Delivered Duty Paid - A delivery agreement whereby the seller assumes all the responsibility, risk, and costs associated with transporting goods until the buyer receives or transfers them at the destination port. i.e. The sender is responsible for paying import customs duties.
  * **DDU** - Delivered Duty Unpaid - Means the seller fulfils his delivery obligation when the goods have been delivered at the designated location in the importing country. The receiver is responsible for paying import customs duties. This is the most used incoterm.

**Single Piece Shipment**

* It is a single package shipment. If a shipment has multiple packages, each package is shipped, tracked, and delivered individually.

**Multi Piece Shipment** (Consignment)

* Is a shipment containing more than one package.

**Consignment Service**

* A carrier service that allows multiple packages to be sent as one shipment (consignment). Not all carriers have consignment services.

**Tracking Number**

* Tracking numbers are identifiers assigned to packages when they are shipped. Tracking numbers are useful for knowing the location of time sensitive deliveries. It is a unique ID number or code assigned to a package or parcel.

**Consignment Tracking Number**

* Unique identifier for a consignment
