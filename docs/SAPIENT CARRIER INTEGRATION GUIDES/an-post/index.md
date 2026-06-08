---
title: An Post
excerpt: >-
  An Post is the national postal service provider of Ireland. It offers a
  variety of services including mail delivery, parcel shipping, and financial
  services.  It provides a comprehensive range of postal services, including
  mail delivery, parcel shipping, and logistics solutions. An Post is known for
  its extensive network of post offices across Ireland, offering not just
  mailing services but also banking and government services.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/d86245cf158e8d0443810c7cd372e3bdf92fa171e4f3f933a46e26f30b1d64b2-An_Post_white_banner.png" />

***

The integration of An Post, Ireland's national postal service, into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Ireland (IE) and Great Britain (GB).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Ireland (IE), Great Britain (GB), Europe, and the Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound and inbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> only.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration support labels in <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
      </Card>
    </Cards>

    <br />

    <Accordion title="Important considerations">
      Please bear in mind the following:

      * An Post does not support consignment services; all services are single-package services only. Also, the Express International and Priority Post services are only available to limited destinations.
      * If shipping from GB to Ireland, undelivered or returned parcels will not be returned to your UK address. Instead, they must be returned to a designated PO Box address at the Portlaoise Mail Centre in Ireland. This information must be populated in the **ReturnToSender** section of the API documentation
    </Accordion>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single Piece Shipments" icon="fa-solid fa-box">
        An Post only supports single package services. Consignment services are not supported
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 *Note*
    >
    > *There are no service enhancements for this integration.*
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect An Post as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint. Based on the destination country, customers must be aware of the following:

      * * For delivery to addresses in Northern Ireland (IE), only the shipping <Glossary>label</Glossary> is required.
          * For delivery to EU destinations excluding Northern Ireland (IE), a security declaration is required.
          * The signature image will be taken from the signature image the customer has uploaded for the shipping account in the [Logos and Signatures](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) screen.
            * For delivery to ROW addresses, including GB and Northern Ireland (IE), a shipping label and <Glossary>CN23</Glossary> is required. SAPIENT will generate a separate address label and CN23, as this is consistent with the behaviour for other integrations.

      > 📘 *Note*
      >
      > *Please be advised that the existing SAPIENT CN23 format will be used*.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment" icon="plus-circle">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for an An Post shipment. This endpoint must be utilised when the label is not generated in the An Post Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking" icon="print">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/add-an-post-shipping-account" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up An Post shipping account on SAPIENT.
      </Card>

      <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/add-an-post-tracking-account" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up An Post tracking account on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Advanced Features">
    <Cards columns={2}>
      <Card title="Add Barcode Ranges" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-an-post-shipping-account" icon="fa-solid fa-barcode">
        Add barcode ranges to facilitate efficient tracking and management of shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT An Post API " href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-anpost" icon="fa-solid fa-code">
        Explore the An Post API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with An Post and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
