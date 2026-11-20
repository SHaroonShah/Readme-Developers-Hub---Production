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
> 🚧 _Important_
>
> _This integration is currently under development. The contents are to be updated as soon as possible._

Asendia is an API integration and in SAPIENT, it integrates with its newest AShipping solution.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and the <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>ZPL203DPI</Glossary>.

## Service enhancements

<Callout icon="far fa-circle-info" theme="info">
  ### **_Note_**

  _There are no service enhancements for this integration._
</Callout>

## Additional features

The Asendia integration provides the following additional features:

* **Single-piece shipments**: Asendia only support single package services. Consignment services are not supported in this integration.
* **Hazardous shipments**: Hazmat shipments are only supported with the e-PAQ Select and Elite DG services.
* **Package Types**: Asendia has its own distinct package types that specifies whether the shipment to EU is either **B** (Boxable) or **N** (Non-boxable) on e-PAQ Standard and e-PAQ Plus services.

## Carrier services

The following are the key services are provided by the Asendia integration:

* e-PAQ Standard Priority: This service provides cost-effective international postal delivery for lightweight parcels, with priority handling for faster delivery.
* e-PAQ Standard Non-Priority: This service provides economical international postal delivery for lightweight parcels where delivery speed is less critical
* e-PAQ Plus Mailbox: This service provides tracked international postal delivery to the recipient’s mailbox, with tracking at key shipment milestones.
* e-PAQ Plus Personal: This service provides tracked international postal delivery with personal delivery and an optional signature on receipt.
* e-PAQ Select: This service provides fully tracked international parcel delivery through local e-commerce delivery specialists, with flexible delivery and customs options.
* e-PAQ Select (DG): This service provides tracked international parcel delivery for eligible dangerous goods through local e-commerce delivery specialists
* e-PAQ Elite – Economy: This service provides fully tracked international courier delivery using an economy option for less time-sensitive shipments.
* e_PAQ Elite – Express: This service provides fast, fully tracked international courier delivery for urgent and high-value shipments.

<Callout icon="💡" theme="default">
  ### _Tip_

  _For the most up-to-date carrier services, use the&#x20;_[_Get Carrier Services_](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_&#x20;endpoint._
</Callout>

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect EVRi as a primary carrier and allowing users to create shipments using the <Anchor target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-evri">Create Shipment</Anchor> endpoint.
    </Accordion>

    <Accordion title="Manifest shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      [Generate and return the label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-evri-shipmentid) for an EVRi shipment in the PDF or PNG format. This endpoint must be utilised when the label is not generated in the EVRi Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For EVRi shipments, the data files are sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add EVRi Shipping Account" href="https://docs.intersoftsapient.net/v4.04/docs/shipping-account-setup-3" icon="fa-solid fa-truck" target="_blank">
        Set up your EVRi shipping account to start creating shipments.
      </Card>

      <Card title="Add EVRi Tracking Account" href="https://docs.intersoftsapient.net/v4.04/docs/tracking-account-setup" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your EVRi shipments.
      </Card>

      <Card title="Add Child Client Department to Parent Shipping Account" href="https://docs.intersoftsapient.net/v4.04/docs/client-id-and-child-clinet-id-management-1" icon="fa-solid fa-circle-user" target="_blank">
        Create a parent shipping account and have multiple sub-accounts.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT EVRi API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-evri" icon="fa-solid fa-code" target="_blank">
        Explore the EVRi API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with EVRi and manage your shipping operations from a single platform.
  </Card>
</Cards>
