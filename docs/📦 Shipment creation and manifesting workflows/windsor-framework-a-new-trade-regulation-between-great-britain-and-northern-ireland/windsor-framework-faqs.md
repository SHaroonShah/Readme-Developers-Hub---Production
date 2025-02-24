---
title: Windsor Framework FAQs
excerpt: >-
  The Windsor Framework is an agreement between the UK and EU to manage trade
  from mainland GB to Northern Ireland, which is also part of GB, following
  Brexit.
deprecated: false
hidden: false
metadata:
  robots: index
---
Before sending your shipments to Northern Ireland, Intersoft recommends you to do do the following:

* [ ] Review the full breakdown of the technical requirements and populate the fields outlined in the example script provided in the [Windsor Framework](https://docs.intersoftsapient.net/docs/windsor-framework-a-new-trade-regulation-between-great-britain-and-northern-ireland) section.
* [ ] Confirm the mandatory fields with the <Glossary>carrier</Glossary> to ensure compliance.

&#x20;&#x20;

<Accordion title="Does the Windsor Framework affect all customers?">
  The Windsor Framework only affects customers sending goods from Great Britain (Great Britain) to Northern Ireland (Northern Ireland). The new regulations do not affect goods sent from Northern Ireland to Great Britain or from Northern Ireland to Northern Ireland, or items of correspondence.
</Accordion>

<Accordion title="Are all carriers subject to the  Windsor Framework?">
  Yes. The regulations apply to all carriers and will take effect from 31 March 2025, however, If a carrier only ships B2C (business to consumer) or C2C (consumer to consumer) parcels between Great Britain (GB) and Northern Ireland (NI), the Windsor Framework applies, but with fewer restrictions. Some items like food, plants and medicines may need extra checks.
</Accordion>

<Accordion title="What do I need to do if I am a Business to Business (B2B) customer?">
  If you are shipping B2B (Business-to-Business) from Great Britain to Northern Ireland, the requirements depend on the shipment value and whether you have a UKIMS pre-registration number.

  1. **Shipments Over £135**

  • You must provide a UKIMS pre-registration number.

  • Item HS Code is optional if a UKIMS number is provided.

  • Item Country of Origin is mandatory.

  2. **Shipments £135 or Under**

     • You can ship with or without a UKIMS pre-registration number.

     • If a UKIMS number is provided → Item HS Code is optional.

     • If no UKIMS number is provided → Item HS Code is mandatory.

     • Item Country of Origin is always mandatory.

  3. **UKIMS Number Validation**

     • If a UKIMS number is provided, it must include either the sender’s or receiver’s EORI number.

  If it does not match the  EORI numbers, the shipment will be rejected.
</Accordion>

<Accordion title="What do I need to do if I am a Business to Consumer (B2C) customer?">
  As a B2C customer shipping from Great Britain to Northern Ireland, you do not need to provide the following:

  • **Item HS Code**

  • **Item Country of Origin**

  You do not need to worry about UKIMS numbers or pre-registration requirements—these only apply to B2B shipment
</Accordion>

<Accordion title="What is the UK Internal Market Scheme (UKIMS)?">
  The UK Internal Market Scheme is an authorisation that allows registered businesses to declare your goods ‘not at risk’ if they are brought into Northern Ireland for sale or final use by end consumers in Northern Ireland (and Great Britain in the case of movements from Great Britain) and meet all the other criteria to move under UKIMS as set out in the guidance. For further details on its benefits, eligibility and registration, visit GOV.UK.
</Accordion>

<Accordion title="Can I use a UK Internal Market Scheme (UKIMS) that is not the senders?">
  Yes, but only under specific conditions and depending on the carriers. The UKIMS number provided must belong to the Northern Ireland recipient (consignee) or a recognised trader responsible for the movement. Further details can be found here.

  Please see below carrier specific requirements

  • **DX**: Do not have a field to capture UKIMS. There is a field in the create shipment request for DX to declare a 					shipment as UKIMS compliant, that is the only data required by DX for UKIMS.

  • **Evri**: Does not support B2B (Business to Business) shipments, so UKIMS isn’t applicable.

  • **Royal Mail**: Customer can provide either sender or receiver UKIMS, but the EORI portion of the UKIMS provided must 			contain either the sender or receiver EORI provided for the shipment. If the UKIMS provided does not contain either 			the sender or receiver EORI, the shipment will fail.

  • **UPS**: Customer supplies UKIMS number to UPS which is  set against their account in UPS’ system, we do not supply it 			 in the API request.
</Accordion>