---
title: BFPO shipments
excerpt: >-
  The _British Forces Post Office (BFPO)®_ is a postal service that operates to
  provide mail and parcel delivery to British military personnel, their
  families, and official organisations stationed abroad or in remote locations.
  The BFPO system enables service members to send and receive mail as if they
  were in the UK, regardless of their posting overseas.
deprecated: false
hidden: false
icon: fad fa-person-military-to-person
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Royal Mail works in collaboration with the Ministry of Defence to provide BFPO services, handling the logistics of BFPO mail delivery. As part of its broader mailing services network, it ensures that military personnel receive their correspondence and packages in a timely manner.

In SAPIENT, you can use the **createShipment** request to facilitate the BFPO <Glossary>shipments</Glossary>.

<Callout icon="📘" theme="info">
  ### _Note_

  Before creating a BFPO shipment, bear in mind the following key features:

  - The British Forces Post Office® (BFPO) offers discounted mail delivery up to 2kg.
  - BFPO destinations support all domestic services, including Standard, Special Delivery, and Tracked.
</Callout>

## Destination format

The **createShipment** request must contain the destination information in the following format:

| Field             | Value                                      |
| ----------------- | ------------------------------------------ |
| **ContactName**   | Service number, rank, and name             |
| **Address Line1** | Unit or Regiment                           |
| **Town**          | Operation or location name (if applicable) |
| **Postcode**      | BFPO postcode                              |

<Callout icon="🚧" theme="warn">
  ### _Important_

  _The shipments to BFPO locations are supported by all Royal Mail domestic services and are not restricted to BF services only. Although Royal Mail allows customers to use a domestic service to ship to BFPO, you are advised to provide certain information that you would otherwise provide for the international shipments, such as the reason for export. This will return the response with the relevant documents and <Glossary>CN23</Glossary> that must be attached to the parcel._
</Callout>

<br />
