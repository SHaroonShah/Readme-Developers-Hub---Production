---
title: A-Scan FAQs
excerpt: Frequently asked questions reagrding the International Arrivals Container API.
deprecated: false
hidden: false
metadata:
  robots: index
---
<Accordion title="Is A-Scan mandatory?">
  The International Product Team have mandated that all Freight to Post customers must have an A-Scan set up.
</Accordion>

<Accordion title="Can you have multiple services in one container?">
  No, you cannot mix different services within a bag. The bags must be separated by service in accordance with the mail preparation specifications for each service.
</Accordion>

<Accordion title="Are there any limits regarding the container’s weight?">
  Yes, teh following are the accepted bag weights:

  • Minumum weight 1.500 Kg

  • Maximum weight applies to the following conditions:

  • 30 Kg for any GB shiipments

  • 11 Kg for any non-GB shipments, for example, those using the DEI, DEJ, PS5, PS7, and so on.
</Accordion>

<Accordion title="How many parcel formats can the containers have?">
  Containers can only have one parcel format. This format is poupulated in the **RmContentFormat** field with one of the following values:

  • **G**: Large Letters and Parcels

  • **P**: Small Letters
</Accordion>

<Accordion title="When should the container be finalised?">
  The container must be finalised latest by one hour before the flight lands in the UK, so that Royal Mail can receive all the data on time.
</Accordion>

<Accordion title="What needs to pupolated in the **rmService** field?">
  The \**RMService* field must be populated with P (Prioroty).
</Accordion>