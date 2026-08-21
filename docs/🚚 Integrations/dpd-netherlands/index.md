---
title: DPD Netherlands (NL)
excerpt: >-
  DPD Netherlands (NL) is the branch of DPD operating in the Netherlands and is
  part of Geopost group.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/67505883534542d666a2fed1d64893c848534290da3ac931e7c09fce390c7fa5-DPD_NL_banner_white.png" align="center" width="900px" />


***

<br />

DPD NL ship domestically and internationally, and approximately 60% of their outbound volume is cross-border.

The integration of DPD NL into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and the Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Consignment services" icon="fa-solid fa-boxes-stacked">
        Consignment services are supported, and DPD UK allows a maximum of 99 packages per consignment.

        > _Please bear in mind that not all services offer consignment options._
      </Card>

      <Card title="Carrier-Specific Fields" icon="fa-solid fa-list-check">
        The **CarrierSpecifics** object in the **Create Shipment** request includes **DeliveryInstructions** for providing additional delivery instructions to the carrier.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards>
      <Card title="Proof of Identity" icon="fa-solid fa-id-card">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fa-solid fa-calendar-circle-user">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fa-solid fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fa-solid fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements and carrier services, refer to the following endpoints:_

      - _[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)_
      - _[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the DPD Netherlands integration.

    | Service Name                                             | Description                                                                                                                                                                                        |
    | :------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **DPD Business Normal Parcel**                           | This service provides standard business-to-business delivery for parcels up to 31.5 kg, offering reliable transport across the Netherlands and Europe with tracking and multiple delivery attempts |
    | **DPD Business Small Parcel**                            | This service provides business-to-business delivery for lightweight parcels up to 3 kg, enabling cost-effective shipping of smaller consignments with full tracking and reliable transit.          |
    | **DPD Home Normal Parcel**                               | This service provides home delivery for standard parcels up to 31.5 kg, including Predict notifications with a 1-hour delivery window and options for recipients to manage delivery preferences.   |
    | **DPD Home Small Parcel**                                | This service provides home delivery for lightweight parcels up to 3 kg, offering a convenient and cost-efficient solution with tracking and flexible delivery options for recipients.              |
    | **DPD ParcelLetter** (Only for delivery to NL addresses) | This service provides mailbox delivery for very small parcels up to 1 kg, allowing items to be delivered through the letterbox without requiring recipient presence within Netherlands only.       |
    | **DPD Shop Return**                                      | This service provides a flexible returns solution that allows customers to return parcels via DPD Parcel Shops using printed or digital labels, including QR code options without printing.        |
    | **DPD Home Saturday**                                    | This service provides home delivery on Saturdays, enabling parcels collected during the week to be delivered to residential addresses at the weekend with full tracking visibility.                |
    | **DPD Business Saturday**                                | This service provides business delivery on Saturdays, allowing shipments to be delivered outside standard weekday business hours for improved flexibility and continuity of operations.            |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect DPD NL as a primary carrier and allowing users to create individual shipments requests using the **Create Shipment** endpoint.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a DPD NL shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DPD NL Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add DPD Netherlands Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dpd-netherlands-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your DPD Netherlands shipping account to start creating shipments.
      </Card>

      <Card title="Add DPD Netherlands Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dpd-nl-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your DPD Netherlands shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT DPD Netherlands API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dpdnl" icon="fa-solid fa-code" target="_blank">
        Explore the DPD Netherlands API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DPD Netherlands and manage your shipping operations from a single platform.
  </Card>
</Cards>
