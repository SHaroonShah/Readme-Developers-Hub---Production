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
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Royal Mail works in collaboration with the Ministry of Defence to provide BFPO services, handling the logistics of BFPO mail delivery; and as a part of its broader mailing services network, it ensures that military personnel receive their correspondence and packages in a timely manner.

In SAPIENT, you can use the **createShipment** request to facilitate the BFPO <<glossary:shipments>>. 

The British Forces Post Office® (BFPO) offers discounted mail delivery up to 2kg. 

The services that can be used for BFPO destinations are all domestic services, including Standard, Special Delivery and Tracked.

The **createShipment** request must contain the destination information in the following format:

**ContactName**: service number, rank, and name.  
**Address Line1**: Unit or Regiment.  
**Town**: Operation or location name (if applicable).  
**Postcode**: BFPO postcode.

> 🚧 _Important_
> 
> _The shipments to BFPO locations are supported by all Royal Mail domestic services and are not restricted to BF services only. Although RM allows customers to use a domestic service to ship to BFPO, you are advised to provide certain information that you would otherwise provide for the international shipments, such as the reason for export. This will return the response with the relevant documents and <<glossary:CN23>> that must be attached to the parcel._