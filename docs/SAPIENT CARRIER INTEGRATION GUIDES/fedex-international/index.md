---
title: FedEx International Connect
excerpt: >-
  FedEx is a global leader in logistics and delivery services, renowned for its
  reliable express shipping and comprehensive transportation solutions. It
  offers a range of shipping options tailored for various international markets,
  making it an essential partner for businesses seeking to optimise their
  shipping operations.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/094a6ea764d7d28798166aaaafe13e3fbe491279d79b1fd691766a419eb13352-FedEx_white_banner.png" />

***

FedEx International Connect is a flexible, cost-effective, worldwide delivery solution with standard e-commerce shipments in mind. Designed to help retailers connect with customers around the globe.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe (EU), and the Rest of the World (<Glossary>ROW</Glossary>).  
> *Please note that this integration does not support shipping to China, Russia, and Australia.*
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format only.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    * **Single-piece shipments**: The integration supports single-piece shipments. Consignment services are not supported by this integration

    > 📘 *Note*
    >
    > *Please bear in mind that not all services offer consignment options.*
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 _Note_
>
> _There are no service enhancements for this integration._
  </Tab>
</Tabs>

<br />

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).

> 📘 _Note_
>
> _The FedEx International Connect does not support shipping to the following ROW countries:_
>
> * _China_
> * _Russia_
> * _Australia_

* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid) and <Glossary>DDP</Glossary> (Delivered Duty Paid).
* **Service Type**: The integration is focused on outbound shipping.
* **label formats**: <Glossary>PDF</Glossary>

## Service enhancements

> 📘 _Note_
>
> _There are no service enhancements for this integration._

## Additional features

The FedEx International Connect integration provides support for single-piece shipments. Consignment services are not supported by this integration.

## Carrier API services

The following API services are provided by the FedEx International Connect integration:

* **Create shipment**: The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the Create Shipment API endpoint that returns the label in base64 encoded format.
* **Tracking**: Provides the tracking data via the tracking webhook.

## Integration types

* **Label integration**: The system generates the label by populating a stored label template with the relevant shipment data.

> 📘 _Note_
>
> _If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels._

* **Tracking integration**: Enables data files to be sent via SFTP and received through the SAPIENT tracking webhook.

***

In this section, learn now to:

* <Anchor label="Add a FedEx International Connect shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-international-shipping-account">Add a FedEx International Connect shipping account</Anchor>
* <Anchor label="Add a FedEx International Connect tracking account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-international-tracking-account">Add a FedEx International Connect tracking account</Anchor>
