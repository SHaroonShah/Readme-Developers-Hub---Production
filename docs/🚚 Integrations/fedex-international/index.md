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

<Image src="https://files.readme.io/11f3505da255437d51f49130804e89b67ffeb214e0eedaea1399d1293eb8ab3e-FIC_banner_white.png" align="center" width="900px" />


***

FedEx International Connect is a flexible, cost-effective, worldwide delivery solution with standard e-commerce shipments in mind. Designed to help retailers connect with customers around the globe.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe (EU), and the Rest of the World (<Glossary>ROW</Glossary>).

        > _Please note that this integration does not support shipping to China, Russia, and Australia._
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


  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single Package Shipments" icon="fa-solid fa-box">
        The integration supports single-package shipments. Consignment services are not supported by this integration
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
    The following key services are provided by the FedEx International Connect integration.

    | Service Name                     | Description                                                                                                                                                                                                                                                 |
    | :------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **FIC - Express Priority**       | This service provides expedited international delivery for e-commerce shipments, offering faster transit times than standard International Connect services, with end-to-end tracking, customs clearance, and priority handling across global destinations. |
    | **FIC - Tracked Worldwide** (UK) | This service provides cost-effective international e-commerce delivery from the UK, offering global coverage, end-to-end tracking, and customs-cleared delivery for less urgent shipments to over 220 countries and territories.                            |
    | **Royal Mail Tracked 24**        | This service provides next-working-day delivery within the UK with full end-to-end tracking, delivery notifications, and proof of delivery, offering a fast and reliable domestic shipping solution.                                                        |
    | **Royal Mail Tracked 48**        | This service provides cost-effective UK delivery within 2–3 working days with full tracking, delivery notifications, and proof of delivery, suitable for less urgent domestic shipments.                                                                    |



    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect FedEx International Connect as a primary carrier and allowing users to create shipments using the Create Shipment API endpoint that returns the label in base64 encoded format.
    </Accordion>



    <Accordion title="Manifest shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.

      <Callout icon="📘" theme="info">
        ### _Note_

        _If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels._
      </Callout>
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a FedEx International Connect shipment in the PDF format. This endpoint must be utilised when the label is not generated in the FedEx International Connect Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
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
      <Card title="Add FedEx International Connect Shipping Account" href="https://docs.intersoftsapient.net/docs/add-fedex-international-shipping-account" icon="fa-solid fa-truck">
        Set up your FedEx International Connect shipping account to start creating shipments.
      </Card>

      <Card title="Add FedEx International Connect Tracking Account" href="https://docs.intersoftsapient.net/docs/add-fedex-international-tracking-account" icon="fa-solid fa-search-location">
        Configure tracking for your FedEx International Connect shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT FedEx International Connect API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-fic" icon="fa-solid fa-code">
        Explore the FedEx International Connect API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with FedEx International Connect and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />

<br />
