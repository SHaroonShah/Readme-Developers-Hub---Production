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
<Cards columns={1}>
     <Card title="Single Package Shipments" icon="fa-solid fa-box">
The integration supports single-package shipments. Consignment services are not supported by this integration

    </Card>
</Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 _Note_
>
> _There are no service enhancements for this integration._
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect EVRi as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest shipment" icon="plus-circle">
      Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for an EVRi shipment in the PDF or PNG format. This endpoint must be utilised when the label is not generated in the EVRi Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking" icon="print">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For EVRi shipments, the data files are sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

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
