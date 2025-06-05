---
title: The Delivery Group
excerpt: >-
  The Delivery Group is a prominent carrier specializing in mail distribution
  services to enhance the efficiency of shipping and delivery processes.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The Delivery Group handover to other carries for final mile delivery of their shipments. Therefore, the services for this integration include services for carriers such as Evri and Yodel. We just create the shipment with The Delivery Group using the requested service, and The Delivery Group manage sending the data and transferring the shipment to the final mile carrier.

The Delivery Group integration provides the following key features:

* **Ship from destinations**: GB.
* **Ship to destinations**: GB, EU, ,<Glossary>ROW</Glossary>.
* **Outbound/Returns services**: Outbound only.
* **Package type**: Single-package shipments only. Consignment services are not supported.
* **Incoterms**: <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary>
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.
* **Carrier API services**: Tracking and SubmitItemAdvice

## Services

The following services are included in the The Delivery Group carrier integration:

* **SubmitItemAPI**: This is used to pre-advise the Delivery Group of shipments. In this case, We will request The Delivery Group to send the label in the **SubmitItemAdvice** response, which returns the shipment tracking number and label, therefore there is no need to call the **GetLabel** API to retrieve the label.
* **TrackingAPI**: The Delivery Group’s tracking API uses the same credentials as the **SubmitItemAdvice** API. Therefore, the username and password set on the shipping account linked to the tracking account is used to authorise requests to the Tracking API.

In this section, learn how to

* [Add the delivery group shipping account](https://docs.intersoftsapient.net/docs/the-delivery-group-account-set-up#/)
* [Add the delivery group tracking account](https://docs.intersoftsapient.net/docs/the-delivery-group-tracking-account-set-up#/)