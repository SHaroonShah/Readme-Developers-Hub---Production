---
title: InPost
excerpt: >-
  InPost is a Polish public logistics limited company with courier, package
  delivery and express mail service. The company specialises in parcel locker
  service operated in Poland, Italy, United Kingdom, France, Benelux, Spain, and
  Portugal.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/75762ee66dc10880c8cfd75e2d683174396ef3ed0fd727fd959f2eb44e013de6-InPost_white_banner.png" />

***

InPost provides a convenient, eco-friendly parcel delivery service through a network of 24/7 automated lockers and partnered shops in the UK. You can drop off or pick up parcels at these locations anytime, offering flexibility and ease for both senders and recipients.

This integration offers several key features that streamline the shipping process. This article summarises the in-scope features of the integration and provides detailed explanations of the associated process flows.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotlabd).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB) mainland only.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound and inbound shipping.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards column={1}>
      <Card title="Labelled B2C" icon="fa-solid fa-id-card">
        Generates and returns a label to be attached to the parcel for a B2C business transaction type deliveries.
      </Card>
<Card title="Labelless Returns Using QR Codes" icon="fa-solid fa-id-card">
  Generates a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.
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
> 📘 *Note*
      >
      > *If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels.*

    </Accordion>
    <br />
<Accordion title="Get PUDO locations" icon="plus-circle">
  Enable customers to users to access essential shipping options for both sending and returning packages seamlessly via the [Get PUDO Locations endpoint](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode).

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

* **API endpoints for shipment creation and QR code retrieval**: The integration includes specific API endpoints that developers can use to create shipments, get PUDO locations, and retrieve labels or QR codes. This enables seamless interaction between the InPost service and SAPIENT system, ensuring efficient data flow and functionality.
  * Create shipment for B2C and returns services
  * Get PUDO Locations

In this section, learn how to:

* <Anchor label="Add an InPost shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-inpost-shipping-account#/">Add an InPost shipping account</Anchor>
* [Use InPost PUDO service](https://docs.intersoftsapient.net/docs/pudo-integration#/)
