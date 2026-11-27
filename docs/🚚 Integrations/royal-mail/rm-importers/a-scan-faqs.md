---
title: International Arrivals Containers FAQs
excerpt: >-
  Find answers to common questions about International Arrivals Containers
  (A-Scan).
deprecated: false
hidden: false
icon: fad fa-comment-question
metadata:
  robots: index
---
<Accordion title="Is A-Scan mandatory?">
  Yes. A-Scan is mandatory for all Freight 2 Post customers.
</Accordion>

<Accordion title="Can you have multiple services in one container?">
  No. You cannot mix different services in one container. You must use a separate container for each service, in line with the mail preparation requirements for that service.
</Accordion>

<Accordion title="Are there any container weight limits?">
  Yes. The following weight limits apply:

  - Minimum weight: 1.5 kg
  - Maximum weight for Import services: 30 kg
  - For other cross-border services, the maximum weight depends on the service used.
</Accordion>

<Accordion title="How many parcel formats can the containers have?">
  Containers can only have one parcel format. This format is poupulated in the **RmContentFormat** field with one of the following values:

  - **G**: Large Letter
  - **P**: Letter
  - **E**: Parcel
</Accordion>

<Accordion title="When should the container be finalised/ manifested?">
  The container must be finalised latest by one hour before the flight lands in the UK, so that Royal Mail can receive all the data on time.
</Accordion>

<Accordion title="What needs to pupolated in the RMService field?">
  The **RMService** field must be populated with **P** (Priority).
</Accordion>

<Accordion title="What are the event codes in the tracking API complete for ETSF?">
  You will first get the **PSAN** tracking event code which indicates that pre-advice was received by Royal Mail—then **PRID**—shipment received in the depot event once the shipment arrives in the UK.
</Accordion>