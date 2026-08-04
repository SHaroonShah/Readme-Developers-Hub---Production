---
title: Starlinks Global
excerpt: "Starlinks Global is a partner carrier providing international and domestic delivery solutions. They offer global delivery solutions for seamless cross-border trade, helping retailers deliver to nearly\_200 countries, even the regions which are typically complex to reach."
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
![](https://files.readme.io/f2a0fec9ac80f7564dafa93c51acde4175cd48e9b82c56bc40078318d18bdcf2-Starlinks_Global_banner.png)

***

The integration of Starlinks Global into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from Great Britain (GB), Unites States of America (USA), Australia, and United Arab Emirates (UAE).

        > _The integration also  supports ship domestically within USA, Australia, and UAE._
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Send shipments to Great Britain (GB), Europe (EU), Unites States of America (USA), Australia, United Arab Emirates (UAE), and <Glossary>ROW</Glossary> (Rest of the World).

        > _The integration also supports sending shipments domestically within USA, Australia, and UAE._
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
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single-package Services" icon="fa-solid fa-box">
        Starlinks Global supports single-package services only. Consignment services are not supported.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following services are available through the Starlinks Global integration.

    | Service Name                                  | Description                                                                                                      |
    | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------------- |
    | **International Home Delivery**               | Delivers parcels internationally to the recipient’s home address.                                                |
    | **International Express Service – Starlinks** | Provides expedited international delivery with end-to-end Starlinks handling.                                    |
    | **International Express Service – Last-Mile** | Provides expedited international delivery, with final delivery completed by a local last-mile carrier.           |
    | **Final Mile**                                | Provides last-mile delivery from the destination hub to the recipient.                                           |
    | **Domestic**                                  | Provides domestic parcel delivery within supported countries, including the UK, USA, and Australia.              |
    | **Cross Border Direct – Starlinks Label**     | Provides cross-border parcel delivery using a Starlinks shipping label.                                          |
    | **Cross Border Direct – Last-Mile Label**     | Provides cross-border parcel delivery using a last-mile carrier label for final delivery.                        |
    | **Starlinks Domestic Premium**                | Provides premium domestic delivery within supported countries, including the UK, USA, and Australia.             |
    | **Cross Border Light**                        | Provides a cost-effective cross-border delivery solution for lightweight shipments.                              |
    | **Starlinks Border Flexi – Starlinks Label**  | Provides flexible cross-border delivery using a Starlinks shipping label.                                        |
    | **Starlinks Border Flexi – Last-Mile Label**  | Provides flexible cross-border delivery, with final delivery performed by a local last-mile carrier.             |
    | **Starlinks Market Places – Starlinks Label** | Provides cross-border marketplace shipment delivery using a Starlinks shipping label.                            |
    | **Starlinks Market Places – Last-Mile Label** | Provides cross-border marketplace shipment delivery, with final delivery completed by a local last-mile carrier. |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
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



    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return a label for a Starlinks Global shipment in PDF, PNG, or ZPL format. Use this endpoint when a label was not generated by the Starlinks Global Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the shipment status to label printed. Call it when you print or create the label, based on your business process. Update shipments to label printed before manifesting._
      </Callout>
    </Accordion>



    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add Starlinks GLobal Shipping Account" href="https://docs.intersoftsapient.net/v4.04/docs/add-starlinks-global-shipping-account" icon="fa-solid fa-truck">
        Set up your Starlinks Global shipping account to start creating shipments.
      </Card>

      <Card title="Add Starlinks Global Tracking Account" href="https://docs.intersoftsapient.net/v4.04/docs/add-starlinks-global-tracking-account" icon="fa-solid fa-search-location">
        Configure tracking for your Starlinks Global shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT Starlinks Global API" icon="fa-solid fa-code">
        Explore the Starlinks Global API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with Starlinks Global and manage your shipping operations from a single platform.
  </Card>
</Cards>
