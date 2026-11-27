---
title: Asendia
excerpt: >-
  Asendia is a global e-commerce and mail delivery specialist and is a joint
  venture, between La Poste and Swiss Post, offering international delivery to
  over 200 countries, handling final mile delivery via partner couriers. 
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/f2d57c2f07af4f94d6e53f49acf46b9ad861884094f7a7df61afff48c15c7851-Asendia_banner_White.png" align="center" width="900px" />

***

Asendia is an API integration and in SAPIENT, it integrates with its newest AShipping solution. The integration of Asendia into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns="3">
      <Card title="Shipping Origins" icon="fa-solid fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) and Northern Ireland (country code GB and postcodes beginning with BT).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and Rest of teh World (<Glossary>ROW</Glossary> ) destinations.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary>,<Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>  incorterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> and <Glossary>ZPL203DPI</Glossary> formats.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single-Piece Shipments" icon="fa-solid fa-box">
        Asendia only support single package services. Consignment services are not supported in this integration.
      </Card>

      <Card title="Hazardous Shipments" icon="fa-solid fa-triangle-exclamation">
        Hazmat shipments are only supported with the e-PAQ Select and Elite DG services.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-truck">
        Asendia has its own distinct package types that specifies whether the shipment to EU is either **B** (Boxable) or **N** (Non-boxable) on e-PAQ Standard and e-PAQ Plus services.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="far fa-circle-info" theme="info">
      ### **_Note_**

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the Asendia integration.

    |           Service name          | Description                                                                                                                                                  |
    | :-----------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
    |   **e-PAQ Standard Priority**   | This service provides cost-effective international postal delivery for lightweight parcels, with priority handling for faster delivery.                      |
    | **e-PAQ Standard Non-Priority** | This service provides economical international postal delivery for lightweight parcels where delivery speed is less critical.                                |
    |      **e-PAQ Plus Mailbox**     | This service provides tracked international postal delivery to the recipient’s mailbox, with tracking at key shipment milestones.                            |
    |     **e-PAQ Plus Personal**     | This service provides tracked international postal delivery with personal delivery and an optional signature on receipt.                                     |
    |         **e-PAQ Select**        | This service provides fully tracked international parcel delivery through local e-commerce delivery specialists, with flexible delivery and customs options. |
    |      **e-PAQ Select (DG)**      | This service provides tracked international parcel delivery for eligible dangerous goods through local e-commerce delivery specialists.                      |
    |    **e-PAQ Elite – Economy**    | This service provides fully tracked international courier delivery using an economy option for less time-sensitive shipments.                                |
    |    **e-PAQ Elite – Express**    | This service provides fast, fully tracked international courier delivery for urgent and high-value shipments.                                                |
<br />

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the&#x20;_[_Get Carrier Services_](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_&#x20;endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect Asendia as a primary carrier and allowing users to create shipments using the <Anchor target="_blank" href="">Create Shipment</Anchor> endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      <Anchor target="_blank" href="">Generate and return the label</Anchor> for an Asendia shipment in the PDF or ZPL203DPI format. This endpoint must be utilised when the label is not generated in the Asendia Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <br />

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. With the [ SAPIENT tracking webhook](https://docs.intersoftsapient.net/docs/tracking-webhook), users can get detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add Asendia Shipping Account" href="https://docs.intersoftsapient.net/docs/add-asendia-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your Asendia shipping account to start creating shipments.
      </Card>

      <Card title="Add Asendia Tracking Account" href="https://docs.intersoftsapient.net/docs/add-asendia-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your Asendia shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT Asendia API" icon="fa-solid fa-code" target="_blank">
        Explore the Asendia API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Asendia and manage your shipping operations from a single platform.
  </Card>
</Cards>