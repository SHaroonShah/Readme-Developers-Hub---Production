---
title: YODEL
excerpt: >-
  YODEL is a UK logistics and parcel delivery service provider. This page
  explains the YODEL integration features, API services, and setup resources
  available through Intersoft SAPIENT.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: shipping-account-setup-1
      title: Yodel shipping account setup
---
<Image align="center" border={false} width="900px" src="https://files.readme.io/3d6b9cd3a2a729d7bb30ada0f5836b3330a213d5425aa775cd814a13b958e44d-YODEL_white_banner.png" />

***

YODEL is fully integrated into the Intersoft SAPIENT platform, allowing businesses to access YODEL’s delivery network through SAPIENT’s unified API.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).

        > *Shipments to Northern Ireland (NI) and the Channel Islands are treated as international.*
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid) incoterm only.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
      <Card title="Consignment Services" icon="fa-solid fa-boxes-stacked">
        The integration supports consignment services. The maximum number of packages depends on the service. Some services allow multiple packages, and some do not; the maximum number of packages is stored against the service.

        > *Multi-package requests are not supported for single-package services.*
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 *Note*
    >
    > *There are no service enhancements documented for this integration.*
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      Create YODEL shipments through the SAPIENT Create Shipment API endpoint.
    </Accordion>

    <br />

    <Accordion title="Label Integration" icon="plus-circle">
      The YODEL label integration is in-house, which means the label is generated within the SAPIENT system without calling the carrier API.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for a YODEL shipment using the SAPIENT Print Label API endpoint.
    </Accordion>

    <br />

    <Accordion title="Tracking" icon="print">
      The YODEL tracking integration enables data files to be sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={3}>
      <Card title="Add YODEL Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/shipping-account-setup-1">
        Set up your YODEL shipping account to start creating shipments.
      </Card>

      <Card title="Add YODEL Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/tracking">
        Configure tracking for your YODEL shipments.
      </Card>

      <Card title="Add a Tracking Barcode Range" icon="fa-solid fa-barcode" href="https://docs.intersoftsapient.net/docs/barcode-range-setup-1#/">
        Add a tracking barcode range to your YODEL shipping account.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT YODEL API" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-yodel">
        Explore the YODEL API endpoints for shipping account and shipment workflows.
      </Card>

      <Card title="Create YODEL Shipment" icon="fa-solid fa-box" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-yodel">
        Create YODEL shipments using the SAPIENT Create Shipment endpoint.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with YODEL and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />

<br />