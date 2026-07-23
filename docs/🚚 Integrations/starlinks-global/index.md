---
title: Starlinks Global
excerpt: "Starlinks Global is a partner carrier providing international and domestic delivery solutions. They offer global delivery solutions for seamless cross-border trade, helping retailers deliver to nearly\_200 countries, even the regions which are typically complex to reach."
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
The integration of Starlinks Global into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Send shipments to Great Britain (GB), Europe (EU), and <Glossary>ROW</Glossary> (Rest of the World).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration supports outbound shipping only.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary>, and <Glossary>ZPL300DPI</Glossary> labels.
      </Card>

      <Card title="Incoterms" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
      <Card title="Single-package Services" icon="fa-solid fa-box">
        Starlinks Global supports single-package services only. Consignment services are not supported.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 *Note*
    >
    > *There are no service enhancements for this integration.*
  </Tab>

  <Tab title="Carrier Services">
    The following services are available through the Starlinks Global integration.

    | Service Name | Description |
    | :--- | :--- |
    | **International Home Delivery** | Delivers parcels internationally to the recipient’s home address. |
    | **International Express Service – Starlinks** | Provides expedited international delivery with end-to-end Starlinks handling. |
    | **International Express Service – Last-Mile** | Provides expedited international delivery, with final delivery completed by a local last-mile carrier. |
    | **Final Mile** | Provides last-mile delivery from the destination hub to the recipient. |
    | **Domestic** | Provides domestic parcel delivery within supported countries, including the UK, USA, and Australia. |
    | **Cross Border Direct – Starlinks Label** | Provides cross-border parcel delivery using a Starlinks shipping label. |
    | **Cross Border Direct – Last-Mile Label** | Provides cross-border parcel delivery using a last-mile carrier label for final delivery. |
    | **Starlinks Domestic Premium** | Provides premium domestic delivery within supported countries, including the UK, USA, and Australia. |
    | **Cross Border Light** | Provides a cost-effective cross-border delivery solution for lightweight shipments. |
    | **Starlinks Border Flexi – Starlinks Label** | Provides flexible cross-border delivery using a Starlinks shipping label. |
    | **Starlinks Border Flexi – Last-Mile Label** | Provides flexible cross-border delivery, with final delivery performed by a local last-mile carrier. |
    | **Starlinks Market Places – Starlinks Label** | Provides cross-border marketplace shipment delivery using a Starlinks shipping label. |
    | **Starlinks Market Places – Last-Mile Label** | Provides cross-border marketplace shipment delivery, with final delivery completed by a local last-mile carrier. |

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint.*
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect Starlinks Global as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment">
       Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).
    </Accordion>

    <br />

  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return a label for a Starlinks Global shipment in PDF, PNG, or ZPL format. Use this endpoint when a label was not generated by the Starlinks Global Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the shipment status to label printed. Call it when you print or create the label, based on your business process. Update shipments to label printed before manifesting.*
    </Accordion>
    <br />

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add Starlinks GLobal Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/v4.04/docs/add-starlinks-global-shipping-account">
        Set up your Starlinks Global shipping account to start creating shipments.
      </Card>

      <Card title="Add Starlinks Global Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/v4.04/docs/add-starlinks-global-tracking-account">
        Configure tracking for your Starlinks Global shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT Starlinks Global API" icon="fa-solid fa-code" href="">
        Explore the Starlinks Global API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Starlinks Global and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
