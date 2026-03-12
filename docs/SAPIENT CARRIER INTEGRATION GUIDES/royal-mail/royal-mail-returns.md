---
title: Return shipments
excerpt: >-
  The _return shipments_ is a logistical service provided by carrier in the
  logistics industry. This service allows the customers to send back items they
  have purchased but do not want to keep, typically due to reasons such as
  dissatisfaction, wrong items, defects, or simply a change of mind. This
  service is an essential aspect of e-commerce and retail operations, as it
  provides a streamlined process for handling returns efficiently.
deprecated: false
hidden: false
icon: fad fa-reply
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, if you are a Royal Mail customer, you can use the return service as follows:

The only API call that you must develop for Royal Mail return services is [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm), which is used to generate the <Glossary>labels</Glossary> for your packages.

## Requirements for return labels

To ensure the correct generation of the return labels, meet all of the following requirements:

<Accordion title="Destination section" icon="fa-location-dot">
  Populate with the details of where you would like the <Glossary>items</Glossary> to be returned.
</Accordion>

<Accordion title="Return to Sender section" icon="fa-rotate-left">
  Populate with the details of the person returning the item(s). This information is displayed on the side of the label.
</Accordion>

<Accordion title="Shipper section" icon="fa-truck">
  Populate with the details of the person returning the item(s). This is also the address that will be used for Parcel Collection.
</Accordion>

<Accordion title="ServiceCode" icon="fa-barcode">
  Populate with either <Glossary>TSN Tracked Returns 24</Glossary>, or <Glossary>TSS Tracked Returns 48</Glossary>.

  For Royal Mail Importers, this can also be populated with *ITA Tracked Returns 24* or *ITB Tracked Returns 48*. Speak to your Royal Mail account manager to confirm which service code you should be using.
</Accordion>

> 📘 _Note_
>
> _The labels created for the return service do not have to be manifested._

## Optional: Paperless returns with QR code

If you are interested in the paperless return solution for your customers, you can generate a QR code after creating the shipment and share it with the end consumer. The customer can then take it to the post office, either printed or on a mobile device, and scan it to have the returns label printed.

***

## API refrences

<Cards columns={2}>
  <Card title="Create Shipment" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-plus">
    Generate return labels for your packages.
  </Card>

  <Card title="Print My Label QR Code" href="https://docs.intersoftsapient.net/reference/get_v4-shipments-printmylabelqrcode-rm-shipmentid" icon="fa-qrcode">
    Generate a QR code for paperless returns.
  </Card>
</Cards>
